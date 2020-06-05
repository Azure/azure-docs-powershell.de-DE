---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 8d53923f76506469cdc2c111faf7c4568b54f7de
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294792"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="897fc-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="897fc-103">Azure PowerShell release notes</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="897fc-104">4.2.0: Juni 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-104">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-105">Az.Accounts</span></span>
* <span data-ttu-id="897fc-106">Problem behoben, das unter Umständen dazu geführt hat, dass Az Protokolle in Azure Automation- oder PowerShell-Aufträgen übersprungen hat [Nr. 11492]</span><span class="sxs-lookup"><span data-stu-id="897fc-106">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="897fc-107">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="897fc-107">Az.AnalysisServices</span></span>
* <span data-ttu-id="897fc-108">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-108">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-109">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-110">Assemblyversion der Dienstverwaltungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-110">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="897fc-111">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="897fc-111">Az.Billing</span></span>
* <span data-ttu-id="897fc-112">Assemblyversion der Nutzungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-112">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-114">Unterstützung des PrivateEndpoint- und des PublicNetworkAccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="897fc-114">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-115">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-116">Assemblyversion der Data Factory v2-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-116">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="897fc-117">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="897fc-117">Az.DataShare</span></span>
* <span data-ttu-id="897fc-118">Allgemeine Verfügbarkeit des Moduls „Az.DataShare“</span><span class="sxs-lookup"><span data-stu-id="897fc-118">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="897fc-119">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="897fc-119">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="897fc-120">Allgemeine Verfügbarkeit des Moduls „Az.DesktopVirtualization“</span><span class="sxs-lookup"><span data-stu-id="897fc-120">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-121">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-121">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-122">SDK auf 0.21.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-122">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="897fc-123">Optionale Parameter hinzugefügt zu:</span><span class="sxs-lookup"><span data-stu-id="897fc-123">Added optional parameters to</span></span> 
    - <span data-ttu-id="897fc-124">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="897fc-124">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="897fc-125">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="897fc-125">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-126">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-126">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-127">Beispiel 3 für „Start-AzPolicyComplianceScan“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-127">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="897fc-128">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="897fc-128">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="897fc-129">Assemblyversion der PowerBI-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-129">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="897fc-130">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="897fc-130">Az.PrivateDns</span></span>
* <span data-ttu-id="897fc-131">Formatierung der ausführlichen Ausgabezeichenfolge für „Remove-AzPrivateDnsRecordSet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-131">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-132">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-132">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-133">Azure Site Recovery-Unterstützung für die Erstellung eines Wiederherstellungsplans für die Replikation zwischen Zonen per XML-Eingabe</span><span class="sxs-lookup"><span data-stu-id="897fc-133">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="897fc-134">Assemblyversion der SiteRecovery- und Backup-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-134">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-135">Az.Resources</span></span>
* <span data-ttu-id="897fc-136">Tail-Parameter zu den Cmdlets „Get-AzDeploymentScriptLog“ und „Save-AzDeploymentScriptLog“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-136">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="897fc-137">Die Output-Eigenschaft wurde formatiert und wird nun in der Ausgabe des Cmdlets „Get-AzDeploymentScript“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="897fc-137">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="897fc-138">Parameter „-DeploymentScriptInputObject“ in „-DeploymentScriptObject“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="897fc-138">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="897fc-139">Fehlender Datei-/Zielname in Cmdlet-Meldungen korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-139">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="897fc-140">Assemblyversion der Resource Manager- und Tags-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-140">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-141">Az.Sql</span></span>
* <span data-ttu-id="897fc-142">„UsePrivateLinkConnection“ zu „New-AzSqlSyncGroup“, „Update-AzSqlSyncGroup“, „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-142">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="897fc-143">„SyncMemberAzureDatabaseResourceId“ zu „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-143">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="897fc-144">Unterstützung für die Gastbenutzersuche zum SQL Server-Cmdlet für den Azure Active Directory-Administrator hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-144">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-145">Az.Storage</span></span>
* <span data-ttu-id="897fc-146">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-146">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="897fc-147">4.1.0 – Mai 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-147">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="897fc-148">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="897fc-148">Highlights since the last release</span></span>
* <span data-ttu-id="897fc-149">Unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="897fc-149">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="897fc-150">Allgemeine Verfügbarkeit von Az.Functions</span><span class="sxs-lookup"><span data-stu-id="897fc-150">General availability of Az.Functions</span></span> 
* <span data-ttu-id="897fc-151">Veröffentlichung von Hauptversionen von Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources und Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-152">Az.Accounts</span></span>
* <span data-ttu-id="897fc-153">„Add-AzEnvironment“ und „Set-AzEnvironment“ akzeptieren jetzt die Parameter „AzureSynapseAnalyticsEndpointResourceId“ und „AzureSynapseAnalyticsEndpointSuffix“.</span><span class="sxs-lookup"><span data-stu-id="897fc-153">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="897fc-154">Assemblys zu Azure.Core wurden Az.Accounts hinzugefügt. Unterstützte PowerShell-Plattformen sind u. a. Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="897fc-154">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="897fc-155">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="897fc-155">Az.Aks</span></span>
* <span data-ttu-id="897fc-156">API-Version wurde auf 2019-10-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-156">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="897fc-157">Unterstützung für die Erstellung von AKS mit einem Windows-Container</span><span class="sxs-lookup"><span data-stu-id="897fc-157">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="897fc-158">Neu verfügbare Cmdlets: „New-AzAksNodePool“, „Update-AzAksNodePool“, „Remove-AzAksNodePool“, „Get-AzAksNodePool“, „Install-AzAksKubectl“, „Get-AzAksVersion“</span><span class="sxs-lookup"><span data-stu-id="897fc-158">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-159">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-159">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-160">„New-AzApiManagement“ und „Set-AzApiManagement“: Parameter [-AssignIdentity] wurde in [-SystemAssignedIdentity] umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-160">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="897fc-161">„New-AzApiManagement“ und „Set-AzApiManagement“: Neuer Parameter hinzugefügt: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="897fc-161">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="897fc-162">„Get-AzApiManagementProperty“ wurde in „Get-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-162">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="897fc-163">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-163">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="897fc-164">„New-AzApiManagementProperty“ wurde in „New-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-164">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="897fc-165">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-165">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="897fc-166">„Set-AzApiManagementProperty“ wurde in „Set-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-166">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="897fc-167">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-167">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="897fc-168">„Remove-AzApiManagementProperty“ wurde in „Remove-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-168">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="897fc-169">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-169">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="897fc-170">Neues Cmdlet „Get-AzApiManagementAuthorizationServerClientSecret“ hinzugefügt. „Get-AzApiManagementAuthorizationServer“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-170">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="897fc-171">Neues Cmdlet „Get-AzApiManagementNamedValueSecretValue“ hinzugefügt. „Get-AzApiManagementNamedValue“ gibt keinen Geheimniswert zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-171">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="897fc-172">Neues Cmdlet „Get-AzApiManagementOpenIdConnectProviderClientSecret“ hinzugefügt. „Get-AzApiManagementOpenIdConnectProvider“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-172">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="897fc-173">Neues Cmdlet „Get-AzApiManagementSubscriptionKey“ hinzugefügt. „Get-AzApiManagementSubscription“ gibt keine Abonnementschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-173">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="897fc-174">Neues Cmdlet „Get-AzApiManagementTenantAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-174">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="897fc-175">Neues Cmdlet „Get-AzApiManagementTenantGitAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantGitAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-175">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="897fc-176">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-176">Az.ApplicationInsights</span></span>
* <span data-ttu-id="897fc-177">Parameter hinzugefügt: „RetentionInDays“, „PublicNetworkAccessForIngestion“, „PublicNetworkAccessForQuery“ für „New-AzApplicationInsights“</span><span class="sxs-lookup"><span data-stu-id="897fc-177">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="897fc-178">Cmdlet „Update-AzApplicationInsights“ erstellt.</span><span class="sxs-lookup"><span data-stu-id="897fc-178">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="897fc-179">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="897fc-179">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-180">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-180">Az.Batch</span></span>
* <span data-ttu-id="897fc-181">Az.Batch für die Verwendung der Microsoft.Azure.Batch-SDK-Version 13.0.0 und der Microsoft.Azure.Management.Batch-SDK-Version 9.0.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-181">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="897fc-182">Die Möglichkeit zum Auswählen der Art des hinzugefügten Zertifikats mithilfe des neuen Parameters „-CertificateKind“ wurde zu „New-AzBatchCertificate“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-182">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="897fc-183">Eigenschaft „ApplicationPackages“ aus „PSApplication“ entfernt, die bislang immer „“ war.</span><span class="sxs-lookup"><span data-stu-id="897fc-183">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="897fc-184">Die spezifischen Pakete in einer Anwendung können jetzt mit „Get-AzBatchApplicationPackage“ abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-184">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="897fc-185">Beispiel: „Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication“</span><span class="sxs-lookup"><span data-stu-id="897fc-185">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="897fc-186">Beim Erstellen eines Pools mit „New-AzBatchPool“ kann die Eigenschaft „VirtualMachineImageId“ von „PSImageReference“ jetzt nur auf ein Bild in einer Shared Image Gallery verweisen.</span><span class="sxs-lookup"><span data-stu-id="897fc-186">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="897fc-187">Wenn Sie einen Pool mit „New-AzBatchPool“ erstellen, kann der Pool mit der Eigenschaft „PublicIPAddressConfiguration“ von „PSNetworkConfiguration“ ohne eine öffentliche IP-Adresse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-187">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="897fc-188">Die Eigenschaft „PublicIPs“ von „PSNetworkConfiguration“ wurde ebenfalls in „PSPublicIPAddressConfiguration“ verschoben.</span><span class="sxs-lookup"><span data-stu-id="897fc-188">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="897fc-189">Diese Eigenschaft kann nur angegeben werden, wenn „IPAddressProvisioningType“ den Wert „UserManaged“ hat.</span><span class="sxs-lookup"><span data-stu-id="897fc-189">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-190">Az.Compute</span></span>
* <span data-ttu-id="897fc-191">HostId-Parameter zum Cmdlet „Update-AzVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-191">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="897fc-192">Hilfedokumente für die Cmdlets „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVmss“, „Set-AzVMOperatingSystem“ und „Set-AzVmssOsProfile“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-192">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="897fc-193">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="897fc-193">Breaking changes</span></span>
    - <span data-ttu-id="897fc-194">Der FilterExpression-Parameter wurde aus dem Cmdlet „Get-AzVMImage“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-194">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="897fc-195">Der AssignIdentity-Parameter wurde aus den Cmdlets „New-AzVmssConfig“, „New-AzVMConfig“ und „Update-AzVM“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-195">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="897fc-196">AutomaticRepairMaxInstanceRepairsPercent wurde aus den Cmdlets „New-AzVmssConfig“ und „Update-AzVmss“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-196">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="897fc-197">Die Eigenschaften AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus und VirtualMachineScaleSetsColocationStatus wurden aus ProximityPlacementGroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-197">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="897fc-198">Die Eigenschaft MaxInstanceRepairsPercent wurde aus AutomaticRepairsPolicy entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-198">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="897fc-199">Die Typen von AvailabilitySets, VirtualMachines und VirtualMachineScaleSets wurden von IList<SubResource> in IList<SubResourceWithColocationStatus> geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-199">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="897fc-200">Die Beschreibung für das Cmdlet „Get-AzVM“ wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="897fc-200">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-201">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-202">CRUD von Datenfluss-Laufzeiteigenschaften in Managed IR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-202">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-203">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-203">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-204">Neue Cmdlets zum Erstellen, Aktualisieren, Abrufen und Löschen von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-204">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="897fc-205">Hilfs-Cmdlets für die Erstellung von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-205">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="897fc-206">Regelmodulverweis auf Front Door-Routingregelobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-206">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="897fc-207">Private Link-Parameter zum Front Door-Back-End-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-207">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="897fc-208">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="897fc-208">Az.Functions</span></span>
* <span data-ttu-id="897fc-209">Allgemeine Verfügbarkeit des Moduls „Az.Functions“</span><span class="sxs-lookup"><span data-stu-id="897fc-209">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-210">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-210">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-211">Datenträgerverschlüsselung mit kundenseitig verwalteten Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-211">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="897fc-212">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="897fc-212">Az.HealthcareApis</span></span>
* <span data-ttu-id="897fc-213">Zugriffsrichtlinien verwenden nicht mehr den aktuellen Prinzipal als Standard.</span><span class="sxs-lookup"><span data-stu-id="897fc-213">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-214">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-214">Az.IotHub</span></span>
* <span data-ttu-id="897fc-215">Cmdlet zum Aufrufen einer Abfrage in einem IoT-Hub zum Abrufen von Informationen mithilfe einer SQL-ähnlichen Sprache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-215">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="897fc-216">Problem behoben, dass „Add-AzIotHubDevice“ kein Edge-aktiviertes Gerät ohne untergeordnete Geräte erstellen konnte. [#11597]</span><span class="sxs-lookup"><span data-stu-id="897fc-216">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="897fc-217">Cmdlet zum Generieren eines SAS-Tokens für IoT-Hub, -Gerät oder -Modul hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-217">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="897fc-218">Cmdlet zum Aufrufen der Konfigurationsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-218">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="897fc-219">Verwalten der automatischen skalierbaren Bereitstellung von IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="897fc-219">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="897fc-220">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-220">New cmdlets are:</span></span>
    - <span data-ttu-id="897fc-221">„Add-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-221">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="897fc-222">„Get-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-222">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="897fc-223">„Remove-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-223">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="897fc-224">„Set-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-224">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="897fc-225">Cmdlet zum Hinzufügen einer IoT Edge-Bereitstellungsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-225">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="897fc-226">Cmdlet zum Anwenden des Konfigurationsinhalts auf das angegebene Edge-Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-226">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-227">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-227">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-228">Zwei Aliase entfernt: „New-AzKeyVaultCertificateAdministratorDetails“ und „New-AzKeyVaultCertificateOrganizationDetails“</span><span class="sxs-lookup"><span data-stu-id="897fc-228">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="897fc-229">Vorläufiges Löschen ist beim Erstellen eines Schlüsseltresors standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="897fc-229">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="897fc-230">Netzwerkregeln können so festgelegt werden, dass der Zugriff von bestimmten Netzwerkstandorten beim Erstellen eines Schlüsseltresors gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-230">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="897fc-231">Unterstützung für BYOK (Bring Your Own Key) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-231">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="897fc-232">„Add-AzKeyVaultKey“ unterstützt die Erstellung eines Schlüsselaustauschschlüssels.</span><span class="sxs-lookup"><span data-stu-id="897fc-232">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="897fc-233">„Get-AzKeyVaultKey“ unterstützt das Herunterladen eines öffentlichen Schlüssels im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="897fc-233">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="897fc-234">Abschnitt „KeyOps“ der Hilfedokumentation zu „Add-AzKeyVaultKey“ wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-234">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-235">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-235">Az.Monitor</span></span>
* <span data-ttu-id="897fc-236">Fehler bei „Set-AzDiagnosticSettings“ behoben. Aufbewahrungsrichtlinie gilt nicht für alle Kategorien. [#11589]</span><span class="sxs-lookup"><span data-stu-id="897fc-236">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="897fc-237">WebTest-Verfügbarkeitskriterien für die Metrikwarnung V2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-237">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="897fc-238">„New-AzMetricAlertRuleV2Criteria“: Option zum Erstellen der Webtest-Verfügbarkeitskriterien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-238">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="897fc-239">„Add-AzMetricAlertRuleV2“: Neue Webtest-Verfügbarkeitskriterien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-239">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="897fc-240">Redundante Definition für „RetentionPolicy“ in PSLogProfile entfernt. [#7608]</span><span class="sxs-lookup"><span data-stu-id="897fc-240">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="897fc-241">Redundante in PSEventData definierte Eigenschaften entfernt. [#11353]</span><span class="sxs-lookup"><span data-stu-id="897fc-241">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="897fc-242">„Get-AzLog“ in „Get-AzActivityLog“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-242">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-243">Az.Network</span></span>
* <span data-ttu-id="897fc-244">Breaking Change-Attribut hinzugefügt als Benachrichtigung, dass sich das Standardverhalten der Zone ändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-244">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="897fc-245">„New-AzPublicIpAddress“</span><span class="sxs-lookup"><span data-stu-id="897fc-245">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="897fc-246">„New-AzPublicIpPrefix“</span><span class="sxs-lookup"><span data-stu-id="897fc-246">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="897fc-247">„New-AzLoadBalancerFrontendIpConfig“</span><span class="sxs-lookup"><span data-stu-id="897fc-247">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="897fc-248">Unterstützung für die neue Ressource der obersten Ebene SecurityPartnerProvider hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-248">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="897fc-249">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-249">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-250">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="897fc-250">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="897fc-251">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="897fc-251">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="897fc-252">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="897fc-252">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="897fc-253">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="897fc-253">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="897fc-254">„RequiredZoneNames“ für „PSPrivateLinkResource“ und „GroupId“ für „PSPrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-254">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="897fc-255">Falscher Typ des Parameters SuccessThresholdRoundTripTimeMs für New-AzNetworkWatcherConnectionMonitorTestConfigurationObject korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-255">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="897fc-256">VirtualWan-Cmdlets aktualisiert, sodass der Standardwert des Arguments AllowVnetToVnetTraffic auf True festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-256">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="897fc-257">„New-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="897fc-257">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="897fc-258">„Update-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="897fc-258">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="897fc-259">Neue Cmdlets zur Unterstützung der DNS-Zonengruppe für den privaten Endpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-259">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="897fc-260">„New-AzPrivateDnsZoneConfig“</span><span class="sxs-lookup"><span data-stu-id="897fc-260">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="897fc-261">„Get-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="897fc-261">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="897fc-262">„New-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="897fc-262">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="897fc-263">„Set-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="897fc-263">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="897fc-264">„Remove-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="897fc-264">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="897fc-265">Parameter „DNSEnableProxy“, „DNSRequireProxyForNetworkRules“ und „DNSServers“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-265">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="897fc-266">Parameter „EnableDnsProxy“, „DnsProxyNotRequiredForNetworkRule“ und „DnsServer“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-266">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="897fc-267">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-267">Updated cmdlet:</span></span>
        - <span data-ttu-id="897fc-268">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="897fc-268">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-269">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-269">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-270">Legacycode zum Anwenden des neuen generierten SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-270">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="897fc-271">Cmdlets aufgrund von veralteten APIs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="897fc-271">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="897fc-272">„Get-AzOperationalInsightsSavedSearchResult“ (alias „Get-AzOperationalInsightsSavedSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="897fc-272">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="897fc-273">„Get-AzOperationalInsightsSearchResult“ (alias „Get-AzOperationalInsightsSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="897fc-273">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="897fc-274">„Get-AzOperationalInsightsLinkTarget“ (alias „Get-AzOperationalInsightsLinkTargets“)</span><span class="sxs-lookup"><span data-stu-id="897fc-274">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="897fc-275">Parameter für „Set-AzOperationalInsightsWorkspace“ und „New-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-275">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="897fc-276">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="897fc-276">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="897fc-277">Cmdlets für Cluster und verknüpften Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="897fc-277">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-279">Azure Site Recovery: Unterstützung für den Schutz von virtuellen Computern der Näherungsplatzierungsgruppe für den Azure-zu-Azure-Anbieter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-279">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="897fc-280">Azure Site Recovery: Unterstützung für die Replikation zwischen Zonen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-280">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="897fc-281">Azure Backup: Unterstützung für die langfristige Aufbewahrung von Azure FileShare-Wiederherstellungspunkten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-281">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="897fc-282">Azure Backup: Eigenschaften für den Ausschluss von Datenträgern zur Ausgabe des Cmdlet „Get-AzRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-282">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="897fc-283">Privater Endpunkt für Tresoranmeldeinformationen für den Site Recovery-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-283">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-284">Az.Resources</span></span>
* <span data-ttu-id="897fc-285">Warnmeldung zur verzögerten Ansicht beim Erstellen einer neuen Rollendefinition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-285">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="897fc-286">Richtlinien-Cmdlets geändert, sodass sie stark typisierte Objekte ausgeben.</span><span class="sxs-lookup"><span data-stu-id="897fc-286">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="897fc-287">Parameter „-TenantLevel“ zum Cmdlet „Get-AzResourceLock“ hinzugefügt. [#11335]</span><span class="sxs-lookup"><span data-stu-id="897fc-287">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="897fc-288">„Remove-AzResourceGroup -Id ResourceId“ korrigiert. [#9882]</span><span class="sxs-lookup"><span data-stu-id="897fc-288">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="897fc-289">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Ressourcengruppenbereich hinzugefügt: „Get-AzDeploymentResourceGroupWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="897fc-289">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="897fc-290">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Abonnementbereich hinzugefügt: „Get-AzDeploymentWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="897fc-290">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="897fc-291">Alias: „Get-AzSubscriptionDeploymentWhatIf“</span><span class="sxs-lookup"><span data-stu-id="897fc-291">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="897fc-292">Parameter „-WhatIf“ und „-Confirm“ für „New-AzDeployment“ und „New-AzResourceGroupDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben.</span><span class="sxs-lookup"><span data-stu-id="897fc-292">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="897fc-293">Meldung zur Einstellung der Unterstützung für „ApiVersion“ in Bereitstellungs-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-293">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="897fc-294">Funktion zum Anzeigen verbesserter Fehlermeldungen für Bereitstellungsfehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-294">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="897fc-295">Protokollierung von correlationId bei Bereitstellungsfehlern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-295">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="897fc-296">Eigenschaft „error“ zur Bereitstellungsskriptausgabe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-296">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="897fc-297">NuGet-Microsoft.Azure.Management.ResourceManager auf „3.7.1-preview“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-297">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="897fc-298">Bestimmte Testfälle entfernt, da die Error-Eigenschaft in DeploymentValidateResult von NuGet 3.7.1-preview in schreibgeschützt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="897fc-298">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="897fc-299">GenericResourceExpanded aus dem SDK ResourceManager 3.7.1-preview importiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-299">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="897fc-300">Tagunterstützung für alle Get-Cmdlets für die Bereitstellung hinzugefügt sowie</span><span class="sxs-lookup"><span data-stu-id="897fc-300">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="897fc-301">„New-AzDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-301">'New-AzDeployment'</span></span>
    - <span data-ttu-id="897fc-302">„New-AzManagementGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-302">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="897fc-303">„New-AzResourceGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-303">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="897fc-304">„New-AzTenantDeployment“</span><span class="sxs-lookup"><span data-stu-id="897fc-304">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-306">Fehler beim Hinzufügen eines Zertifikats mithilfe von „--SecretIdentifier“ behoben, der den falschen Zertifikatfingerabdruck erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="897fc-306">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-307">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-307">Az.Sql</span></span>
* <span data-ttu-id="897fc-308">Leistungsoptimierung von:</span><span class="sxs-lookup"><span data-stu-id="897fc-308">Enhance performance of:</span></span>
    - <span data-ttu-id="897fc-309">„Set-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="897fc-309">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="897fc-310">„Set-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="897fc-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="897fc-311">„Remove-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="897fc-311">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="897fc-312">„Remove-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="897fc-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="897fc-313">„Enable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="897fc-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="897fc-314">„Enable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="897fc-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="897fc-315">„Disable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="897fc-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="897fc-316">„Disable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="897fc-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="897fc-317">Clientseitige Validierung des Parameters „RetentionDays“ aus dem Cmdlet „Set-AzSqlDatabaseBackupShortTermRetentionPolicy“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-317">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="897fc-318">Fehler beim Überwachen eines Speicherkontos in Vnet und Erstellen einer Rolle für den Mitwirkenden an Speicherblobdaten behoben.</span><span class="sxs-lookup"><span data-stu-id="897fc-318">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-319">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-319">Az.Storage</span></span>
* <span data-ttu-id="897fc-320">„-AsJob“ hinzugefügt, um das Konto für das Cmdlet „Get-AzStorageAccount“ abzurufen/aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="897fc-320">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="897fc-321">KeyVersion als optional festgelegt, wenn das Speicherkonto mit KeyvaultEncryption aktualisiert wird, um die automatische Schlüsselrotation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="897fc-321">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="897fc-322">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-322">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="897fc-323">Fehler beim Entfernen des Azure-Dateiverzeichnisses mit der Pipeline behoben.</span><span class="sxs-lookup"><span data-stu-id="897fc-323">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="897fc-324">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="897fc-324">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="897fc-325">Behoben [#9880]: Definition des DefaultAction-Werts für NetWorkRule in Übereinstimmung mit Swagger geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-325">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="897fc-326">„Update-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-326">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="897fc-327">„Get-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-327">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="897fc-328">Behoben [#11624]: Doppelte Regeln werden beim Hinzufügen von NetworkRules übersprungen, um Serverfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="897fc-328">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="897fc-329">„Add-AzStorageAccountNetworkRule“</span><span class="sxs-lookup"><span data-stu-id="897fc-329">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="897fc-330">Microsoft.Azure.Cosmos.Table SDK auf 1.0.7 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-330">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="897fc-331">Warnmeldung hinzugefügt, mit der der Benutzer darauf hingewiesen wird, eine erneute Auflistung mit ContinuationToken auszuführen, wenn nur ein Teil der Elemente in der Liste der DataLake Gen2-Elemente zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-331">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="897fc-332">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="897fc-332">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="897fc-333">Unterstützung für das Erstellen oder Aktualisieren eines Speicherkontos mit Active Directory Domain Service-Authentifizierung für Azure Files.</span><span class="sxs-lookup"><span data-stu-id="897fc-333">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="897fc-334">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-334">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="897fc-335">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-335">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="897fc-336">Unterstützung für das Hinzufügen und Auflisten von Kerberos-Schlüsseln des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="897fc-336">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="897fc-337">„New-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="897fc-337">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="897fc-338">„Get-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="897fc-338">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="897fc-339">Unterstützung für Failover für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="897fc-339">Supported failover Storage account</span></span>
    - <span data-ttu-id="897fc-340">„Invoke-AzStorageAccountFailover“</span><span class="sxs-lookup"><span data-stu-id="897fc-340">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="897fc-341">Hilfe zu „Get-AzStorageBlobCopyState“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-341">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="897fc-342">Hilfe zu „Get-AzStorageFileCopyState“ und „Start-AzStorageBlobCopy“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-342">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="897fc-343">Speicherclientbibliothek v12 in Cmdlets Queue und File integriert.</span><span class="sxs-lookup"><span data-stu-id="897fc-343">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="897fc-344">Ausgabetyp von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="897fc-344">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="897fc-345">„Get-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="897fc-345">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="897fc-346">„Remove-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="897fc-346">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="897fc-347">„Get-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="897fc-347">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="897fc-348">„Set-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="897fc-348">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="897fc-349">„Start-AzStorageFileCopy“</span><span class="sxs-lookup"><span data-stu-id="897fc-349">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="897fc-350">Ausgabetyp von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="897fc-350">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="897fc-351">„New-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="897fc-351">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="897fc-352">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="897fc-352">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="897fc-353">Ausgabetyp von CloudFileShare in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="897fc-353">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="897fc-354">„Get-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="897fc-354">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="897fc-355">„New-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="897fc-355">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="897fc-356">„Remove-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="897fc-356">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="897fc-357">Ausgabetyp von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="897fc-357">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="897fc-358">„Set-AzStorageShareQuota“</span><span class="sxs-lookup"><span data-stu-id="897fc-358">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="897fc-359">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="897fc-359">Az.TrafficManager</span></span>
* <span data-ttu-id="897fc-360">Falscher Profilname in der ausführlichen Ausgabe von „DisableAzureTrafficManagerEndpoint“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-360">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-361">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-361">Az.Websites</span></span>
* <span data-ttu-id="897fc-362">Tippfehler in der Hilfe zu „Update-AzWebAppAccessRestrictionConfig“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-362">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="897fc-363">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-363">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="897fc-364">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="897fc-364">Highlights since the last release</span></span>
* <span data-ttu-id="897fc-365">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="897fc-365">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-366">Az.Accounts</span></span>
* <span data-ttu-id="897fc-367">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="897fc-367">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-368">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-368">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-369">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-369">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="897fc-370">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-370">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-371">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-371">Az.Cdn</span></span>
* <span data-ttu-id="897fc-372">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-372">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-373">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-373">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-374">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="897fc-374">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-375">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-375">Az.Compute</span></span>
* <span data-ttu-id="897fc-376">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-376">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="897fc-377">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="897fc-377">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-378">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-378">Az.IotHub</span></span>
* <span data-ttu-id="897fc-379">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-379">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="897fc-380">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="897fc-380">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="897fc-381">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="897fc-381">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="897fc-382">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-382">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="897fc-383">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-383">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="897fc-384">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="897fc-384">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="897fc-385">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="897fc-385">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="897fc-386">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="897fc-386">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="897fc-387">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-387">New cmdlets are:</span></span>
    - <span data-ttu-id="897fc-388">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-388">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="897fc-389">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-389">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="897fc-390">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-390">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="897fc-391">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-391">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="897fc-392">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-392">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-393">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-393">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-394">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="897fc-394">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="897fc-395">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="897fc-395">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="897fc-396">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="897fc-396">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="897fc-397">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-397">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="897fc-398">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="897fc-398">Az.Maintenance</span></span>
* <span data-ttu-id="897fc-399">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-399">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-400">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-400">Az.Monitor</span></span>
* <span data-ttu-id="897fc-401">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-401">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="897fc-402">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="897fc-402">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="897fc-403">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="897fc-403">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="897fc-404">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="897fc-404">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="897fc-405">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="897fc-405">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="897fc-406">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="897fc-406">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="897fc-407">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="897fc-407">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="897fc-408">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="897fc-408">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-409">Az.Network</span></span>
* <span data-ttu-id="897fc-410">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-410">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="897fc-411">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-411">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="897fc-412">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-412">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="897fc-413">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-413">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="897fc-414">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-414">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="897fc-415">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-415">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="897fc-416">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-416">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="897fc-417">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="897fc-417">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="897fc-418">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-418">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="897fc-419">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-419">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="897fc-420">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="897fc-420">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="897fc-421">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-421">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="897fc-422">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-422">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="897fc-423">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-423">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="897fc-424">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-424">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="897fc-425">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-425">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-426">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-426">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-427">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-427">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="897fc-428">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-428">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-429">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-430">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-430">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-431">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-431">Az.Sql</span></span>
* <span data-ttu-id="897fc-432">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-432">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="897fc-433">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="897fc-433">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-434">Az.Storage</span></span>
* <span data-ttu-id="897fc-435">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-435">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="897fc-436">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="897fc-436">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="897fc-437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-437">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="897fc-438">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-438">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="897fc-439">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="897fc-439">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="897fc-440">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="897fc-440">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="897fc-441">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="897fc-441">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="897fc-442">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="897fc-442">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="897fc-443">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="897fc-443">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="897fc-444">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="897fc-444">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="897fc-445">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="897fc-445">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="897fc-446">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="897fc-446">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="897fc-447">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="897fc-447">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="897fc-448">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-448">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="897fc-449">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-449">General</span></span>
* <span data-ttu-id="897fc-450">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="897fc-450">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="897fc-451">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="897fc-451">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="897fc-452">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="897fc-452">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="897fc-453">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="897fc-453">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="897fc-454">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="897fc-454">Az.Billing</span></span>
  - <span data-ttu-id="897fc-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-455">Az.Compute</span></span>
  - <span data-ttu-id="897fc-456">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="897fc-456">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="897fc-457">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-457">Az.EventHub</span></span>
  - <span data-ttu-id="897fc-458">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-458">Az.IotHub</span></span>
  - <span data-ttu-id="897fc-459">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-459">Az.KeyVault</span></span>
  - <span data-ttu-id="897fc-460">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-460">Az.Monitor</span></span>
  - <span data-ttu-id="897fc-461">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-461">Az.Network</span></span>
  - <span data-ttu-id="897fc-462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-462">Az.Resources</span></span>
  - <span data-ttu-id="897fc-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-463">Az.Storage</span></span>
  - <span data-ttu-id="897fc-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-464">Az.Websites</span></span>
* <span data-ttu-id="897fc-465">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="897fc-465">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="897fc-466">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-466">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="897fc-467">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="897fc-467">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="897fc-468">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-468">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-469">Az.Accounts</span></span>
* <span data-ttu-id="897fc-470">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="897fc-470">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-471">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-471">Az.Compute</span></span>
* <span data-ttu-id="897fc-472">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-472">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="897fc-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="897fc-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="897fc-474">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="897fc-474">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="897fc-475">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-475">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="897fc-476">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="897fc-476">[#11354]</span></span>
* <span data-ttu-id="897fc-477">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-477">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="897fc-478">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="897fc-478">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="897fc-479">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="897fc-479">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="897fc-480">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="897fc-480">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="897fc-481">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="897fc-481">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="897fc-482">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-482">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="897fc-483">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="897fc-483">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="897fc-484">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="897fc-484">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="897fc-485">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="897fc-485">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-486">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-487">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-487">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="897fc-488">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-488">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-489">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-490">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-490">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="897fc-491">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-491">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-492">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-492">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-493">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="897fc-493">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-494">Az.IotHub</span></span>
* <span data-ttu-id="897fc-495">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-495">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="897fc-496">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-496">New Cmdlets are:</span></span>
    - <span data-ttu-id="897fc-497">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="897fc-497">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="897fc-498">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="897fc-498">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-499">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-500">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-500">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-501">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-501">Az.Monitor</span></span>
* <span data-ttu-id="897fc-502">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-502">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-503">Az.Network</span></span>
* <span data-ttu-id="897fc-504">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-504">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="897fc-505">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-505">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="897fc-506">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-506">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="897fc-507">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="897fc-507">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="897fc-508">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="897fc-508">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="897fc-509">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-509">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-510">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-510">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-511">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="897fc-511">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-512">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-513">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-513">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="897fc-514">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-514">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="897fc-515">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-515">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="897fc-516">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-516">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="897fc-517">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-517">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="897fc-518">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-518">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-519">Az.Resources</span></span>
* <span data-ttu-id="897fc-520">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="897fc-520">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="897fc-521">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-521">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="897fc-522">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="897fc-522">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="897fc-523">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-523">Added example.</span></span>
* <span data-ttu-id="897fc-524">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="897fc-524">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="897fc-525">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-525">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-526">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-526">Az.Sql</span></span>
* <span data-ttu-id="897fc-527">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-527">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="897fc-528">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-528">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="897fc-529">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="897fc-529">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="897fc-530">Az.Support</span><span class="sxs-lookup"><span data-stu-id="897fc-530">Az.Support</span></span>
* <span data-ttu-id="897fc-531">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="897fc-531">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-532">Az.Websites</span></span>
* <span data-ttu-id="897fc-533">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-533">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="897fc-534">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="897fc-534">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="897fc-535">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="897fc-535">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="897fc-536">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="897fc-536">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="897fc-537">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="897fc-537">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="897fc-538">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-538">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-539">Az.Accounts</span></span>
* <span data-ttu-id="897fc-540">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="897fc-540">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="897fc-541">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="897fc-541">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="897fc-542">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-542">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-543">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-543">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-544">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="897fc-544">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="897fc-545">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="897fc-545">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="897fc-546">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-546">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="897fc-547">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="897fc-547">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-548">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-548">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-549">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-549">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-550">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-550">Az.IotHub</span></span>
* <span data-ttu-id="897fc-551">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-551">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="897fc-552">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-552">New Cmdlets are:</span></span>
    - <span data-ttu-id="897fc-553">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-553">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-554">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-554">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-555">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-555">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-556">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-556">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="897fc-557">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-557">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="897fc-558">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-558">New Cmdlets are:</span></span>
    - <span data-ttu-id="897fc-559">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="897fc-559">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="897fc-560">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="897fc-560">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="897fc-561">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="897fc-561">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="897fc-562">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="897fc-562">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="897fc-563">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-563">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="897fc-564">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-564">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="897fc-565">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-565">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="897fc-566">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-566">New Cmdlets are:</span></span>
    - <span data-ttu-id="897fc-567">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="897fc-567">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="897fc-568">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="897fc-568">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="897fc-569">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-569">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-570">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-570">Az.Monitor</span></span>
* <span data-ttu-id="897fc-571">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="897fc-571">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-572">Az.Network</span></span>
* <span data-ttu-id="897fc-573">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-573">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="897fc-574">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="897fc-574">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="897fc-575">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="897fc-575">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="897fc-576">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-576">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-577">Az.Resources</span></span>
* <span data-ttu-id="897fc-578">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-578">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="897fc-579">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="897fc-579">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="897fc-580">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="897fc-580">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="897fc-581">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="897fc-581">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="897fc-582">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-582">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="897fc-583">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-583">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="897fc-584">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-584">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="897fc-585">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="897fc-585">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="897fc-586">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="897fc-586">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="897fc-587">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="897fc-587">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="897fc-588">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="897fc-588">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="897fc-589">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-589">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="897fc-590">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="897fc-590">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="897fc-591">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="897fc-591">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-592">Az.Sql</span></span>
* <span data-ttu-id="897fc-593">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-593">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="897fc-594">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-594">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="897fc-595">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="897fc-595">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="897fc-596">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="897fc-596">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="897fc-597">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="897fc-597">Remove an LTR backup</span></span>
    - <span data-ttu-id="897fc-598">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="897fc-598">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="897fc-599">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-599">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="897fc-600">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-600">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="897fc-601">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="897fc-601">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-602">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-602">Az.Storage</span></span>
* <span data-ttu-id="897fc-603">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-603">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="897fc-604">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="897fc-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="897fc-605">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="897fc-605">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="897fc-606">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="897fc-606">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="897fc-607">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="897fc-607">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-608">Az.Websites</span></span>
* <span data-ttu-id="897fc-609">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-609">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="897fc-610">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="897fc-610">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="897fc-611">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="897fc-611">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="897fc-612">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="897fc-612">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="897fc-613">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-613">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="897fc-614">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-614">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-615">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-615">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-616">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-616">Updated client side telemetry.</span></span>
* <span data-ttu-id="897fc-617">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-617">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="897fc-618">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-618">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-619">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-619">Az.Accounts</span></span>
* <span data-ttu-id="897fc-620">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-620">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-621">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-621">Az.Automation</span></span>
* <span data-ttu-id="897fc-622">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-622">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-623">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-623">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-624">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-624">Updated SDK to 7.0</span></span>
* <span data-ttu-id="897fc-625">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="897fc-625">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-626">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-626">Az.Compute</span></span>
* <span data-ttu-id="897fc-627">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="897fc-627">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-628">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-628">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-629">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="897fc-629">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-630">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-630">Az.IotHub</span></span>
* <span data-ttu-id="897fc-631">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-631">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="897fc-632">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-632">New Cmdlets are:</span></span>
    - <span data-ttu-id="897fc-633">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-633">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-634">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-634">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-635">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-635">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="897fc-636">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="897fc-636">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-637">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-638">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-638">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-639">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-639">Az.Monitor</span></span>
* <span data-ttu-id="897fc-640">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-640">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="897fc-641">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-641">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="897fc-642">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="897fc-642">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-643">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-643">Az.Network</span></span>
* <span data-ttu-id="897fc-644">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-644">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="897fc-645">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-645">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="897fc-646">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-646">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="897fc-647">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="897fc-647">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="897fc-648">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-648">No new cmdlets are added.</span></span> <span data-ttu-id="897fc-649">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="897fc-649">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-651">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-651">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-652">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-652">Az.Resources</span></span>
* <span data-ttu-id="897fc-653">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="897fc-653">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="897fc-654">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="897fc-654">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="897fc-655">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="897fc-655">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="897fc-656">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="897fc-656">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="897fc-657">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-657">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="897fc-658">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="897fc-658">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="897fc-659">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="897fc-659">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="897fc-660">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="897fc-660">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-661">Az.Sql</span></span>
* <span data-ttu-id="897fc-662">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-662">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="897fc-663">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-663">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="897fc-664">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="897fc-664">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="897fc-665">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="897fc-665">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="897fc-666">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-666">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="897fc-667">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="897fc-667">Az.StorageSync</span></span>
* <span data-ttu-id="897fc-668">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-668">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="897fc-669">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-669">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-670">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-670">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-671">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="897fc-671">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="897fc-672">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-672">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-673">Az.Accounts</span></span>
* <span data-ttu-id="897fc-674">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="897fc-674">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="897fc-675">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="897fc-675">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-676">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-676">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-677">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="897fc-677">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="897fc-678">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="897fc-678">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="897fc-679">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="897fc-679">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="897fc-680">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="897fc-680">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-681">Az.Compute</span></span>
* <span data-ttu-id="897fc-682">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="897fc-682">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="897fc-683">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-683">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="897fc-684">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-684">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="897fc-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="897fc-686">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-686">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-687">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-688">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-688">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="897fc-689">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="897fc-689">Az.DeploymentManager</span></span>
* <span data-ttu-id="897fc-690">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-690">Adds LIST operations for resources</span></span>
* <span data-ttu-id="897fc-691">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-691">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-692">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-692">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-693">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-693">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-694">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-694">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-695">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="897fc-695">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-696">Az.Network</span></span>
* <span data-ttu-id="897fc-697">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="897fc-697">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="897fc-698">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="897fc-698">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="897fc-699">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="897fc-699">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="897fc-700">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="897fc-700">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="897fc-701">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="897fc-701">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="897fc-702">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="897fc-702">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="897fc-703">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="897fc-703">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="897fc-704">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-704">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="897fc-705">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-705">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="897fc-707">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-707">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="897fc-708">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="897fc-708">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="897fc-709">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-709">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-710">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-710">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-711">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="897fc-711">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="897fc-712">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-712">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="897fc-713">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-713">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="897fc-714">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-714">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-715">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-715">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-716">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="897fc-716">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="897fc-717">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-717">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-718">Az.Resources</span></span>
* <span data-ttu-id="897fc-719">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="897fc-719">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="897fc-720">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-720">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-721">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-721">Az.Sql</span></span>
<span data-ttu-id="897fc-722">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="897fc-722">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-723">Az.Storage</span></span>
* <span data-ttu-id="897fc-724">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="897fc-724">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="897fc-725">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-725">New-AzStorageAccount</span></span>
* <span data-ttu-id="897fc-726">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="897fc-726">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="897fc-727">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-727">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-728">Az.Websites</span></span>
* <span data-ttu-id="897fc-729">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="897fc-729">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="897fc-730">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="897fc-730">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="897fc-731">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="897fc-731">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-732">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-732">Az.Accounts</span></span>
* <span data-ttu-id="897fc-733">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="897fc-733">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-734">Az.Cdn</span></span>
* <span data-ttu-id="897fc-735">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="897fc-735">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-736">Az.Compute</span></span>
* <span data-ttu-id="897fc-737">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-737">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="897fc-738">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-738">Az.ContainerInstance</span></span>
* <span data-ttu-id="897fc-739">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-739">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="897fc-740">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="897fc-740">Az.DataBoxEdge</span></span>
* <span data-ttu-id="897fc-741">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-741">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="897fc-742">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-742">Get the Edge Storage Container</span></span>
* <span data-ttu-id="897fc-743">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-743">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="897fc-744">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="897fc-744">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="897fc-745">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-745">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="897fc-746">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="897fc-746">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="897fc-747">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-747">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="897fc-748">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-748">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="897fc-749">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-749">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="897fc-750">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-750">Get the Edge Storage Account</span></span>
* <span data-ttu-id="897fc-751">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-751">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="897fc-752">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="897fc-752">Create new Edge Storage Account</span></span>
* <span data-ttu-id="897fc-753">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-753">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="897fc-754">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="897fc-754">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="897fc-755">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-755">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="897fc-756">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-756">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="897fc-757">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-757">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="897fc-758">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="897fc-758">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-759">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-760">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-760">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="897fc-761">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-761">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="897fc-762">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="897fc-762">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="897fc-763">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="897fc-763">Az.DevTestLabs</span></span>
* <span data-ttu-id="897fc-764">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-764">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-765">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-765">Az.EventHub</span></span>
* <span data-ttu-id="897fc-766">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-766">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-767">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-767">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-768">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-768">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="897fc-769">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="897fc-769">Az.MachineLearning</span></span>
* <span data-ttu-id="897fc-770">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="897fc-770">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="897fc-771">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="897fc-771">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="897fc-772">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="897fc-772">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="897fc-773">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="897fc-773">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="897fc-774">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="897fc-774">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="897fc-775">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="897fc-775">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="897fc-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="897fc-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="897fc-777">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="897fc-777">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-778">Az.Network</span></span>
* <span data-ttu-id="897fc-779">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="897fc-779">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-780">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-780">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-781">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="897fc-781">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="897fc-782">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="897fc-782">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="897fc-783">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="897fc-783">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="897fc-784">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="897fc-784">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-785">Az.Resources</span></span>
* <span data-ttu-id="897fc-786">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-786">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-787">Az.Sql</span></span>
* <span data-ttu-id="897fc-788">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="897fc-788">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="897fc-789">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-789">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="897fc-790">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="897fc-790">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="897fc-791">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-791">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-792">Az.Storage</span></span>
* <span data-ttu-id="897fc-793">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="897fc-793">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="897fc-794">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-794">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="897fc-795">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="897fc-795">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="897fc-796">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-796">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="897fc-797">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-797">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="897fc-798">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-798">General</span></span>
* <span data-ttu-id="897fc-799">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-799">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-800">Az.Accounts</span></span>
* <span data-ttu-id="897fc-801">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="897fc-801">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="897fc-802">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="897fc-802">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-803">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-803">Az.Batch</span></span>
* <span data-ttu-id="897fc-804">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-804">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-805">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-806">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-806">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-807">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-808">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-808">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="897fc-809">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-809">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="897fc-810">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="897fc-810">Az.HealthcareApis</span></span>
* <span data-ttu-id="897fc-811">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="897fc-811">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-812">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-812">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-813">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-813">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="897fc-814">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="897fc-814">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="897fc-815">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-815">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-816">Az.Monitor</span></span>
* <span data-ttu-id="897fc-817">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-817">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="897fc-818">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="897fc-818">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="897fc-819">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="897fc-819">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-820">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-820">Az.Network</span></span>
* <span data-ttu-id="897fc-821">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="897fc-821">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-822">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-822">Az.Resources</span></span>
* <span data-ttu-id="897fc-823">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="897fc-823">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="897fc-824">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="897fc-824">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-825">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-825">Az.Sql</span></span>
* <span data-ttu-id="897fc-826">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-826">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-827">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-827">Az.Storage</span></span>
* <span data-ttu-id="897fc-828">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="897fc-828">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="897fc-829">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="897fc-829">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="897fc-830">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="897fc-830">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="897fc-831">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="897fc-831">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="897fc-832">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="897fc-832">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="897fc-833">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="897fc-833">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="897fc-834">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-834">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="897fc-835">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-835">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="897fc-836">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-836">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="897fc-837">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-837">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="897fc-838">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="897fc-838">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="897fc-839">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="897fc-839">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="897fc-840">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="897fc-840">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="897fc-841">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-841">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-842">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-842">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-843">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="897fc-843">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="897fc-844">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="897fc-844">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-845">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-845">Az.Compute</span></span>
* <span data-ttu-id="897fc-846">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="897fc-846">VM Reapply feature</span></span>
    - <span data-ttu-id="897fc-847">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-847">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="897fc-848">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="897fc-848">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="897fc-849">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="897fc-849">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="897fc-850">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="897fc-850">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="897fc-851">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-851">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="897fc-852">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-852">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="897fc-853">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-853">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="897fc-854">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-854">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="897fc-855">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-855">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="897fc-856">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-856">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="897fc-857">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="897fc-857">Az.DataBoxEdge</span></span>
* <span data-ttu-id="897fc-858">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-858">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="897fc-859">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="897fc-859">Get the Order</span></span>
* <span data-ttu-id="897fc-860">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-860">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="897fc-861">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="897fc-861">Create new Order</span></span>
* <span data-ttu-id="897fc-862">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-862">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="897fc-863">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="897fc-863">Remove the Order</span></span>
* <span data-ttu-id="897fc-864">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="897fc-864">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="897fc-865">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="897fc-865">Now creates Local Share</span></span>
* <span data-ttu-id="897fc-866">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-866">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="897fc-867">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-867">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="897fc-868">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-868">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="897fc-869">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="897fc-869">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="897fc-870">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-870">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="897fc-871">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="897fc-871">Gets the information about Triggers</span></span>
* <span data-ttu-id="897fc-872">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-872">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="897fc-873">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="897fc-873">Create new Triggers</span></span>
* <span data-ttu-id="897fc-874">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-874">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="897fc-875">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="897fc-875">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-876">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-876">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-877">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-877">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="897fc-878">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="897fc-878">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-879">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-879">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-880">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-880">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-881">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-881">Az.EventHub</span></span>
* <span data-ttu-id="897fc-882">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-882">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-883">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-883">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-884">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-884">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="897fc-885">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-885">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="897fc-886">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-886">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="897fc-887">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="897fc-887">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-888">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-888">Az.Network</span></span>
* <span data-ttu-id="897fc-889">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-889">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="897fc-890">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="897fc-890">Az.PrivateDns</span></span>
* <span data-ttu-id="897fc-891">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-891">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-892">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-892">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-893">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="897fc-893">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="897fc-894">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="897fc-894">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="897fc-895">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="897fc-895">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="897fc-896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="897fc-896">Az.RedisCache</span></span>
* <span data-ttu-id="897fc-897">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-897">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="897fc-898">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-898">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="897fc-899">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-899">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-900">Az.Resources</span></span>
- <span data-ttu-id="897fc-901">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="897fc-901">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="897fc-902">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-902">Updated create policy definition help example</span></span>
- <span data-ttu-id="897fc-903">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-903">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="897fc-904">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="897fc-904">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="897fc-905">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="897fc-905">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-906">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-906">Az.Sql</span></span>
* <span data-ttu-id="897fc-907">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-907">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="897fc-908">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="897fc-908">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="897fc-909">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-909">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="897fc-910">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-910">General</span></span>
* <span data-ttu-id="897fc-911">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="897fc-911">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-912">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-912">Az.Accounts</span></span>
* <span data-ttu-id="897fc-913">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-913">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="897fc-914">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="897fc-914">Az.Advisor</span></span>
* <span data-ttu-id="897fc-915">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-915">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-916">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-916">Az.Batch</span></span>
* <span data-ttu-id="897fc-917">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-917">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="897fc-918">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-918">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="897fc-919">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="897fc-919">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="897fc-920">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-920">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="897fc-921">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="897fc-921">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="897fc-922">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-922">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="897fc-923">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="897fc-923">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="897fc-924">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="897fc-924">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="897fc-925">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="897fc-925">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="897fc-926">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-926">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="897fc-927">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-927">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="897fc-928">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="897fc-928">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="897fc-929">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-929">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="897fc-930">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="897fc-930">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="897fc-931">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-931">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="897fc-932">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-932">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="897fc-933">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-933">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="897fc-934">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-934">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="897fc-935">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-935">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="897fc-936">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-936">This operation is no longer supported.</span></span>
* <span data-ttu-id="897fc-937">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-937">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="897fc-938">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-938">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="897fc-939">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-939">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="897fc-940">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="897fc-940">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="897fc-941">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="897fc-941">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="897fc-942">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="897fc-942">New non-verified images are also now returned.</span></span> <span data-ttu-id="897fc-943">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="897fc-943">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="897fc-944">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-944">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="897fc-945">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="897fc-945">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="897fc-946">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="897fc-946">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="897fc-947">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="897fc-947">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="897fc-948">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="897fc-948">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="897fc-949">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-949">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="897fc-950">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="897fc-950">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="897fc-951">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="897fc-951">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="897fc-952">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="897fc-952">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-953">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-953">Az.Cdn</span></span>
* <span data-ttu-id="897fc-954">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="897fc-954">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="897fc-955">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="897fc-955">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-956">Az.Compute</span></span>
* <span data-ttu-id="897fc-957">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="897fc-957">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="897fc-958">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="897fc-958">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="897fc-959">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="897fc-959">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="897fc-960">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-960">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="897fc-961">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-961">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="897fc-962">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="897fc-962">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="897fc-963">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-963">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="897fc-964">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="897fc-964">Breaking changes</span></span>
    - <span data-ttu-id="897fc-965">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="897fc-965">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="897fc-966">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="897fc-966">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-967">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-967">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-968">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-968">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-969">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-969">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-970">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="897fc-970">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="897fc-971">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="897fc-971">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="897fc-972">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="897fc-972">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="897fc-973">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="897fc-973">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="897fc-974">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="897fc-974">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="897fc-975">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="897fc-975">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-976">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-976">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-977">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-977">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-978">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-978">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-979">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="897fc-979">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="897fc-980">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="897fc-980">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="897fc-981">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-981">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="897fc-982">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="897fc-982">Removed five cmdlets:</span></span>
    - <span data-ttu-id="897fc-983">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="897fc-983">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="897fc-984">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="897fc-984">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="897fc-985">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="897fc-985">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="897fc-986">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="897fc-986">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="897fc-987">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="897fc-987">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="897fc-988">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-988">Added three cmdlets:</span></span>
    - <span data-ttu-id="897fc-989">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="897fc-989">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="897fc-990">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="897fc-990">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="897fc-991">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="897fc-991">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="897fc-992">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="897fc-992">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="897fc-993">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-993">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="897fc-994">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-994">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="897fc-995">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="897fc-995">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="897fc-996">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-996">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="897fc-997">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-997">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="897fc-998">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-998">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="897fc-999">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-999">Added some scenario test cases.</span></span>
* <span data-ttu-id="897fc-1000">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="897fc-1000">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1001">Az.IotHub</span></span>
* <span data-ttu-id="897fc-1002">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="897fc-1002">Breaking changes:</span></span>
    - <span data-ttu-id="897fc-1003">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1003">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="897fc-1004">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1004">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="897fc-1005">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1005">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="897fc-1006">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1006">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="897fc-1007">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1007">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="897fc-1008">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1008">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="897fc-1009">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="897fc-1009">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="897fc-1010">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="897fc-1010">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="897fc-1011">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1011">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="897fc-1012">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1012">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="897fc-1013">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1013">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="897fc-1014">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1014">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1015">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1015">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1016">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1016">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1017">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1017">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="897fc-1018">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1018">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="897fc-1019">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1019">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1020">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1020">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1021">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1021">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1022">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1022">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1023">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1023">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1024">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1024">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1025">Az.Resources</span></span>
* <span data-ttu-id="897fc-1026">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1026">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1027">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1027">Az.Network</span></span>
* <span data-ttu-id="897fc-1028">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1028">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="897fc-1029">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-1029">Updated cmdlet:</span></span>
        - <span data-ttu-id="897fc-1030">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1030">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1031">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1031">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1032">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1032">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1033">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1033">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1034">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1034">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="897fc-1035">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="897fc-1035">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="897fc-1036">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-1036">New cmdlet:</span></span>
        - <span data-ttu-id="897fc-1037">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="897fc-1037">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="897fc-1038">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1038">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="897fc-1039">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1039">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="897fc-1040">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1040">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="897fc-1041">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1041">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="897fc-1042">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1042">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="897fc-1043">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1043">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="897fc-1044">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1044">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="897fc-1045">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1045">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-1046">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="897fc-1046">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="897fc-1047">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-1047">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="897fc-1048">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-1048">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="897fc-1049">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-1049">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="897fc-1050">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1050">Set-AzVirtualHub</span></span>
* <span data-ttu-id="897fc-1051">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1051">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="897fc-1052">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1052">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="897fc-1053">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1053">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="897fc-1054">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1054">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="897fc-1055">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1055">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="897fc-1056">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1056">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="897fc-1057">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1057">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="897fc-1058">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1058">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-1059">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1059">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="897fc-1060">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1060">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="897fc-1061">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1061">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="897fc-1062">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1062">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="897fc-1063">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1063">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="897fc-1064">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1064">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="897fc-1065">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1065">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="897fc-1066">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1066">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="897fc-1067">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1067">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-1068">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="897fc-1068">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="897fc-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="897fc-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="897fc-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="897fc-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="897fc-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="897fc-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="897fc-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="897fc-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="897fc-1074">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1074">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="897fc-1075">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1075">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="897fc-1076">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1076">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="897fc-1077">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1077">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="897fc-1078">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1078">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="897fc-1079">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1079">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="897fc-1080">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1080">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="897fc-1081">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1081">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="897fc-1082">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="897fc-1082">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="897fc-1083">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1083">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="897fc-1084">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1084">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="897fc-1085">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1085">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-1086">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1086">New-AzIpGroup</span></span>
        - <span data-ttu-id="897fc-1087">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1087">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="897fc-1088">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1088">Get-AzIpGroup</span></span>
        - <span data-ttu-id="897fc-1089">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1089">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-1090">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1090">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-1091">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="897fc-1091">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1092">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1092">Az.Sql</span></span>
* <span data-ttu-id="897fc-1093">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1093">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="897fc-1094">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1094">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="897fc-1095">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="897fc-1095">Removed deprecated aliases:</span></span>
* <span data-ttu-id="897fc-1096">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="897fc-1096">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="897fc-1097">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="897fc-1097">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="897fc-1098">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1098">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="897fc-1099">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1099">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="897fc-1100">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="897fc-1100">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="897fc-1101">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1101">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1102">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1102">Az.Storage</span></span>
* <span data-ttu-id="897fc-1103">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1103">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="897fc-1104">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1104">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="897fc-1105">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1105">Set-AzStorageAccount</span></span>
* <span data-ttu-id="897fc-1106">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1106">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="897fc-1107">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="897fc-1107">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="897fc-1108">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="897fc-1108">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="897fc-1109">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1109">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="897fc-1110">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-1110">General</span></span>
* <span data-ttu-id="897fc-1111">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="897fc-1111">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-1112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1112">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1113">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1113">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-1114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-1114">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-1115">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1115">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="897fc-1116">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="897fc-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1117">Az.Automation</span></span>
* <span data-ttu-id="897fc-1118">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1118">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-1119">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-1119">Az.Batch</span></span>
* <span data-ttu-id="897fc-1120">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1120">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1121">Az.Compute</span></span>
* <span data-ttu-id="897fc-1122">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1122">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="897fc-1123">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1123">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="897fc-1124">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1124">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="897fc-1125">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="897fc-1125">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1126">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1126">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1127">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="897fc-1127">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="897fc-1128">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="897fc-1128">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="897fc-1129">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1129">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-1130">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-1130">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-1131">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="897fc-1131">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="897fc-1132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="897fc-1132">Az.HealthcareApis</span></span>
* <span data-ttu-id="897fc-1133">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1133">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="897fc-1134">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1134">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="897fc-1135">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="897fc-1135">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="897fc-1136">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1136">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-1137">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1137">Az.IotHub</span></span>
* <span data-ttu-id="897fc-1138">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="897fc-1138">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="897fc-1139">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="897fc-1139">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1140">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1140">Az.Monitor</span></span>
* <span data-ttu-id="897fc-1141">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="897fc-1141">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="897fc-1142">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1142">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="897fc-1143">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="897fc-1143">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="897fc-1144">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="897fc-1144">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1145">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1145">Az.Network</span></span>
* <span data-ttu-id="897fc-1146">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="897fc-1146">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="897fc-1147">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1147">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="897fc-1148">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1148">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-1149">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-1149">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="897fc-1150">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1150">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="897fc-1151">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1151">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="897fc-1152">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1152">Updated cmdlets:</span></span>
        - <span data-ttu-id="897fc-1153">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1153">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="897fc-1154">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1154">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="897fc-1155">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1155">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="897fc-1156">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1156">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="897fc-1157">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="897fc-1157">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="897fc-1158">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="897fc-1158">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="897fc-1159">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="897fc-1159">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="897fc-1160">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="897fc-1160">Az.RedisCache</span></span>
* <span data-ttu-id="897fc-1161">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="897fc-1161">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1162">Az.Sql</span></span>
* <span data-ttu-id="897fc-1163">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1163">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1164">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1164">Az.Storage</span></span>
* <span data-ttu-id="897fc-1165">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1165">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="897fc-1166">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="897fc-1166">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="897fc-1167">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="897fc-1167">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="897fc-1168">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="897fc-1168">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="897fc-1169">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1169">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="897fc-1170">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="897fc-1170">Az.StorageSync</span></span>
* <span data-ttu-id="897fc-1171">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1171">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1172">Az.Websites</span></span>
* <span data-ttu-id="897fc-1173">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="897fc-1173">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="897fc-1174">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1174">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="897fc-1175">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-1175">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-1176">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1176">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="897fc-1177">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1177">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="897fc-1178">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="897fc-1178">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1179">Az.Automation</span></span>
* <span data-ttu-id="897fc-1180">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1180">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="897fc-1181">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1181">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="897fc-1182">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1182">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1183">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1183">Az.Compute</span></span>
* <span data-ttu-id="897fc-1184">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1184">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="897fc-1185">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1185">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="897fc-1186">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-1186">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="897fc-1187">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1187">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="897fc-1188">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1188">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="897fc-1189">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="897fc-1189">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="897fc-1190">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1190">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="897fc-1191">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1191">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="897fc-1192">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1192">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1193">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1193">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1194">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="897fc-1194">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="897fc-1195">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1195">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-1196">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-1196">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-1197">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1197">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-1198">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1198">Az.IotHub</span></span>
* <span data-ttu-id="897fc-1199">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1199">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="897fc-1200">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1200">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="897fc-1201">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="897fc-1201">New cmdlets are:</span></span>
    - <span data-ttu-id="897fc-1202">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="897fc-1202">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="897fc-1203">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="897fc-1203">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="897fc-1204">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="897fc-1204">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="897fc-1205">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="897fc-1205">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1206">Az.Monitor</span></span>
* <span data-ttu-id="897fc-1207">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="897fc-1207">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="897fc-1208">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="897fc-1208">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="897fc-1209">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="897fc-1209">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="897fc-1210">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="897fc-1210">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="897fc-1211">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1211">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="897fc-1212">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="897fc-1212">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="897fc-1213">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1213">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="897fc-1214">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="897fc-1214">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="897fc-1215">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1215">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="897fc-1216">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="897fc-1216">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="897fc-1217">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-1217">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="897fc-1218">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="897fc-1218">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="897fc-1219">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="897fc-1219">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="897fc-1220">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="897fc-1220">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="897fc-1221">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="897fc-1221">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="897fc-1222">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="897fc-1222">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="897fc-1223">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="897fc-1223">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="897fc-1224">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1224">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="897fc-1225">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1225">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="897fc-1226">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-1226">Overall improved help files</span></span>
* <span data-ttu-id="897fc-1227">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1227">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1228">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1228">Az.Network</span></span>
* <span data-ttu-id="897fc-1229">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1229">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="897fc-1230">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1230">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="897fc-1231">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="897fc-1231">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="897fc-1232">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="897fc-1232">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="897fc-1233">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="897fc-1233">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="897fc-1234">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1234">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="897fc-1235">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1235">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="897fc-1236">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1236">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="897fc-1237">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1237">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="897fc-1238">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1238">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="897fc-1239">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1239">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="897fc-1240">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="897fc-1240">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="897fc-1241">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1241">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1242">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="897fc-1242">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="897fc-1243">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1243">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="897fc-1244">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-1244">Updated cmdlet:</span></span>
        - <span data-ttu-id="897fc-1245">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="897fc-1245">New-VpnSite</span></span>
        - <span data-ttu-id="897fc-1246">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="897fc-1246">Update-VpnSite</span></span>
        - <span data-ttu-id="897fc-1247">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1247">New-VpnConnection</span></span>
        - <span data-ttu-id="897fc-1248">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1248">Update-VpnConnection</span></span>
* <span data-ttu-id="897fc-1249">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="897fc-1249">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1250">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1251">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1251">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="897fc-1252">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1252">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1253">Az.Resources</span></span>
* <span data-ttu-id="897fc-1254">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="897fc-1254">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-1255">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1255">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-1256">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1256">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="897fc-1257">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-1257">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="897fc-1258">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="897fc-1258">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="897fc-1259">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="897fc-1259">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="897fc-1260">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="897fc-1260">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="897fc-1261">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="897fc-1261">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="897fc-1262">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="897fc-1262">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="897fc-1263">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="897fc-1263">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="897fc-1264">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="897fc-1264">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="897fc-1265">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="897fc-1265">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="897fc-1266">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="897fc-1266">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="897fc-1267">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="897fc-1267">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="897fc-1268">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="897fc-1268">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="897fc-1269">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="897fc-1269">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="897fc-1270">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="897fc-1270">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="897fc-1271">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="897fc-1271">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="897fc-1272">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="897fc-1272">Az.SignalR</span></span>
* <span data-ttu-id="897fc-1273">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1273">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1274">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1274">Az.Sql</span></span>
* <span data-ttu-id="897fc-1275">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1275">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="897fc-1276">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="897fc-1276">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="897fc-1277">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="897fc-1277">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="897fc-1278">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-1278">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="897fc-1279">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="897fc-1279">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1280">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1280">Az.Storage</span></span>
* <span data-ttu-id="897fc-1281">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1281">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="897fc-1282">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1282">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="897fc-1283">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="897fc-1283">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="897fc-1284">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="897fc-1284">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="897fc-1285">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1285">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="897fc-1286">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="897fc-1286">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="897fc-1287">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="897fc-1287">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="897fc-1288">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-1288">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="897fc-1289">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-1289">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="897fc-1290">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-1290">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="897fc-1291">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="897fc-1291">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1292">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1292">Az.Websites</span></span>
* <span data-ttu-id="897fc-1293">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="897fc-1293">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="897fc-1294">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1294">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="897fc-1295">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1295">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="897fc-1296">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1296">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="897fc-1297">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-1297">General</span></span>
* <span data-ttu-id="897fc-1298">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1298">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-1299">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1299">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1300">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="897fc-1300">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="897fc-1301">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="897fc-1301">Az.Aks</span></span>
* <span data-ttu-id="897fc-1302">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1302">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="897fc-1303">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="897fc-1303">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-1304">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-1304">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-1305">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="897fc-1305">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="897fc-1306">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="897fc-1306">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="897fc-1307">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1307">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="897fc-1308">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="897fc-1308">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="897fc-1309">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="897fc-1309">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-1310">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-1310">Az.Batch</span></span>
* <span data-ttu-id="897fc-1311">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="897fc-1311">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-1312">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-1312">Az.Cdn</span></span>
* <span data-ttu-id="897fc-1313">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1313">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1314">Az.Compute</span></span>
* <span data-ttu-id="897fc-1315">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1315">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="897fc-1316">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1316">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="897fc-1317">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1317">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="897fc-1318">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1318">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="897fc-1319">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="897fc-1319">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="897fc-1320">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1320">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="897fc-1321">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1321">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="897fc-1322">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1322">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1323">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1324">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="897fc-1324">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="897fc-1325">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1325">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="897fc-1326">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-1326">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="897fc-1327">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1327">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-1328">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-1328">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-1329">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1329">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-1330">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1330">Az.EventHub</span></span>
* <span data-ttu-id="897fc-1331">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-1331">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="897fc-1332">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="897fc-1332">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="897fc-1333">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1333">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="897fc-1334">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1334">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="897fc-1335">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="897fc-1335">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="897fc-1336">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1336">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1337">Az.Monitor</span></span>
* <span data-ttu-id="897fc-1338">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1338">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1339">Az.Network</span></span>
* <span data-ttu-id="897fc-1340">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1340">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="897fc-1341">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-1341">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="897fc-1342">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="897fc-1342">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="897fc-1343">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1343">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="897fc-1344">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1344">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="897fc-1345">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1345">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="897fc-1346">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="897fc-1346">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-1347">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1347">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-1348">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="897fc-1348">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="897fc-1349">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1349">Added example</span></span>
    - <span data-ttu-id="897fc-1350">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1350">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="897fc-1351">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1351">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="897fc-1352">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1352">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1353">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1354">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1354">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1355">Az.Resources</span></span>
* <span data-ttu-id="897fc-1356">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1356">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="897fc-1357">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1357">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="897fc-1358">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="897fc-1358">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="897fc-1359">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1359">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-1360">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-1360">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-1361">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-1361">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="897fc-1362">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1362">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="897fc-1363">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1363">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-1364">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1364">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-1365">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="897fc-1365">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="897fc-1366">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="897fc-1366">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="897fc-1367">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="897fc-1367">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="897fc-1368">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="897fc-1368">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="897fc-1369">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="897fc-1369">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="897fc-1370">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="897fc-1370">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1371">Az.Sql</span></span>
* <span data-ttu-id="897fc-1372">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1372">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1373">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1373">Az.Storage</span></span>
* <span data-ttu-id="897fc-1374">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="897fc-1374">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="897fc-1375">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="897fc-1375">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="897fc-1376">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="897fc-1376">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="897fc-1377">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="897fc-1377">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="897fc-1378">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="897fc-1378">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="897fc-1379">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="897fc-1379">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1380">Az.Websites</span></span>
* <span data-ttu-id="897fc-1381">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="897fc-1381">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="897fc-1382">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1382">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-1383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1383">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1384">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1384">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="897fc-1385">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1385">Az.ApplicationInsights</span></span>
* <span data-ttu-id="897fc-1386">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1386">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1387">Az.Automation</span></span>
* <span data-ttu-id="897fc-1388">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1388">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-1389">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1389">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-1390">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1390">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1391">Az.Compute</span></span>
* <span data-ttu-id="897fc-1392">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1392">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="897fc-1393">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="897fc-1393">Az.ContainerRegistry</span></span>
* <span data-ttu-id="897fc-1394">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1394">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="897fc-1395">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="897fc-1395">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1396">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1396">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1397">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1397">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="897fc-1398">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1398">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-1399">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1399">Az.EventHub</span></span>
* <span data-ttu-id="897fc-1400">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="897fc-1400">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="897fc-1401">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1401">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-1402">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-1402">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-1403">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1403">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="897fc-1404">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="897fc-1404">Az.LogicApp</span></span>
* <span data-ttu-id="897fc-1405">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="897fc-1405">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="897fc-1406">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1406">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="897fc-1407">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1407">Az.ManagedServices</span></span>
* <span data-ttu-id="897fc-1408">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1408">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1409">Az.Network</span></span>
* <span data-ttu-id="897fc-1410">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1410">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="897fc-1411">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1411">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1412">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="897fc-1412">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="897fc-1413">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="897fc-1413">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="897fc-1414">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1414">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1415">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1415">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1416">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1416">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1417">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1417">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="897fc-1418">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="897fc-1418">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="897fc-1419">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="897fc-1419">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="897fc-1420">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="897fc-1420">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="897fc-1421">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1421">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="897fc-1422">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="897fc-1422">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="897fc-1423">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="897fc-1423">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="897fc-1424">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1424">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="897fc-1425">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="897fc-1425">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="897fc-1426">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1426">Updated cmdlets</span></span>
        - <span data-ttu-id="897fc-1427">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1427">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="897fc-1428">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1428">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="897fc-1429">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1429">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="897fc-1430">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1430">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="897fc-1431">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1431">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="897fc-1432">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-1432">Updated cmdlet:</span></span>
        - <span data-ttu-id="897fc-1433">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1433">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="897fc-1434">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1434">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="897fc-1435">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1435">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="897fc-1436">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1436">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="897fc-1437">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-1437">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="897fc-1438">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="897fc-1438">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-1439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1439">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-1440">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1440">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="897fc-1441">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1441">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1442">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1442">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1443">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1443">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="897fc-1444">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1444">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="897fc-1445">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1445">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="897fc-1446">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1446">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="897fc-1447">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1447">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="897fc-1448">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1448">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="897fc-1449">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1449">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="897fc-1450">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1450">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="897fc-1451">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1451">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="897fc-1452">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1452">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1453">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1453">Az.Resources</span></span>
- <span data-ttu-id="897fc-1454">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1454">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="897fc-1455">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1455">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-1456">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-1456">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-1457">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="897fc-1457">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="897fc-1458">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1458">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1459">Az.Sql</span></span>
* <span data-ttu-id="897fc-1460">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1460">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="897fc-1461">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1461">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="897fc-1462">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1462">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1463">Az.Storage</span></span>
* <span data-ttu-id="897fc-1464">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1464">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="897fc-1465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="897fc-1465">Az.StorageSync</span></span>
* <span data-ttu-id="897fc-1466">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1466">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="897fc-1467">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1467">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1468">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1468">Az.Websites</span></span>
* <span data-ttu-id="897fc-1469">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="897fc-1469">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="897fc-1470">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1470">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="897fc-1471">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1471">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="897fc-1472">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1472">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-1473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1473">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1474">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1474">Add support for profile cmdlets</span></span>
* <span data-ttu-id="897fc-1475">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1475">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="897fc-1476">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-1476">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="897fc-1477">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="897fc-1477">Az.Advisor</span></span>
* <span data-ttu-id="897fc-1478">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="897fc-1478">GA release of Az.Advisor</span></span>
* <span data-ttu-id="897fc-1479">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="897fc-1479">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="897fc-1480">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-1480">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-1481">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="897fc-1481">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="897fc-1482">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="897fc-1482">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="897fc-1483">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1483">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="897fc-1484">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="897fc-1484">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="897fc-1485">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="897fc-1485">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="897fc-1486">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="897fc-1486">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="897fc-1487">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1487">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1488">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1488">Az.Automation</span></span>
* <span data-ttu-id="897fc-1489">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1489">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1490">Az.Compute</span></span>
* <span data-ttu-id="897fc-1491">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1491">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1492">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1493">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="897fc-1493">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="897fc-1494">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="897fc-1494">Az.EventGrid</span></span>
* <span data-ttu-id="897fc-1495">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1495">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-1496">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1496">Az.IotHub</span></span>
* <span data-ttu-id="897fc-1497">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1497">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1498">Az.Network</span></span>
* <span data-ttu-id="897fc-1499">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1499">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="897fc-1500">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-1500">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-1501">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1501">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-1502">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="897fc-1502">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="897fc-1503">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="897fc-1503">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-1504">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1504">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-1505">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1505">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1506">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1507">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="897fc-1507">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1508">Az.Resources</span></span>
    - <span data-ttu-id="897fc-1509">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1509">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="897fc-1510">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1510">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="897fc-1511">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1511">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="897fc-1512">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1512">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-1513">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-1513">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-1514">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="897fc-1514">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1515">Az.Sql</span></span>
* <span data-ttu-id="897fc-1516">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1516">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="897fc-1517">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1517">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="897fc-1518">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1518">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="897fc-1519">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1519">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="897fc-1520">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1520">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="897fc-1521">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1521">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="897fc-1522">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1522">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="897fc-1523">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="897fc-1523">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="897fc-1524">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-1524">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1525">Az.Storage</span></span>
* <span data-ttu-id="897fc-1526">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="897fc-1526">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="897fc-1527">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="897fc-1527">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="897fc-1528">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="897fc-1528">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="897fc-1529">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="897fc-1529">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="897fc-1530">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="897fc-1530">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="897fc-1531">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1531">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="897fc-1532">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1532">Set-AzStorageAccount</span></span>
* <span data-ttu-id="897fc-1533">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="897fc-1533">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="897fc-1534">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="897fc-1534">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="897fc-1535">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="897fc-1535">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="897fc-1536">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="897fc-1536">Az.StorageSync</span></span>
* <span data-ttu-id="897fc-1537">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="897fc-1537">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="897fc-1538">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1538">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-1539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1539">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1540">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-1540">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="897fc-1541">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="897fc-1541">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="897fc-1542">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1542">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="897fc-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="897fc-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="897fc-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="897fc-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1545">Az.Compute</span></span>
* <span data-ttu-id="897fc-1546">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="897fc-1546">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="897fc-1547">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1547">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="897fc-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="897fc-1548">Az.Dns</span></span>
* <span data-ttu-id="897fc-1549">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1549">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="897fc-1550">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="897fc-1550">Az.EventGrid</span></span>
* <span data-ttu-id="897fc-1551">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1551">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="897fc-1552">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1552">New cmdlets:</span></span>
    - <span data-ttu-id="897fc-1553">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="897fc-1553">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="897fc-1554">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="897fc-1554">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="897fc-1555">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="897fc-1555">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="897fc-1556">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="897fc-1556">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="897fc-1557">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="897fc-1557">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="897fc-1558">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="897fc-1558">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="897fc-1559">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="897fc-1559">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="897fc-1560">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="897fc-1560">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="897fc-1561">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="897fc-1561">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="897fc-1562">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1562">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="897fc-1563">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="897fc-1563">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="897fc-1564">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="897fc-1564">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="897fc-1565">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="897fc-1565">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="897fc-1566">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="897fc-1566">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="897fc-1567">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="897fc-1567">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="897fc-1568">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="897fc-1568">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="897fc-1569">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-1569">Updated cmdlets:</span></span>
    - <span data-ttu-id="897fc-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="897fc-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="897fc-1571">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1571">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="897fc-1572">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1572">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="897fc-1573">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="897fc-1573">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="897fc-1574">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-1574">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="897fc-1575">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="897fc-1575">Event subscription expiration date,</span></span>
            - <span data-ttu-id="897fc-1576">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="897fc-1576">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="897fc-1577">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1577">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="897fc-1578">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="897fc-1578">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="897fc-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="897fc-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="897fc-1580">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1580">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="897fc-1581">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="897fc-1581">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="897fc-1582">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1582">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="897fc-1583">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="897fc-1583">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-1584">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-1584">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-1585">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="897fc-1585">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="897fc-1586">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1586">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="897fc-1587">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="897fc-1587">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="897fc-1588">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1588">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1589">Az.Network</span></span>
* <span data-ttu-id="897fc-1590">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1590">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="897fc-1591">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1591">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="897fc-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="897fc-1593">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="897fc-1593">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="897fc-1594">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1594">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1595">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="897fc-1595">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="897fc-1596">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1596">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="897fc-1597">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1597">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1598">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="897fc-1598">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="897fc-1599">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="897fc-1599">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="897fc-1600">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="897fc-1600">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="897fc-1601">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1601">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="897fc-1602">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1602">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="897fc-1603">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1603">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="897fc-1604">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1604">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1605">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="897fc-1605">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="897fc-1606">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="897fc-1606">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="897fc-1607">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="897fc-1607">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="897fc-1608">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="897fc-1608">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="897fc-1609">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="897fc-1609">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="897fc-1610">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="897fc-1610">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="897fc-1611">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="897fc-1611">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="897fc-1612">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1612">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="897fc-1613">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1613">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="897fc-1614">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="897fc-1614">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="897fc-1615">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1615">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="897fc-1616">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="897fc-1616">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="897fc-1617">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1617">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="897fc-1618">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1618">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="897fc-1619">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="897fc-1619">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="897fc-1620">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1620">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="897fc-1621">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1621">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="897fc-1622">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1622">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="897fc-1623">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="897fc-1623">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="897fc-1624">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1624">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="897fc-1625">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1625">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="897fc-1626">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="897fc-1626">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="897fc-1627">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1627">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="897fc-1628">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="897fc-1628">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="897fc-1629">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1629">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="897fc-1630">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1630">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="897fc-1631">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1631">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-1632">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1632">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-1633">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="897fc-1633">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1634">Az.Resources</span></span>
* <span data-ttu-id="897fc-1635">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1635">Support for additional Template Export options</span></span>
    - <span data-ttu-id="897fc-1636">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1636">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="897fc-1637">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1637">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="897fc-1638">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-1638">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1639">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-1640">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="897fc-1640">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1641">Az.Sql</span></span>
* <span data-ttu-id="897fc-1642">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1642">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="897fc-1643">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1643">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="897fc-1644">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1644">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="897fc-1645">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="897fc-1645">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="897fc-1646">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="897fc-1646">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="897fc-1647">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="897fc-1647">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="897fc-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="897fc-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="897fc-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="897fc-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1650">Az.Storage</span></span>
* <span data-ttu-id="897fc-1651">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="897fc-1651">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="897fc-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="897fc-1653">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="897fc-1653">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="897fc-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1655">Az.Websites</span></span>
* <span data-ttu-id="897fc-1656">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="897fc-1656">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="897fc-1657">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1657">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="897fc-1658">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1658">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="897fc-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-1659">Az.Cdn</span></span>
* <span data-ttu-id="897fc-1660">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1660">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1661">Az.Compute</span></span>
* <span data-ttu-id="897fc-1662">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="897fc-1662">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="897fc-1663">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="897fc-1663">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-1664">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1664">Az.EventHub</span></span>
* <span data-ttu-id="897fc-1665">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="897fc-1665">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="897fc-1666">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="897fc-1666">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1667">Az.Network</span></span>
* <span data-ttu-id="897fc-1668">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1668">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="897fc-1669">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1669">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-1670">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1670">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-1671">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="897fc-1671">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1672">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1673">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1673">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-1674">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-1674">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-1675">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="897fc-1675">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-1676">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1676">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-1677">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1677">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="897fc-1678">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1678">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1679">Az.Sql</span></span>
* <span data-ttu-id="897fc-1680">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="897fc-1680">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="897fc-1681">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1681">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="897fc-1682">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="897fc-1682">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="897fc-1683">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="897fc-1683">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1684">Az.Websites</span></span>
* <span data-ttu-id="897fc-1685">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-1685">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="897fc-1686">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1686">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="897fc-1687">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-1687">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-1688">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1688">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="897fc-1689">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-1689">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="897fc-1690">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="897fc-1690">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="897fc-1691">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="897fc-1691">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="897fc-1692">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="897fc-1692">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="897fc-1693">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="897fc-1693">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="897fc-1694">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="897fc-1694">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="897fc-1695">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="897fc-1695">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="897fc-1696">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1696">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="897fc-1697">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="897fc-1697">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="897fc-1698">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="897fc-1698">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="897fc-1699">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="897fc-1699">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="897fc-1700">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="897fc-1700">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="897fc-1701">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1701">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="897fc-1702">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="897fc-1702">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="897fc-1703">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="897fc-1703">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="897fc-1704">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="897fc-1704">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="897fc-1705">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="897fc-1705">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="897fc-1706">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1706">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="897fc-1707">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="897fc-1707">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="897fc-1708">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="897fc-1708">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="897fc-1709">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="897fc-1709">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="897fc-1710">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="897fc-1710">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="897fc-1711">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1711">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="897fc-1712">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1712">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="897fc-1713">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1713">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="897fc-1714">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="897fc-1714">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="897fc-1715">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="897fc-1715">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="897fc-1716">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1716">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="897fc-1717">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="897fc-1717">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="897fc-1718">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="897fc-1718">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="897fc-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="897fc-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="897fc-1720">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1720">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="897fc-1721">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1721">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="897fc-1722">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="897fc-1722">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="897fc-1723">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="897fc-1723">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="897fc-1724">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="897fc-1724">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="897fc-1725">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="897fc-1725">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="897fc-1726">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="897fc-1726">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="897fc-1727">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1727">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="897fc-1728">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="897fc-1728">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="897fc-1729">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-1729">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="897fc-1730">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="897fc-1730">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="897fc-1731">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="897fc-1731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="897fc-1732">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1732">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="897fc-1733">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="897fc-1733">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="897fc-1734">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="897fc-1734">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="897fc-1735">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="897fc-1735">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="897fc-1736">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1736">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="897fc-1737">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="897fc-1737">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="897fc-1738">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="897fc-1738">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="897fc-1739">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="897fc-1739">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="897fc-1740">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="897fc-1740">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="897fc-1741">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1741">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="897fc-1742">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="897fc-1742">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="897fc-1743">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="897fc-1743">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="897fc-1744">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1744">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="897fc-1745">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="897fc-1745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="897fc-1746">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="897fc-1746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="897fc-1747">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="897fc-1748">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1748">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="897fc-1749">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="897fc-1749">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="897fc-1750">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="897fc-1750">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="897fc-1751">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1751">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="897fc-1752">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="897fc-1752">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="897fc-1753">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="897fc-1753">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="897fc-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="897fc-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="897fc-1755">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="897fc-1755">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="897fc-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="897fc-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="897fc-1757">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="897fc-1757">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="897fc-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="897fc-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="897fc-1759">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="897fc-1759">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="897fc-1760">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="897fc-1760">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="897fc-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="897fc-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="897fc-1762">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="897fc-1762">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="897fc-1763">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="897fc-1763">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="897fc-1764">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="897fc-1764">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1765">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1765">Az.Automation</span></span>
* <span data-ttu-id="897fc-1766">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="897fc-1766">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="897fc-1767">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="897fc-1767">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="897fc-1768">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="897fc-1768">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="897fc-1769">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="897fc-1769">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="897fc-1770">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="897fc-1770">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="897fc-1771">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="897fc-1771">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="897fc-1772">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="897fc-1772">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1773">Az.Compute</span></span>
* <span data-ttu-id="897fc-1774">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1774">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="897fc-1775">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="897fc-1775">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-1776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-1776">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-1777">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="897fc-1777">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1778">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1778">Az.Monitor</span></span>
* <span data-ttu-id="897fc-1779">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="897fc-1779">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1780">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1780">Az.Network</span></span>
* <span data-ttu-id="897fc-1781">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1781">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="897fc-1782">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="897fc-1782">Updated cmdlet:</span></span>
        - <span data-ttu-id="897fc-1783">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-1783">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="897fc-1784">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="897fc-1784">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1785">Az.Resources</span></span>
* <span data-ttu-id="897fc-1786">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1786">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1787">Az.Sql</span></span>
* <span data-ttu-id="897fc-1788">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="897fc-1788">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="897fc-1789">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1789">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1790">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1791">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="897fc-1791">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-1792">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1792">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-1793">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="897fc-1793">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="897fc-1794">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="897fc-1794">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1795">Az.Compute</span></span>
* <span data-ttu-id="897fc-1796">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="897fc-1796">Proximity placement group feature.</span></span>
    - <span data-ttu-id="897fc-1797">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1797">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="897fc-1798">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-1798">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="897fc-1799">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1799">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="897fc-1800">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="897fc-1800">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="897fc-1801">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1801">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="897fc-1802">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="897fc-1802">Breaking changes</span></span>
    - <span data-ttu-id="897fc-1803">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1803">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="897fc-1804">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1804">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="897fc-1805">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="897fc-1805">Az.DeploymentManager</span></span>
* <span data-ttu-id="897fc-1806">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1806">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="897fc-1807">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="897fc-1807">Az.Dns</span></span>
* <span data-ttu-id="897fc-1808">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="897fc-1808">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="897fc-1809">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="897fc-1809">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="897fc-1810">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1810">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="897fc-1811">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-1811">Az.FrontDoor</span></span>
* <span data-ttu-id="897fc-1812">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1812">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="897fc-1813">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="897fc-1813">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="897fc-1814">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-1814">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-1815">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="897fc-1815">Removed two cmdlets:</span></span>
    - <span data-ttu-id="897fc-1816">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="897fc-1816">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="897fc-1817">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="897fc-1817">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="897fc-1818">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="897fc-1818">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="897fc-1819">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="897fc-1819">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="897fc-1820">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="897fc-1820">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="897fc-1821">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="897fc-1821">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1822">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1822">Az.Monitor</span></span>
* <span data-ttu-id="897fc-1823">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="897fc-1823">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="897fc-1824">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="897fc-1824">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="897fc-1825">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="897fc-1825">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="897fc-1826">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="897fc-1826">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="897fc-1827">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="897fc-1827">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="897fc-1828">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="897fc-1828">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="897fc-1829">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="897fc-1829">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="897fc-1830">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1830">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="897fc-1831">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1831">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="897fc-1832">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1832">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="897fc-1833">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1833">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="897fc-1834">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="897fc-1834">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="897fc-1835">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="897fc-1835">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="897fc-1836">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="897fc-1836">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1837">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1837">Az.Network</span></span>
* <span data-ttu-id="897fc-1838">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1838">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="897fc-1839">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1839">New cmdlets</span></span>
        - <span data-ttu-id="897fc-1840">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-1840">New-AzNatGateway</span></span>
        - <span data-ttu-id="897fc-1841">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-1841">Get-AzNatGateway</span></span>
        - <span data-ttu-id="897fc-1842">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-1842">Set-AzNatGateway</span></span>
        - <span data-ttu-id="897fc-1843">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-1843">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="897fc-1844">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-1844">Updated cmdlets</span></span>
        - <span data-ttu-id="897fc-1845">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="897fc-1845">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="897fc-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="897fc-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="897fc-1847">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-1847">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="897fc-1848">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="897fc-1848">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="897fc-1849">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="897fc-1849">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-1850">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1850">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-1851">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="897fc-1851">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="897fc-1852">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1852">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="897fc-1853">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="897fc-1853">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1854">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1854">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1855">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="897fc-1855">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="897fc-1856">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="897fc-1856">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="897fc-1857">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="897fc-1857">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="897fc-1858">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="897fc-1858">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="897fc-1859">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="897fc-1859">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="897fc-1860">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="897fc-1860">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="897fc-1861">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="897fc-1861">Az.Relay</span></span>
* <span data-ttu-id="897fc-1862">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="897fc-1862">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-1863">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-1863">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-1864">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1864">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1865">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1865">Az.Storage</span></span>
* <span data-ttu-id="897fc-1866">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="897fc-1866">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="897fc-1867">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="897fc-1867">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="897fc-1868">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-1868">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="897fc-1869">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1869">New-AzStorageAccount</span></span>
* <span data-ttu-id="897fc-1870">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="897fc-1870">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="897fc-1871">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1871">New-AzStorageAccount</span></span>
    - <span data-ttu-id="897fc-1872">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1872">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="897fc-1873">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-1873">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1874">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1874">Az.Websites</span></span>
* <span data-ttu-id="897fc-1875">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1875">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="897fc-1876">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1876">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="897fc-1877">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1877">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-1878">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-1878">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-1879">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="897fc-1879">General availability of `Az` module</span></span>
* <span data-ttu-id="897fc-1880">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="897fc-1880">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="897fc-1881">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="897fc-1881">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="897fc-1882">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1882">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="897fc-1883">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1883">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="897fc-1884">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1884">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="897fc-1885">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-1885">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-1886">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1886">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1887">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="897fc-1887">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="897fc-1888">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-1888">Az.Batch</span></span>
* <span data-ttu-id="897fc-1889">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-1890">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-1890">Az.Cdn</span></span>
* <span data-ttu-id="897fc-1891">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1891">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-1892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1892">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-1893">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1894">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1894">Az.Compute</span></span>
* <span data-ttu-id="897fc-1895">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="897fc-1895">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="897fc-1896">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1896">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1897">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1897">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1898">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1899">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="897fc-1899">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-1900">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-1900">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-1901">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="897fc-1902">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="897fc-1902">Az.EventGrid</span></span>
* <span data-ttu-id="897fc-1903">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="897fc-1903">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-1904">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1904">Az.EventHub</span></span>
* <span data-ttu-id="897fc-1905">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1905">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="897fc-1906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="897fc-1906">Az.HDInsight</span></span>
* <span data-ttu-id="897fc-1907">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-1908">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-1908">Az.IotHub</span></span>
* <span data-ttu-id="897fc-1909">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1909">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-1910">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-1910">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-1911">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1912">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1912">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="897fc-1913">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="897fc-1913">Az.MachineLearning</span></span>
* <span data-ttu-id="897fc-1914">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1914">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="897fc-1915">Az.Media</span><span class="sxs-lookup"><span data-stu-id="897fc-1915">Az.Media</span></span>
* <span data-ttu-id="897fc-1916">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1916">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-1917">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-1917">Az.Monitor</span></span>
  * <span data-ttu-id="897fc-1918">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="897fc-1918">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="897fc-1919">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="897fc-1919">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="897fc-1920">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="897fc-1920">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="897fc-1921">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="897fc-1921">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="897fc-1922">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="897fc-1922">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="897fc-1923">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="897fc-1923">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="897fc-1924">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1924">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-1925">Az.Network</span></span>
* <span data-ttu-id="897fc-1926">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1927">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1927">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="897fc-1928">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="897fc-1928">Az.NotificationHubs</span></span>
* <span data-ttu-id="897fc-1929">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-1930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-1930">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-1931">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="897fc-1932">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="897fc-1932">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="897fc-1933">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1933">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-1934">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1934">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-1935">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1935">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1936">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1936">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="897fc-1937">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1937">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="897fc-1938">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1938">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="897fc-1939">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="897fc-1939">Az.RedisCache</span></span>
* <span data-ttu-id="897fc-1940">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1940">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1941">Az.Resources</span></span>
* <span data-ttu-id="897fc-1942">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1942">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1943">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1943">Az.Sql</span></span>
* <span data-ttu-id="897fc-1944">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="897fc-1944">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="897fc-1945">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1946">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="897fc-1946">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="897fc-1947">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1947">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="897fc-1948">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="897fc-1948">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="897fc-1949">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="897fc-1949">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="897fc-1950">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1950">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-1951">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-1951">Az.Websites</span></span>
* <span data-ttu-id="897fc-1952">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="897fc-1952">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="897fc-1953">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="897fc-1953">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="897fc-1954">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1954">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="897fc-1955">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-1955">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="897fc-1956">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-1956">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-1957">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-1957">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-1958">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="897fc-1958">General availability of `Az` module</span></span>
* <span data-ttu-id="897fc-1959">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="897fc-1959">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="897fc-1960">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="897fc-1960">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="897fc-1961">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1961">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="897fc-1962">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1962">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="897fc-1963">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1963">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="897fc-1964">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-1964">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="897fc-1965">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-1965">Az.Accounts</span></span>
* <span data-ttu-id="897fc-1966">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="897fc-1966">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="897fc-1967">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="897fc-1967">Az.AnalysisServices</span></span>
* <span data-ttu-id="897fc-1968">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="897fc-1968">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="897fc-1969">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="897fc-1969">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-1970">Az.Automation</span></span>
* <span data-ttu-id="897fc-1971">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="897fc-1971">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="897fc-1972">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="897fc-1972">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="897fc-1973">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="897fc-1973">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-1974">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-1974">Az.Compute</span></span>
* <span data-ttu-id="897fc-1975">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-1975">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="897fc-1976">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="897fc-1976">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="897fc-1977">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-1977">Az.ContainerInstance</span></span>
* <span data-ttu-id="897fc-1978">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="897fc-1978">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-1979">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-1979">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-1980">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1980">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="897fc-1981">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-1981">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-1982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-1982">Az.Resources</span></span>
* <span data-ttu-id="897fc-1983">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-1983">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="897fc-1984">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-1984">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="897fc-1985">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="897fc-1985">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="897fc-1986">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="897fc-1986">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="897fc-1987">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="897fc-1987">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="897fc-1988">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="897fc-1988">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-1989">Az.Sql</span></span>
* <span data-ttu-id="897fc-1990">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="897fc-1990">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-1991">Az.Storage</span></span>
* <span data-ttu-id="897fc-1992">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="897fc-1992">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="897fc-1993">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="897fc-1993">New-AzStorageContext</span></span>
* <span data-ttu-id="897fc-1994">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="897fc-1994">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="897fc-1995">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="897fc-1995">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="897fc-1996">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="897fc-1996">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="897fc-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="897fc-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="897fc-1999">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="897fc-1999">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="897fc-2000">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="897fc-2000">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="897fc-2001">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="897fc-2001">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="897fc-2002">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="897fc-2002">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="897fc-2003">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="897fc-2003">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="897fc-2004">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2004">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="897fc-2005">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="897fc-2005">Highlights since the last major release</span></span>
* <span data-ttu-id="897fc-2006">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="897fc-2006">General availability of `Az` module</span></span>
* <span data-ttu-id="897fc-2007">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="897fc-2007">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="897fc-2008">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="897fc-2008">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="897fc-2009">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2009">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="897fc-2010">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2010">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="897fc-2011">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2011">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="897fc-2012">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2012">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-2013">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-2013">Az.Automation</span></span>
* <span data-ttu-id="897fc-2014">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="897fc-2014">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="897fc-2015">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="897fc-2015">Dynamic grouping</span></span>
    * <span data-ttu-id="897fc-2016">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="897fc-2016">Pre-Post script</span></span>
    * <span data-ttu-id="897fc-2017">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="897fc-2017">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2018">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2018">Az.Compute</span></span>
* <span data-ttu-id="897fc-2019">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2019">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="897fc-2020">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2020">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-2021">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-2021">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-2022">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2022">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2023">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2023">Az.Network</span></span>
* <span data-ttu-id="897fc-2024">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2024">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="897fc-2025">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2025">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2026">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2026">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-2027">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="897fc-2027">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="897fc-2028">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2028">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2029">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2029">Az.Resources</span></span>
* <span data-ttu-id="897fc-2030">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2030">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="897fc-2031">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="897fc-2031">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2032">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2032">Az.Sql</span></span>
* <span data-ttu-id="897fc-2033">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="897fc-2033">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2034">Az.Storage</span></span>
* <span data-ttu-id="897fc-2035">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2035">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="897fc-2036">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-2036">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="897fc-2037">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-2037">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="897fc-2038">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="897fc-2038">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="897fc-2039">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="897fc-2039">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="897fc-2040">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="897fc-2040">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="897fc-2041">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="897fc-2041">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-2042">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2042">Az.Websites</span></span>
* <span data-ttu-id="897fc-2043">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="897fc-2043">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="897fc-2044">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2044">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-2045">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2045">Az.Accounts</span></span>
* <span data-ttu-id="897fc-2046">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="897fc-2046">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="897fc-2047">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2047">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-2048">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-2048">Az.Automation</span></span>
* <span data-ttu-id="897fc-2049">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="897fc-2049">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="897fc-2050">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="897fc-2050">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="897fc-2051">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="897fc-2051">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-2052">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-2052">Az.Cdn</span></span>
* <span data-ttu-id="897fc-2053">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="897fc-2053">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2054">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2054">Az.Compute</span></span>
* <span data-ttu-id="897fc-2055">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2055">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-2056">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-2056">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-2057">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2057">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="897fc-2058">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="897fc-2058">Az.LogicApp</span></span>
* <span data-ttu-id="897fc-2059">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="897fc-2059">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2060">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2060">Az.Network</span></span>
* <span data-ttu-id="897fc-2061">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2061">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2062">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2062">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-2063">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="897fc-2063">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="897fc-2064">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="897fc-2064">SDK Update</span></span>
* <span data-ttu-id="897fc-2065">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-2065">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="897fc-2066">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2066">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2067">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2067">Az.Resources</span></span>
* <span data-ttu-id="897fc-2068">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2068">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="897fc-2069">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="897fc-2069">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="897fc-2070">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2070">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="897fc-2071">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="897fc-2071">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="897fc-2072">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2072">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="897fc-2073">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="897fc-2073">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2074">Az.Sql</span></span>
* <span data-ttu-id="897fc-2075">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2075">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="897fc-2076">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2076">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2077">Az.Storage</span></span>
* <span data-ttu-id="897fc-2078">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="897fc-2078">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="897fc-2079">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2079">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="897fc-2080">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2080">Az.AnalysisServices</span></span>
* <span data-ttu-id="897fc-2081">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2081">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-2082">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-2082">Az.Automation</span></span>
* <span data-ttu-id="897fc-2083">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2083">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="897fc-2084">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2084">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="897fc-2085">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="897fc-2085">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-2087">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-2087">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2088">Az.Compute</span></span>
* <span data-ttu-id="897fc-2089">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2089">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="897fc-2090">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="897fc-2090">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="897fc-2091">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2091">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="897fc-2092">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="897fc-2092">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2093">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2093">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-2094">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2094">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="897fc-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="897fc-2095">Az.EventHub</span></span>
* <span data-ttu-id="897fc-2096">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2096">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-2097">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-2097">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-2098">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2098">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="897fc-2099">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="897fc-2099">Az.LogicApp</span></span>
* <span data-ttu-id="897fc-2100">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2100">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="897fc-2101">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2101">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="897fc-2102">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="897fc-2102">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="897fc-2103">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="897fc-2103">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="897fc-2104">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="897fc-2104">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="897fc-2105">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="897fc-2105">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="897fc-2106">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="897fc-2106">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="897fc-2107">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2107">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="897fc-2108">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2108">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="897fc-2109">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2109">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="897fc-2110">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2110">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="897fc-2111">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2111">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="897fc-2112">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2112">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="897fc-2113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-2113">Az.Monitor</span></span>
* <span data-ttu-id="897fc-2114">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2114">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2115">Az.Network</span></span>
* <span data-ttu-id="897fc-2116">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2116">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-2117">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-2117">Az.OperationalInsights</span></span>
* <span data-ttu-id="897fc-2118">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2118">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="897fc-2119">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2119">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="897fc-2120">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="897fc-2120">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2121">Az.Resources</span></span>
* <span data-ttu-id="897fc-2122">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="897fc-2122">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="897fc-2123">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="897fc-2123">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="897fc-2124">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="897fc-2124">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="897fc-2125">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="897fc-2125">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2126">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2126">Az.Sql</span></span>
* <span data-ttu-id="897fc-2127">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2127">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="897fc-2128">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="897fc-2128">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-2129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2129">Az.Websites</span></span>
* <span data-ttu-id="897fc-2130">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2130">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="897fc-2131">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2131">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-2132">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2132">Az.Accounts</span></span>
* <span data-ttu-id="897fc-2133">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="897fc-2133">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="897fc-2134">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2134">Az.AnalysisServices</span></span>
<span data-ttu-id="897fc-2135">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="897fc-2135">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2136">Az.Compute</span></span>
* <span data-ttu-id="897fc-2137">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2137">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="897fc-2138">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2138">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="897fc-2139">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2139">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2140">Az.RecoveryServices</span></span>
<span data-ttu-id="897fc-2141">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="897fc-2141">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2142">Az.Resources</span></span>
* <span data-ttu-id="897fc-2143">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2143">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="897fc-2144">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="897fc-2144">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="897fc-2145">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2145">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="897fc-2146">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="897fc-2146">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2147">Az.Sql</span></span>
* <span data-ttu-id="897fc-2148">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2148">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="897fc-2149">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="897fc-2149">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="897fc-2150">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2150">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="897fc-2151">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2151">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-2152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2152">Az.Accounts</span></span>
* <span data-ttu-id="897fc-2153">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="897fc-2153">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="897fc-2154">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2154">Az.AnalysisServices</span></span>
* <span data-ttu-id="897fc-2155">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="897fc-2155">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2156">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2156">Az.RecoveryServices</span></span>
* <span data-ttu-id="897fc-2157">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="897fc-2157">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="897fc-2158">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2158">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-2159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2159">Az.Accounts</span></span>
* <span data-ttu-id="897fc-2160">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2160">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="897fc-2161">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="897fc-2162">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2162">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="897fc-2163">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="897fc-2163">Az.Aks</span></span>
* <span data-ttu-id="897fc-2164">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2164">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="897fc-2165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-2165">Az.Automation</span></span>
* <span data-ttu-id="897fc-2166">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2166">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="897fc-2167">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2167">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="897fc-2168">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="897fc-2168">Az.Cdn</span></span>
* <span data-ttu-id="897fc-2169">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2169">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2170">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2170">Az.Compute</span></span>
* <span data-ttu-id="897fc-2171">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2171">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="897fc-2172">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2172">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="897fc-2173">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2173">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="897fc-2174">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="897fc-2174">Az.ContainerRegistry</span></span>
* <span data-ttu-id="897fc-2175">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2175">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="897fc-2176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="897fc-2176">Az.DataFactory</span></span>
* <span data-ttu-id="897fc-2177">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2177">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2178">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2178">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-2179">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2179">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="897fc-2180">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="897fc-2180">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="897fc-2181">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2181">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-2182">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-2182">Az.IotHub</span></span>
* <span data-ttu-id="897fc-2183">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2183">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="897fc-2184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-2184">Az.KeyVault</span></span>
* <span data-ttu-id="897fc-2185">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2185">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2186">Az.Network</span></span>
* <span data-ttu-id="897fc-2187">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2187">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2188">Az.Resources</span></span>
* <span data-ttu-id="897fc-2189">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2189">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="897fc-2190">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="897fc-2190">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="897fc-2191">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="897fc-2191">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="897fc-2192">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="897fc-2192">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="897fc-2193">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="897fc-2193">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="897fc-2194">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2194">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="897fc-2195">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="897fc-2195">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-2196">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-2196">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-2197">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="897fc-2197">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="897fc-2198">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2198">Fix some error messages.</span></span>
* <span data-ttu-id="897fc-2199">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="897fc-2199">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="897fc-2200">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-2200">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="897fc-2201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="897fc-2201">Az.SignalR</span></span>
* <span data-ttu-id="897fc-2202">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2202">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2203">Az.Sql</span></span>
* <span data-ttu-id="897fc-2204">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2204">Update incorrect online help URLs</span></span>
* <span data-ttu-id="897fc-2205">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2205">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="897fc-2206">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="897fc-2206">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="897fc-2207">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="897fc-2207">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-2208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2208">Az.Storage</span></span>
* <span data-ttu-id="897fc-2209">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2209">Update incorrect online help URLs</span></span>
* <span data-ttu-id="897fc-2210">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-2210">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="897fc-2211">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="897fc-2211">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="897fc-2212">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="897fc-2212">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="897fc-2213">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="897fc-2213">Az.TrafficManager</span></span>
* <span data-ttu-id="897fc-2214">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2214">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-2215">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2215">Az.Websites</span></span>
* <span data-ttu-id="897fc-2216">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2216">Update incorrect online help URLs</span></span>
* <span data-ttu-id="897fc-2217">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-2217">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="897fc-2218">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="897fc-2218">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="897fc-2219">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="897fc-2219">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="897fc-2220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2220">Az.Accounts</span></span>
* <span data-ttu-id="897fc-2221">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2221">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2222">Az.Compute</span></span>
* <span data-ttu-id="897fc-2223">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="897fc-2223">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="897fc-2224">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2224">Updated the description of ID in help files</span></span>
* <span data-ttu-id="897fc-2225">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2225">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-2227">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="897fc-2227">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="897fc-2228">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2228">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="897fc-2229">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="897fc-2229">Az.EventGrid</span></span>
* <span data-ttu-id="897fc-2230">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2230">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="897fc-2231">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="897fc-2231">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="897fc-2232">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-2232">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="897fc-2233">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="897fc-2233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="897fc-2234">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="897fc-2234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="897fc-2235">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="897fc-2235">Dead letter endpoint.</span></span>
    - <span data-ttu-id="897fc-2236">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="897fc-2236">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="897fc-2237">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="897fc-2237">Event Time-To-Live,</span></span>
        - <span data-ttu-id="897fc-2238">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="897fc-2238">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="897fc-2239">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="897fc-2239">Dead letter endpoint.</span></span>
* <span data-ttu-id="897fc-2240">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2240">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="897fc-2241">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="897fc-2241">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="897fc-2242">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="897fc-2242">Az.IotHub</span></span>
* <span data-ttu-id="897fc-2243">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2243">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="897fc-2244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="897fc-2244">Az.LogicApp</span></span>
* <span data-ttu-id="897fc-2245">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="897fc-2245">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2246">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2246">Az.Resources</span></span>
* <span data-ttu-id="897fc-2247">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2247">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="897fc-2248">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="897fc-2248">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="897fc-2249">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2249">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="897fc-2250">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2250">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="897fc-2251">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="897fc-2251">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="897fc-2252">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="897fc-2252">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="897fc-2253">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="897fc-2253">Az.SignalR</span></span>
* <span data-ttu-id="897fc-2254">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2254">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2255">Az.Sql</span></span>
* <span data-ttu-id="897fc-2256">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2256">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="897fc-2257">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2257">Az.Storage</span></span>
* <span data-ttu-id="897fc-2258">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2258">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="897fc-2259">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="897fc-2259">New-AzStorageContext</span></span>
* <span data-ttu-id="897fc-2260">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="897fc-2260">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="897fc-2261">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="897fc-2261">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-2262">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2262">Az.Websites</span></span>
* <span data-ttu-id="897fc-2263">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2263">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="897fc-2264">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2264">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="897fc-2265">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2265">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="897fc-2266">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-2266">General</span></span>

- <span data-ttu-id="897fc-2267">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="897fc-2267">General Availability of Az Module</span></span>
- <span data-ttu-id="897fc-2268">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="897fc-2268">Online help for each module</span></span>
- <span data-ttu-id="897fc-2269">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="897fc-2269">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="897fc-2270">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2270">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="897fc-2271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="897fc-2271">Az.Accounts</span></span>
- <span data-ttu-id="897fc-2272">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="897fc-2272">Changed from Az.Profile</span></span>
- <span data-ttu-id="897fc-2273">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="897fc-2273">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="897fc-2274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-2274">Az.ApiManagement</span></span>
- <span data-ttu-id="897fc-2275">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="897fc-2275">Fixes for #7002</span></span>
- <span data-ttu-id="897fc-2276">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="897fc-2277">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="897fc-2277">Az.Batch</span></span>
- <span data-ttu-id="897fc-2278">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2278">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="897fc-2279">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="897fc-2279">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="897fc-2280">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="897fc-2281">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="897fc-2281">Az.Billing</span></span>
- <span data-ttu-id="897fc-2282">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2282">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="897fc-2283">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2283">Az.CognitivServices</span></span>
- <span data-ttu-id="897fc-2284">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2284">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="897fc-2285">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-2285">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="897fc-2286">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2286">Az.ContainerInstance</span></span>
- <span data-ttu-id="897fc-2287">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2287">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="897fc-2288">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="897fc-2288">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="897fc-2289">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2289">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2290">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2290">Az.DataLakeStore</span></span>
- <span data-ttu-id="897fc-2291">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2291">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="897fc-2292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="897fc-2292">Az.Monitor</span></span>
- <span data-ttu-id="897fc-2293">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2293">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="897fc-2294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="897fc-2294">Az.KeyVault</span></span>
- <span data-ttu-id="897fc-2295">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-2295">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="897fc-2296">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="897fc-2296">Az.MachineLearning</span></span>
- <span data-ttu-id="897fc-2297">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="897fc-2297">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="897fc-2298">Az.Media</span><span class="sxs-lookup"><span data-stu-id="897fc-2298">Az.Media</span></span>
- <span data-ttu-id="897fc-2299">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="897fc-2299">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="897fc-2300">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2300">Az.Network</span></span>
<span data-ttu-id="897fc-2301">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2301">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="897fc-2302">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-2302">New cmdlets added:</span></span>
        - <span data-ttu-id="897fc-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2308">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="897fc-2308">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="897fc-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="897fc-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="897fc-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="897fc-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="897fc-2311">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2311">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="897fc-2312">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="897fc-2312">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="897fc-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="897fc-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="897fc-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="897fc-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="897fc-2315">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-2315">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="897fc-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="897fc-2317">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2317">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="897fc-2318">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="897fc-2318">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="897fc-2319">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="897fc-2319">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="897fc-2320">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="897fc-2320">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="897fc-2321">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="897fc-2321">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="897fc-2322">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2322">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="897fc-2323">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="897fc-2324">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-2324">Az.OperationalInsights</span></span>
- <span data-ttu-id="897fc-2325">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="897fc-2326">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="897fc-2326">Az.Profile</span></span>
- <span data-ttu-id="897fc-2327">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-2327">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2328">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2328">Az.RecoveryServices</span></span>
- <span data-ttu-id="897fc-2329">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2329">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="897fc-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2330">Az.Resources</span></span>
- <span data-ttu-id="897fc-2331">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2331">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="897fc-2332">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-2332">Az.ServiceFabric</span></span>
- <span data-ttu-id="897fc-2333">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="897fc-2333">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="897fc-2334">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2334">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="897fc-2335">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="897fc-2335">Az.SIgnalR</span></span>
- <span data-ttu-id="897fc-2336">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="897fc-2336">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="897fc-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2337">Az.Sql</span></span>
- <span data-ttu-id="897fc-2338">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2338">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="897fc-2339">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2339">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="897fc-2340">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="897fc-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2341">Az.Storage</span></span>
- <span data-ttu-id="897fc-2342">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2342">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="897fc-2343">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2343">Az.Websites</span></span>
- <span data-ttu-id="897fc-2344">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="897fc-2344">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="897fc-2345">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2345">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="897fc-2346">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-2346">General</span></span>

* <span data-ttu-id="897fc-2347">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="897fc-2347">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="897fc-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2348">Az.Compute</span></span>

* <span data-ttu-id="897fc-2349">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2349">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2350">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2350">Az.DataLakeStore</span></span>

* <span data-ttu-id="897fc-2351">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2351">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="897fc-2352">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="897fc-2352">Az.FrontDoor</span></span>

* <span data-ttu-id="897fc-2353">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2353">Fixed some broken links</span></span>
    - <span data-ttu-id="897fc-2354">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2354">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="897fc-2355">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2355">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="897fc-2356">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2356">Az.RecoveryServices</span></span>

* <span data-ttu-id="897fc-2357">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2357">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="897fc-2358">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="897fc-2358">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="897fc-2359">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2359">Az.Resources</span></span>

* <span data-ttu-id="897fc-2360">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="897fc-2360">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="897fc-2361">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="897fc-2361">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="897fc-2362">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2362">Az.Sql</span></span>

* <span data-ttu-id="897fc-2363">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="897fc-2363">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="897fc-2364">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2364">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="897fc-2365">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2365">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="897fc-2366">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2366">Az.Storage</span></span>

* <span data-ttu-id="897fc-2367">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2367">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="897fc-2368">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2368">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="897fc-2369">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="897fc-2369">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="897fc-2370">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2370">Support Static Website configuration</span></span>
    - <span data-ttu-id="897fc-2371">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="897fc-2371">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="897fc-2372">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="897fc-2372">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="897fc-2373">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2373">Az.Websites</span></span>

* <span data-ttu-id="897fc-2374">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="897fc-2374">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="897fc-2375">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="897fc-2375">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="897fc-2376">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="897fc-2376">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="897fc-2377">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2377">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="897fc-2378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="897fc-2378">Az.ApiManagement</span></span>
* <span data-ttu-id="897fc-2379">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2379">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="897fc-2380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="897fc-2380">Az.Automation</span></span>
* <span data-ttu-id="897fc-2381">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="897fc-2381">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="897fc-2382">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2382">Added Update Management cmdlets</span></span>
* <span data-ttu-id="897fc-2383">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2383">Added Source Control cmdlets</span></span>
* <span data-ttu-id="897fc-2384">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2384">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="897fc-2385">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2385">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="897fc-2386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2386">Az.Compute</span></span>
* <span data-ttu-id="897fc-2387">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2387">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="897fc-2388">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2388">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="897fc-2389">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2389">Az.ContainerInstance</span></span>
* <span data-ttu-id="897fc-2390">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2390">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="897fc-2391">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="897fc-2391">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="897fc-2392">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2392">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="897fc-2393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2393">Az.Network</span></span>
* <span data-ttu-id="897fc-2394">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="897fc-2394">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="897fc-2395">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2395">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="897fc-2396">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2396">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="897fc-2397">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2397">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="897fc-2398">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="897fc-2398">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="897fc-2399">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2399">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="897fc-2400">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="897fc-2400">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="897fc-2401">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="897fc-2401">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="897fc-2402">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="897fc-2402">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="897fc-2403">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2403">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="897fc-2404">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="897fc-2404">Az.Relay</span></span>
* <span data-ttu-id="897fc-2405">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="897fc-2405">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="897fc-2406">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2406">Az.Resources</span></span>
* <span data-ttu-id="897fc-2407">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2407">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="897fc-2408">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="897fc-2408">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="897fc-2409">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="897fc-2409">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="897fc-2410">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-2410">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-2411">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2411">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="897fc-2412">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2412">Az.Sql</span></span>
* <span data-ttu-id="897fc-2413">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2413">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="897fc-2414">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2414">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="897fc-2415">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2415">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="897fc-2416">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2416">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="897fc-2417">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="897fc-2417">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="897fc-2418">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="897fc-2418">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="897fc-2419">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="897fc-2419">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="897fc-2420">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="897fc-2420">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="897fc-2421">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="897fc-2421">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="897fc-2422">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="897fc-2422">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="897fc-2423">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="897fc-2423">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="897fc-2424">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="897fc-2424">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="897fc-2425">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="897fc-2425">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="897fc-2426">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="897fc-2426">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="897fc-2427">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="897fc-2427">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="897fc-2428">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="897fc-2428">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="897fc-2429">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2429">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="897fc-2430">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2430">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="897fc-2431">Allgemein</span><span class="sxs-lookup"><span data-stu-id="897fc-2431">General</span></span>
* <span data-ttu-id="897fc-2432">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="897fc-2432">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="897fc-2433">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="897fc-2433">Az.Profile</span></span>
* <span data-ttu-id="897fc-2434">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2434">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="897fc-2435">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2435">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="897fc-2436">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2436">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="897fc-2437">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2437">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="897fc-2438">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2438">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="897fc-2439">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2439">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="897fc-2440">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="897fc-2440">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-2441">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2441">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-2442">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2442">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2443">Az.Compute</span></span>
* <span data-ttu-id="897fc-2444">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2444">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="897fc-2445">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="897fc-2445">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="897fc-2446">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="897fc-2446">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2447">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-2448">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="897fc-2448">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="897fc-2449">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2449">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="897fc-2450">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="897fc-2450">Az.Insights</span></span>
* <span data-ttu-id="897fc-2451">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="897fc-2451">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="897fc-2452">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="897fc-2452">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="897fc-2453">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="897fc-2453">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="897fc-2454">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2454">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2455">Az.Network</span></span>
* <span data-ttu-id="897fc-2456">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="897fc-2456">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="897fc-2457">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-2457">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="897fc-2458">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="897fc-2458">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="897fc-2459">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="897fc-2459">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="897fc-2460">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="897fc-2460">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="897fc-2461">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="897fc-2461">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="897fc-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="897fc-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="897fc-2463">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="897fc-2463">Az.PolicyInsights</span></span>
* <span data-ttu-id="897fc-2464">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2464">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2465">Az.Resources</span></span>
* <span data-ttu-id="897fc-2466">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="897fc-2466">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="897fc-2467">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="897fc-2467">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="897fc-2468">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="897fc-2468">Az.ServiceBus</span></span>
* <span data-ttu-id="897fc-2469">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="897fc-2469">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="897fc-2470">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="897fc-2470">Az.ServiceFabric</span></span>
* <span data-ttu-id="897fc-2471">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2471">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="897fc-2472">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="897fc-2472">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="897fc-2473">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="897fc-2473">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="897fc-2474">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="897fc-2474">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="897fc-2475">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2475">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="897fc-2476">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2476">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="897fc-2477">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="897fc-2477">Az.Profile</span></span>
* <span data-ttu-id="897fc-2478">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2478">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="897fc-2479">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2479">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2480">Az.Compute</span></span>
* <span data-ttu-id="897fc-2481">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="897fc-2481">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="897fc-2482">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2482">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="897fc-2483">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="897fc-2483">Az.DataLakeStore</span></span>
* <span data-ttu-id="897fc-2484">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2484">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="897fc-2485">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="897fc-2485">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="897fc-2486">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="897fc-2486">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="897fc-2487">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="897fc-2487">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="897fc-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="897fc-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2489">Az.Network</span></span>
* <span data-ttu-id="897fc-2490">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="897fc-2490">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="897fc-2491">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2491">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2492">Az.Resources</span></span>
* <span data-ttu-id="897fc-2493">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="897fc-2493">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="897fc-2494">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2494">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="897fc-2495">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2495">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="897fc-2496">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="897fc-2496">Azure.Storage</span></span>
* <span data-ttu-id="897fc-2497">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="897fc-2497">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="897fc-2498">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="897fc-2498">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="897fc-2499">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="897fc-2499">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="897fc-2500">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="897fc-2500">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="897fc-2501">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="897fc-2501">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="897fc-2502">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="897fc-2502">Az.CognitiveServices</span></span>
* <span data-ttu-id="897fc-2503">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2503">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="897fc-2504">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="897fc-2504">Az.Compute</span></span>
* <span data-ttu-id="897fc-2505">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="897fc-2505">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="897fc-2506">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2506">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="897fc-2507">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="897fc-2507">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="897fc-2508">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="897fc-2508">Az.DataFactoryV2</span></span>
* <span data-ttu-id="897fc-2509">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="897fc-2509">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="897fc-2510">Az.Network</span><span class="sxs-lookup"><span data-stu-id="897fc-2510">Az.Network</span></span>
* <span data-ttu-id="897fc-2511">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="897fc-2511">Added NetworkProfile functionality.</span></span> <span data-ttu-id="897fc-2512">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2512">new cmdlets added</span></span>
    - <span data-ttu-id="897fc-2513">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="897fc-2513">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="897fc-2514">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="897fc-2514">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="897fc-2515">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="897fc-2515">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="897fc-2516">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="897fc-2516">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="897fc-2517">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-2517">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="897fc-2518">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="897fc-2518">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="897fc-2519">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2519">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="897fc-2520">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2520">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="897fc-2521">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2521">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="897fc-2522">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="897fc-2522">Az.RedisCache</span></span>
* <span data-ttu-id="897fc-2523">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="897fc-2523">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="897fc-2524">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2524">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="897fc-2525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="897fc-2525">Az.Resources</span></span>
* <span data-ttu-id="897fc-2526">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="897fc-2526">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="897fc-2527">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="897fc-2527">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="897fc-2528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="897fc-2528">Az.Sql</span></span>
* <span data-ttu-id="897fc-2529">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="897fc-2529">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="897fc-2530">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="897fc-2530">Az.Websites</span></span>
* <span data-ttu-id="897fc-2531">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="897fc-2531">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="897fc-2532">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="897fc-2532">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="897fc-2533">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="897fc-2533">0.2.0 - September 2018</span></span>
 <span data-ttu-id="897fc-2534">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="897fc-2534">Initial Release</span></span>
