---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: ea8169e0aa04fb4cc27b715ef9dfde86f0e75e85
ms.sourcegitcommit: b94a3f00c147144b0ef7f8cf8d0f151e04674b89
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/25/2020
ms.locfileid: "88821759"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="cd17d-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd17d-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="cd17d-104">4.6.0: August 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-105">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-106">Alle öffentlichen Cloudumgebungen geladen, wenn der Ermittlungsendpunkt keine standardmäßigen AzureCloud-Umgebungen oder anderen öffentlichen Umgebungen zurückgibt [Nr. 12633]</span><span class="sxs-lookup"><span data-stu-id="cd17d-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="cd17d-107">SubscriptionPolicies in „Get-AzSubscription“ verfügbar gemacht [Nr. 12551]</span><span class="sxs-lookup"><span data-stu-id="cd17d-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-108">Az.Automation</span></span>
* <span data-ttu-id="cd17d-109">Parameter „-RunOn“ zu „Set-AzAutomationWebhook“ hinzugefügt, um eine Hybrid Worker-Gruppe anzugeben</span><span class="sxs-lookup"><span data-stu-id="cd17d-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-110">Az.Compute</span></span>
* <span data-ttu-id="cd17d-111">Parameter „-EncryptionAtHost“ zu „New-AzVm“, „New-AzVmss“, „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="cd17d-112">„SecurityProfile“ zu Rückgabeobjekt „Get-AzVM“ und „Get-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="cd17d-113">Switch „-InstanceView“ als optionalen Parameter zu „Get-AzHostGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="cd17d-114">Neues Cmdlet „Invoke-AzVmPatchAssessment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-115">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-116">Fehlende Eigenschaften zur PSPipelineRun-Klasse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-117">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-118">Unterstützung für das Erstellen eines Clusters mit dem Feature für Verschlüsselung auf dem Host</span><span class="sxs-lookup"><span data-stu-id="cd17d-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-119">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-120">Warnmeldungen für geplante Deaktivierung des vorläufigen Löschens hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="cd17d-121">Warnmeldungen für die geplante Entfernung des Attributs „SecretValueText“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cd17d-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cd17d-122">Az.Maintenance</span></span>
* <span data-ttu-id="cd17d-123">Optionale zeitplanbezogene Felder zu „New-AzMaintenanceConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="cd17d-124">Neues Cmdlet für „Get-AzMaintenancePublicConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd17d-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-125">Az.ManagedServices</span></span>
* <span data-ttu-id="cd17d-126">Breaking Change-Warnungen zu Cmdlets für die Zuweisung und Definition von verwalteten Diensten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-127">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-128">Parametersatz in „Set-AzDiagnosticSetting“ zur Trennung der Aktivierung von Protokollen und Metriken erweitert [Nr. 12482]</span><span class="sxs-lookup"><span data-stu-id="cd17d-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="cd17d-129">Fehler für „Add-AzMetricAlertRuleV2“ behoben, der beim Abrufen einer Metrikwarnung aus der Pipeline auftrat</span><span class="sxs-lookup"><span data-stu-id="cd17d-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-130">Az.Resources</span></span>
* <span data-ttu-id="cd17d-131">Antwort auf „Get-AzPolicyAlias“ aktualisiert. Sie enthält nun Informationen dazu, ob der Alias von Azure Policy geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd17d-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="cd17d-132">Neues Cmdlet „Set-AzRoleAssignment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="cd17d-133">„Get-AzDeploymentManagementGroupWhatIfResult“ zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Verwaltungsgruppenbereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="cd17d-134">Neues Cmdlet „Get-AzTenantWhatIfResult“ zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Mandantenbereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="cd17d-135">Parameter „-WhatIf“ und „-Confirm“ für „New-AzManagementGroupDeployment“ und „New-AzTenantDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben</span><span class="sxs-lookup"><span data-stu-id="cd17d-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cd17d-136">Verhalten von „-WhatIf“ und „-Confirm“ für neue Bereitstellungs-Cmdlets korrigiert (abgestimmt auf „False“ und</span><span class="sxs-lookup"><span data-stu-id="cd17d-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="cd17d-137">Serialisierungsfehler für „-TemplateObject“ und „TemplateParameterObject“ behoben [Nr. 1528] [Nr. 6292]</span><span class="sxs-lookup"><span data-stu-id="cd17d-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="cd17d-138">Breaking Change-Attribut zu „Get-AzResourceGroupDeploymentOperation“ für anstehende Ausgabetypänderung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd17d-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-139">Az.SignalR</span></span>
* <span data-ttu-id="cd17d-140">Fehler in Hilfedateien für „Restart-AzSignalR“ und „Update-AzSignalR behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="cd17d-141">Cmdlets „Update-AzSignalRNetworkAcl“ und „Set-AzSignalRUpstream“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-142">Az.Storage</span></span>
* <span data-ttu-id="cd17d-143">Unterstützung für die Beschleunigung von Blobabfragen</span><span class="sxs-lookup"><span data-stu-id="cd17d-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="cd17d-144">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="cd17d-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="cd17d-145">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="cd17d-146">Hilfedatei aktualisiert, ausführlichere Beschreibung hinzugefügt und Tippfehler korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="cd17d-147">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="cd17d-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="cd17d-148">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="cd17d-149">Fehler beim Blobdownload behoben, der auftrat, wenn das zugehörige Unterverzeichnis nicht vorhanden ist [Nr. 12592]</span><span class="sxs-lookup"><span data-stu-id="cd17d-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="cd17d-150">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="cd17d-151">Unterstützung für das Festlegen/Abrufen/Entfernen der Objektreplikationsrichtlinie für Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="cd17d-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="cd17d-152">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="cd17d-153">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cd17d-154">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cd17d-155">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="cd17d-156">Unterstützung für das Aktivieren/Deaktivieren des Änderungsfeeds für den Blobdienst eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="cd17d-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cd17d-157">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="cd17d-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="cd17d-158">4.5.0: August 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-159">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-160">„Connect-AzAccount“ wurde aktualisiert und akzeptiert nun den Parameter „MaxContextPopulation“. [Nr. 9865]</span><span class="sxs-lookup"><span data-stu-id="cd17d-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="cd17d-161">SubscriptionClient-Version auf 2019-06-01 aktualisiert und Anzeigen von Mandantendomänen [Nr. 9838]</span><span class="sxs-lookup"><span data-stu-id="cd17d-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="cd17d-162">Unterstützung für Informationen des Home- und des managedBy-Mandanten des Abonnements</span><span class="sxs-lookup"><span data-stu-id="cd17d-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="cd17d-163">Modulname, Versionsinformationen in Telemetriedaten korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="cd17d-164">SqlDatabaseDnsSuffix und ServiceManagementUrl angepasst, wenn Umgebungsmetadatenendpunkt inkompatiblen Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="cd17d-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-165">Az.Aks</span></span>
* <span data-ttu-id="cd17d-166">„ClientIdAndSecret“ bis „ServicePrincipalIdAndSecret“ entfernt und „ClientIdAndSecret“ als Alias festgelegt [Nr. 12381].</span><span class="sxs-lookup"><span data-stu-id="cd17d-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="cd17d-167">„Get-AzAks“/„New-AzAks“/“Remove-AzAks“/„Set-AzAks“ bis „Get-AzAksCluster“/„New-AzAksCluster“/„Remove-AzAksCluster“/„Set-AzAksCluster“ entfernt und ursprüngliche Cmdlets als Alias festgelegt [Nr. 12373].</span><span class="sxs-lookup"><span data-stu-id="cd17d-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-168">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-169">Neues Cmdlet „Add-AzApiManagementApiToGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-170">Neues Cmdlet „Get-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-171">Neues Cmdlet „Get-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd17d-172">Neues Cmdlet „Get-AzApiManagementGatewayKey“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="cd17d-173">Neues Cmdlet „New-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-174">Neues Cmdlet „New-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd17d-175">Neues Cmdlet „New-AzApiManagementResourceLocationObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="cd17d-176">Neues Cmdlet „Remove-AzApiManagementApiFromGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-177">Neues Cmdlet „Remove-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-178">Neues Cmdlet „Remove-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cd17d-179">Neues Cmdlet „Update-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cd17d-180">Neuer optionaler Parameter „[-GatewayId]“ zum Cmdlet „Get-AzApiManagementApi“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-182">„Deny“ speziell als NetworkRules-Standardaktion verwendet</span><span class="sxs-lookup"><span data-stu-id="cd17d-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-183">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-184">Problem behoben, aufgrund dessen eine Ausnahme ausgelöst wird, wenn Enum.Parse versucht, einen NULL-Wert in Enumerationswerte vom Typ „Enabled“ oder „Disabled“ umzuwandeln [Nr. 12344]</span><span class="sxs-lookup"><span data-stu-id="cd17d-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-185">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-186">Unterstützung für das Erstellen eines Clusters mit dem Feature für Verschlüsselung während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="cd17d-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="cd17d-187">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cd17d-188">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cd17d-189">Unterstützung für das Erstellen eines Clusters mit der Funktion für private Links:</span><span class="sxs-lookup"><span data-stu-id="cd17d-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="cd17d-190">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cd17d-191">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cd17d-192">Beim Aufruf von „New-AzHDInsightCluster“ oder „Get-AzHDInsightCluster“ werden Informationen zum virtuellen Netzwerk zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-193">Az.Network</span></span>
* <span data-ttu-id="cd17d-194">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cd17d-195">Nonbreaking Changes hinzugefügt: PeerAddressType-Funktion für privates Peering in „Remove-AzExpressRouteCircutPeeringConfig“</span><span class="sxs-lookup"><span data-stu-id="cd17d-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="cd17d-196">Code geändert, um die Groß-/Kleinschreibung für die Parameter „AddressPrefixType“ und „PeerAddressType“ zu ignorieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="cd17d-197">Warnmeldung für „New-AzLoadBalancerFrontendIpConfig“, „New-AzPublicIpAddress“ und „New-AzPublicIpPrefix“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-199">Option „-ForceDelete“ für „Remove-AzOperationalInsightsworkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="cd17d-200">Neues Cmdlet „Get-AzOperationalInsightsDeletedWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="cd17d-201">Neues Cmdlet „Restore-AzOperationalInsightsWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-203">Ermittlung von Azure Backup-Containern/-Elementen verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-204">Az.Resources</span></span>
* <span data-ttu-id="cd17d-205">Eigenschaften „Condition“, „ConditionVersion“ und „Description“ zu „New-AzRoleAssignment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="cd17d-206">Dies enthielt alle relevanten Änderungen an den Datenmodellen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-207">Az.Sql</span></span>
* <span data-ttu-id="cd17d-208">Potenzieller Fehler aufgrund der Nichtbeachtung von Groß-/Kleinschreibung beim Servernamen in „New-AzSqlServer“ und „Set-AzSqlServer“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cd17d-209">Fehler behoben, aufgrund dessen in „New-AzSqlDatabaseSecondary“ ein falscher Datenbankname für eine vorhandene Datenbank zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-210">Az.Storage</span></span>
* <span data-ttu-id="cd17d-211">Erstellen von Container-/Blob-SAS-Token mit neuer Berechtigung x,t unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="cd17d-212">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="cd17d-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="cd17d-213">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="cd17d-214">Erstellen von Konto-SAS-Token mit neuer Berechtigung x,t,f unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="cd17d-215">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="cd17d-216">Abrufen der Nutzung einer einzelnen Dateifreigabe unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="cd17d-217">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="cd17d-218">4.4.0 – Juli 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-219">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-220">Neues Cmdlet „Invoke-AzRestMethod“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="cd17d-221">Ein Problem wurde behoben, das Authentifizierungsfehler in Szenarien mit mehreren Prozessen verursachen konnte, z. B. beim Ausführen mehrerer Azure PowerShell-Cmdlets mithilfe von „Start-Job“ [Nr. 9448].</span><span class="sxs-lookup"><span data-stu-id="cd17d-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-222">Az.Aks</span></span>
* <span data-ttu-id="cd17d-223">Fehler behoben: „Get-AzAks“ ruft nicht alle Cluster ab [Nr. 12296]</span><span class="sxs-lookup"><span data-stu-id="cd17d-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd17d-225">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-226">Az.Automation</span></span>
* <span data-ttu-id="cd17d-227">Das Problem wurde behoben, dass die Zeichenfolge mit Escapezeichen nicht in das JSON-Objekt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd17d-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-228">Az.Compute</span></span>
* <span data-ttu-id="cd17d-229">Beim Verwenden von „New-azvmss“ ohne die Imageversion „latest“ wurde eine Warnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-230">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-231">Globale Parameter zu Data Factory hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd17d-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd17d-232">Az.EventGrid</span></span>
* <span data-ttu-id="cd17d-233">Zur Verwendung der API-Version 2020-06-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="cd17d-234">Neue Funktionen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-234">Added new features:</span></span>
    - <span data-ttu-id="cd17d-235">Eingabezuordnung</span><span class="sxs-lookup"><span data-stu-id="cd17d-235">Input mapping</span></span>
    - <span data-ttu-id="cd17d-236">Schema für Ereignisbereitstellung</span><span class="sxs-lookup"><span data-stu-id="cd17d-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="cd17d-237">Private Link</span><span class="sxs-lookup"><span data-stu-id="cd17d-237">Private Link</span></span>
    - <span data-ttu-id="cd17d-238">Cloud Event V10-Schema</span><span class="sxs-lookup"><span data-stu-id="cd17d-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="cd17d-239">Service Bus-Thema as Ziel</span><span class="sxs-lookup"><span data-stu-id="cd17d-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="cd17d-240">Azure-Funktion als Ziel</span><span class="sxs-lookup"><span data-stu-id="cd17d-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="cd17d-241">WebHook-Batchverarbeitung</span><span class="sxs-lookup"><span data-stu-id="cd17d-241">WebHook Batching</span></span>
    - <span data-ttu-id="cd17d-242">Sicherer Webhook (AAD-Unterstützung)</span><span class="sxs-lookup"><span data-stu-id="cd17d-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="cd17d-243">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="cd17d-243">IpFiltering</span></span>
* <span data-ttu-id="cd17d-244">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="cd17d-245">„New-AzEventGridSubscription“/„Update-AzEventGridSubscription“:</span><span class="sxs-lookup"><span data-stu-id="cd17d-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="cd17d-246">Neue optionale Parameter zur Unterstützung der Webhook-Batchverarbeitung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="cd17d-247">Neue optionale Parameter zur Unterstützung der Batchverarbeitung gesicherter Webhooks mithilfe von AAD hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="cd17d-248">Neue Enumeration für den EndpointType-Parameter hinzufügen, um das Azure-Funktions-und Service Bus-Thema als neue Ziele zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="cd17d-249">Neuen optionalen Parameter für das Zustellungsschema hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="cd17d-250">„New-AzEventGridTopic“/„Update-AzEventGridTopic“ und „New-AzEventGridDomain“/„Update-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="cd17d-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cd17d-251">Neue optionale Parameter zur Unterstützung von IpFiltering hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="cd17d-252">„New-AzEventGridTopic“/„New-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="cd17d-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cd17d-253">Neue optionale Parameter zur Unterstützung von Eingabezuordnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-254">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-255">Modul zur Verwendung von API 2020-05-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="cd17d-256">Unterstützung für private Links für Storage-, Keyvault- und Web App Service-Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-257">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-258">Erstellen eines Clusters mit ADLSGen1/2-Speicher in nationalen Clouds unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-259">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-260">Fehler für „Get-AzDiagnosticSetting“ behoben, wenn Metriken oder Protokolle NULL sind [Nr. 12272]</span><span class="sxs-lookup"><span data-stu-id="cd17d-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-261">Az.Network</span></span>
* <span data-ttu-id="cd17d-262">Austausch von Parametern in VWan-HubVnet-Verbindung-korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="cd17d-263">Neue Cmdlets für Sites von virtuellen Azure-Netzwerkgeräten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="cd17d-264">„Get-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="cd17d-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd17d-265">„New-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="cd17d-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd17d-266">„Remove-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="cd17d-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd17d-267">„Update-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="cd17d-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cd17d-268">„New-AzOffice365PolicyProperty“</span><span class="sxs-lookup"><span data-stu-id="cd17d-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="cd17d-269">Neue Cmdlets für virtuelle Azure-Netzwerkgeräte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="cd17d-270">„Get-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="cd17d-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd17d-271">„New-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="cd17d-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd17d-272">„Remove-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="cd17d-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd17d-273">„Update-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="cd17d-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cd17d-274">„Get-AzNetworkVirtualApplianceSku“</span><span class="sxs-lookup"><span data-stu-id="cd17d-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="cd17d-275">„New-AzVirtualApplianceSkuProperty“</span><span class="sxs-lookup"><span data-stu-id="cd17d-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="cd17d-276">Onboarding für Application Gateway für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="cd17d-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cd17d-277">Onboarding für StorageSync für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="cd17d-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cd17d-278">Onboarding für SignalR für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="cd17d-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-280">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="cd17d-281">Azure Backup hat Cmdlets optimiert, um den Text genauer zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="cd17d-282">Azure Backup hat Unterstützung für das Abrufen von MAB-Agent-Aufträgen mithilfe des Cmdlets „Get-AzRecoveryServicesBackupJob“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-283">Az.Resources</span></span>
* <span data-ttu-id="cd17d-284">„Save-azresourcegroupdeploymenttemplate“ auf Verwendung des SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="cd17d-285">Cmdlet „Unregister-AzResourceProvider“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-286">Az.Sql</span></span>
* <span data-ttu-id="cd17d-287">Unterstützung für Dienstprinzipal und Gastbenutzer im Cmdlet „Set-AzSqlInstanceActiveDirectoryAdministrator“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="cd17d-288">Problem in Data Classification-Cmdlets behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="cd17d-289">Unterstützung für Azure SQL Managed Instance-Failover hinzugefügt: „Invoke-AzSqlInstanceFailover“</span><span class="sxs-lookup"><span data-stu-id="cd17d-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-290">Az.Storage</span></span>
* <span data-ttu-id="cd17d-291">Problem behoben, dass UserAgent für einige Datenebenen-Cmdlets nicht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cd17d-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="cd17d-292">Erstellen/Aktualisieren eines Storage-Kontos mit „MinimumTlsVersion“ und „AllowBlobPublicAccess“ unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="cd17d-293">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cd17d-294">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-295">Aktivieren/Deaktivieren der Versionsverwaltung für Blobdienst eines Storage-Kontos unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cd17d-296">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="cd17d-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cd17d-297">Auflisten von Blobs mit Blobversionen unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="cd17d-298">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="cd17d-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="cd17d-299">Abrufen/Entfernen einer einzelnen Blob-Momentaufnahme oder Blobversion unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="cd17d-300">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="cd17d-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="cd17d-301">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="cd17d-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="cd17d-302">Pipeline aus Blobobjekt unterstützen, das aus Azure.Storage.Blobs V12 generiert wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="cd17d-303">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cd17d-304">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="cd17d-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="cd17d-305">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="cd17d-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="cd17d-306">„Set-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cd17d-307">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="cd17d-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd17d-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd17d-308">Az.StorageSync</span></span>
* <span data-ttu-id="cd17d-309">Neue Version von StorageSync SDK für ApiVersion 2020-03-01 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="cd17d-310">Cmdlet „Update Storage Sync Service“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="cd17d-311">„Set-AzStorageSyncService“</span><span class="sxs-lookup"><span data-stu-id="cd17d-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="cd17d-312">„IncomingTrafficPolicy“ und „PrivateEndpointConnections“ zu StorageSyncService-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-313">Az.Websites</span></span>
* <span data-ttu-id="cd17d-314">Unterstützung zur Durchführung von Vorgängen für Slots hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="cd17d-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="cd17d-315">4.3.0 – Juni 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-316">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-317">Standardmäßige Unterstützung der Einstellung der Erkennungsumgebung und das Hinzufügen der Umgebung über „Add-AzEnvironment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="cd17d-318">Aktualisieren von vorgeladenen Assemblys [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="cd17d-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="cd17d-319">Assembly „Azure.Core“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="cd17d-320">Fehler behoben, der dazu führen konnte, dass „Connect-AzAccount“ in der Multithread-Ausführung fehlschlägt [#11201]</span><span class="sxs-lookup"><span data-stu-id="cd17d-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-321">Az.Aks</span></span>
* <span data-ttu-id="cd17d-322">Ersetzen der Verwendung der alten [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) durch Aufrufe der [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials)- und [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)-APIs</span><span class="sxs-lookup"><span data-stu-id="cd17d-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-323">Az.Batch</span></span>
* <span data-ttu-id="cd17d-324">Az.Batch für die Verwendung der Microsoft.Azure.Management.Batch-SDK-Version auf 11.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="cd17d-325">Möglichkeit zum Festlegen der BatchAccount-Identität im Cmdlet „New-AzBatchAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-327">Anzeige von Kontofunktionen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="cd17d-328">Ändern von PublicNetworkAccess wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-329">Az.Compute</span></span>
* <span data-ttu-id="cd17d-330">Parameter „SimulateEviction“ wurde den Cmdlets „Set-AzVM“ und „Set-AzVmssVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="cd17d-331">„Premium_LRS“ wurde zur Argumentvervollständigung des StorageAccountType-Parameters für das Cmdlet „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="cd17d-332">Unterstatus zu VMCustomScriptExtension hinzugefügt [#11297]</span><span class="sxs-lookup"><span data-stu-id="cd17d-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="cd17d-333">„Delete“ wurde zur Argumentvervollständigung des EvictionPolicy-Parameters für die Cmdlets „New-AzVM“ und „New-AzVMConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="cd17d-334">Name der neuen VM-Erweiterung für SAP korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-335">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-336">ADF .Net-SDK-Version auf 4.9.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-337">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-338">Parameter der verwalteten Identität zu Cmdlets „New-AzEventHubNamespace“ und „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd17d-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd17d-339">Az.Functions</span></span>
* <span data-ttu-id="cd17d-340">Unterstützung zum Erstellen von PowerShell 7.0- und Java 11-Funktions-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-341">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-342">Listenhosts unterstützt und bestimmte Hosts des HDInsight-Clusters neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd17d-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd17d-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd17d-344">SDK-Version auf 1.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="cd17d-345">Unterstützung für Exporteinstellungen und verwaltete Identität hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-346">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-347">Eingabeobjektparameter für „Set-AzActivityLogAlert“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="cd17d-348">InputObject-Parameter für „Set-AzActionGroup“ korrigiert [#10868]</span><span class="sxs-lookup"><span data-stu-id="cd17d-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-349">Az.Network</span></span>
* <span data-ttu-id="cd17d-350">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cd17d-351">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cd17d-352">„New-AzFirewallPolicyDnsSetting“</span><span class="sxs-lookup"><span data-stu-id="cd17d-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="cd17d-353">Unterstützung für Ziel-FQDN in Netzwerkregeln für Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="cd17d-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="cd17d-354">Unterstützung für Back-End-Adresspool-Vorgänge hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="cd17d-355">„New-AzLoadBalancerBackendAddressConfig“</span><span class="sxs-lookup"><span data-stu-id="cd17d-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="cd17d-356">„New-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="cd17d-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd17d-357">„Set-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="cd17d-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd17d-358">„Remove-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="cd17d-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cd17d-359">„Get-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="cd17d-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="cd17d-360">Namensvalidierung für „New-AzIpGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="cd17d-361">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cd17d-362">„New-AzFirewallPolicyThreatIntelWhitelist“</span><span class="sxs-lookup"><span data-stu-id="cd17d-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="cd17d-363">Folgende Befehle für das Feature aktualisiert: Festlegen/Entfernen von benutzerdefinierten DNS-Servern auf „VirtualWan P2SVpnGateway“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="cd17d-364">„New-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="cd17d-365">„Update-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="cd17d-366">„Update-AzVpnGateway“ aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="cd17d-367">Der optionale Parameter „-BgpPeeringAddress“ wurde hinzugefügt, damit Kunden ihre benutzerdefinierten BGSs angeben können, die auf „VpnGateway“ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="cd17d-368">Neues Cmdlet hinzugefügt, um das Zurücksetzen des Routingstatus einer VirtualHub-Ressource zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="cd17d-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="cd17d-369">„Reset-AzHubRouter“</span><span class="sxs-lookup"><span data-stu-id="cd17d-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="cd17d-370">Folgendes wurde basierend auf der aktuellen Swagger-Änderung für die Firewallrichtlinie aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="cd17d-371">Namen für „RuleGroup“, „RuleCollectionGroup“ und „RuleType“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="cd17d-372">Unterstützung für NAT-Regelsammlungen der Firewallrichtlinie zur Unterstützung mehrerer NAT-Regelsammlungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="cd17d-373">[Breaking Change] Obligatorischer Parameter „SourceIpGroup“ für „New-AzFirewallPolicyApplicationRule“ und „New-AzFirewallPolicyNetworkRule“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="cd17d-374">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cd17d-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cd17d-375">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cd17d-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cd17d-376">[Breaking Change] Obligatorische Parameter entfernt: „TranslatedAddress“, „TranslatedPort“ für „New-AzFirewallPolicyNatRuleCollection“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="cd17d-377">Neue Cmdlets zur Unterstützung von „PrivateLink“ auf Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="cd17d-378">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd17d-379">„Get-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd17d-380">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd17d-381">„Set-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd17d-382">„Remove-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cd17d-383">„New-AzApplicationGatewayPrivateLinkIpConfiguration“</span><span class="sxs-lookup"><span data-stu-id="cd17d-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="cd17d-384">Neue Cmdlets für untergeordnete Ressource „HubRouteTables“ von „VirtualHub“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="cd17d-385">„New-AzVHubRoute“</span><span class="sxs-lookup"><span data-stu-id="cd17d-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="cd17d-386">„New-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd17d-387">„Get-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd17d-388">„Update-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cd17d-389">„Remove-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="cd17d-390">Vorhandene Cmdlets aktualisiert, sodass sie den optionalen Eingabeparameter „RoutingConfiguration“ für benutzerdefiniertes Routing in „VirtualWan“ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="cd17d-391">„New-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="cd17d-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cd17d-392">„Set-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="cd17d-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cd17d-393">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd17d-394">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd17d-395">„New-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="cd17d-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="cd17d-396">„Update-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="cd17d-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="cd17d-397">„New-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="cd17d-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="cd17d-398">„Update-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="cd17d-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-400">Fehler behoben: „PSWorkspace“ implementiert „IOperationalInsightsWorkspace“ nicht [#12135]</span><span class="sxs-lookup"><span data-stu-id="cd17d-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="cd17d-401">„pergb2018“ wurde dem gültigen Satz des Parameters „Sku“ in „Set-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="cd17d-402">Der Alias „FunctionParameters“ für den Parameter „FunctionParameter“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="cd17d-403">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cd17d-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cd17d-404">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cd17d-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-406">Azure Backup hat Unterstützung für das Abrufen von MAB-Elementen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="cd17d-407">Azure Site Recovery unterstützt Datenträgertyp „StandardSSD_LRS“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-408">Az.Resources</span></span>
* <span data-ttu-id="cd17d-409">„UsageLocation“, „GivenName“, „Surname“, „AccountEnabled“, „MailNickname“, „Mail“ in „PSADUser“ hinzugefügt [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="cd17d-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="cd17d-410">Problem behoben, dass „-Mail“ für „Get-AzADUser“ nicht funktioniert [#11981]</span><span class="sxs-lookup"><span data-stu-id="cd17d-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="cd17d-411">Parameter „-ExcludeChangeType“ zu „Get-AzDeploymentWhatIfResult“ und „Get-AzResourceGroupDeploymentWhatIfResult“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="cd17d-412">Parameter „-WhatIfExcludeChangeType“ zu „New-AzDeployment“ und „New-AzResourceGroupDeployment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="cd17d-413">Cmdlets von „Test-Az\*Deployment“, sodass bessere Fehlermeldungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="cd17d-414">Hilfemeldung für Parameter „-Name“ der Cmdlets „deployment create“ und „What-If“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-415">Az.Sql</span></span>
* <span data-ttu-id="cd17d-416">Unterstützung für Dienstprinzipal für Cmdlet „Set SQL Server Azure Active Directory Admin“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="cd17d-417">Synchronisierungsproblem in Datenklassifizierungs-Cmdlets wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="cd17d-418">Suchen von Benutzern nach E-Mail wird für „Set-AzSqlServerActiveDirectoryAdministrator“ unterstützt [#12192]</span><span class="sxs-lookup"><span data-stu-id="cd17d-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-419">Az.Storage</span></span>
* <span data-ttu-id="cd17d-420">Erstellen eines Speicherkontos mit „RequireInfrastructureEncryption“ wird unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="cd17d-421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-422">Logik zum Laden von „Azure.Core to Az.Accounts“ verschoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-423">Az.Websites</span></span>
* <span data-ttu-id="cd17d-424">Schutz zum Löschen der erstellten Web-App hinzugefügt, wenn die Wiederherstellung in „Restore-AzDeletedWebApp“ fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cd17d-425">„SourceWebApp.Location“ für „New-AzWebApp“ und „New-AzWebAppSlot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="cd17d-426">Fehler behoben, der das Ändern von Containereinstellungen in „Set-AzWebApp“ und „Set-AzWebAppSlot“ verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="cd17d-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="cd17d-427">Fehler beim Abrufen von „SiteConfig“ behoben, wenn „-Name“ für „Get-AzWebApp“ nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="cd17d-428">Unterstützung zum Erstellen von ASP für Linux-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="cd17d-429">Ausnahmen für den Ressourcengruppen übergreifenden Klonvorgang hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="cd17d-430">4.2.0: Juni 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-431">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-432">Problem behoben, das unter Umständen dazu geführt hat, dass Az Protokolle in Azure Automation- oder PowerShell-Aufträgen übersprungen hat [Nr. 11492]</span><span class="sxs-lookup"><span data-stu-id="cd17d-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd17d-434">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-435">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-436">Assemblyversion der Dienstverwaltungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cd17d-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd17d-437">Az.Billing</span></span>
* <span data-ttu-id="cd17d-438">Assemblyversion der Nutzungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-440">Unterstützung des PrivateEndpoint- und des PublicNetworkAccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="cd17d-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-441">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-442">Assemblyversion der Data Factory v2-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="cd17d-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-443">Az.DataShare</span></span>
* <span data-ttu-id="cd17d-444">Allgemeine Verfügbarkeit des Moduls „Az.DataShare“</span><span class="sxs-lookup"><span data-stu-id="cd17d-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cd17d-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cd17d-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cd17d-446">Allgemeine Verfügbarkeit des Moduls „Az.DesktopVirtualization“</span><span class="sxs-lookup"><span data-stu-id="cd17d-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-448">SDK auf 0.21.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="cd17d-449">Optionale Parameter hinzugefügt zu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="cd17d-450">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cd17d-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cd17d-451">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cd17d-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-453">Beispiel 3 für „Start-AzPolicyComplianceScan“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cd17d-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cd17d-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cd17d-455">Assemblyversion der PowerBI-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cd17d-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cd17d-456">Az.PrivateDns</span></span>
* <span data-ttu-id="cd17d-457">Formatierung der ausführlichen Ausgabezeichenfolge für „Remove-AzPrivateDnsRecordSet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-459">Azure Site Recovery-Unterstützung für die Erstellung eines Wiederherstellungsplans für die Replikation zwischen Zonen per XML-Eingabe</span><span class="sxs-lookup"><span data-stu-id="cd17d-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="cd17d-460">Assemblyversion der SiteRecovery- und Backup-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-461">Az.Resources</span></span>
* <span data-ttu-id="cd17d-462">Tail-Parameter zu den Cmdlets „Get-AzDeploymentScriptLog“ und „Save-AzDeploymentScriptLog“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="cd17d-463">Die Output-Eigenschaft wurde formatiert und wird nun in der Ausgabe des Cmdlets „Get-AzDeploymentScript“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="cd17d-464">Parameter „-DeploymentScriptInputObject“ in „-DeploymentScriptObject“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="cd17d-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="cd17d-465">Fehlender Datei-/Zielname in Cmdlet-Meldungen korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="cd17d-466">Assemblyversion der Resource Manager- und Tags-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-467">Az.Sql</span></span>
* <span data-ttu-id="cd17d-468">„UsePrivateLinkConnection“ zu „New-AzSqlSyncGroup“, „Update-AzSqlSyncGroup“, „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cd17d-469">„SyncMemberAzureDatabaseResourceId“ zu „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cd17d-470">Unterstützung für die Gastbenutzersuche zum SQL Server-Cmdlet für den Azure Active Directory-Administrator hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-471">Az.Storage</span></span>
* <span data-ttu-id="cd17d-472">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="cd17d-473">4.1.0 – Mai 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cd17d-474">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="cd17d-474">Highlights since the last release</span></span>
* <span data-ttu-id="cd17d-475">Unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cd17d-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="cd17d-476">Allgemeine Verfügbarkeit von Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd17d-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="cd17d-477">Veröffentlichung von Hauptversionen von Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources und Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-478">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-479">„Add-AzEnvironment“ und „Set-AzEnvironment“ akzeptieren jetzt die Parameter „AzureSynapseAnalyticsEndpointResourceId“ und „AzureSynapseAnalyticsEndpointSuffix“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="cd17d-480">Assemblys zu Azure.Core wurden Az.Accounts hinzugefügt. Unterstützte PowerShell-Plattformen sind u. a. Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="cd17d-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-481">Az.Aks</span></span>
* <span data-ttu-id="cd17d-482">API-Version wurde auf 2019-10-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="cd17d-483">Unterstützung für die Erstellung von AKS mit einem Windows-Container</span><span class="sxs-lookup"><span data-stu-id="cd17d-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="cd17d-484">Neu verfügbare Cmdlets: „New-AzAksNodePool“, „Update-AzAksNodePool“, „Remove-AzAksNodePool“, „Get-AzAksNodePool“, „Install-AzAksKubectl“, „Get-AzAksVersion“</span><span class="sxs-lookup"><span data-stu-id="cd17d-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-485">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-486">„New-AzApiManagement“ und „Set-AzApiManagement“: Parameter [-AssignIdentity] wurde in [-SystemAssignedIdentity] umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="cd17d-487">„New-AzApiManagement“ und „Set-AzApiManagement“: Neuer Parameter hinzugefügt: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="cd17d-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="cd17d-488">„Get-AzApiManagementProperty“ wurde in „Get-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd17d-489">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd17d-490">„New-AzApiManagementProperty“ wurde in „New-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd17d-491">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="cd17d-492">„Set-AzApiManagementProperty“ wurde in „Set-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd17d-493">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd17d-494">„Remove-AzApiManagementProperty“ wurde in „Remove-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cd17d-495">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cd17d-496">Neues Cmdlet „Get-AzApiManagementAuthorizationServerClientSecret“ hinzugefügt. „Get-AzApiManagementAuthorizationServer“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="cd17d-497">Neues Cmdlet „Get-AzApiManagementNamedValueSecretValue“ hinzugefügt. „Get-AzApiManagementNamedValue“ gibt keinen Geheimniswert zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="cd17d-498">Neues Cmdlet „Get-AzApiManagementOpenIdConnectProviderClientSecret“ hinzugefügt. „Get-AzApiManagementOpenIdConnectProvider“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="cd17d-499">Neues Cmdlet „Get-AzApiManagementSubscriptionKey“ hinzugefügt. „Get-AzApiManagementSubscription“ gibt keine Abonnementschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="cd17d-500">Neues Cmdlet „Get-AzApiManagementTenantAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="cd17d-501">Neues Cmdlet „Get-AzApiManagementTenantGitAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantGitAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cd17d-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cd17d-503">Parameter hinzugefügt: „RetentionInDays“, „PublicNetworkAccessForIngestion“, „PublicNetworkAccessForQuery“ für „New-AzApplicationInsights“</span><span class="sxs-lookup"><span data-stu-id="cd17d-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="cd17d-504">Cmdlet „Update-AzApplicationInsights“ erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="cd17d-505">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-506">Az.Batch</span></span>
* <span data-ttu-id="cd17d-507">Az.Batch für die Verwendung der Microsoft.Azure.Batch-SDK-Version 13.0.0 und der Microsoft.Azure.Management.Batch-SDK-Version 9.0.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="cd17d-508">Die Möglichkeit zum Auswählen der Art des hinzugefügten Zertifikats mithilfe des neuen Parameters „-CertificateKind“ wurde zu „New-AzBatchCertificate“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="cd17d-509">Eigenschaft „ApplicationPackages“ aus „PSApplication“ entfernt, die bislang immer „“ war.</span><span class="sxs-lookup"><span data-stu-id="cd17d-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="cd17d-510">Die spezifischen Pakete in einer Anwendung können jetzt mit „Get-AzBatchApplicationPackage“ abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="cd17d-511">Beispiel: „Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication“</span><span class="sxs-lookup"><span data-stu-id="cd17d-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="cd17d-512">Beim Erstellen eines Pools mit „New-AzBatchPool“ kann die Eigenschaft „VirtualMachineImageId“ von „PSImageReference“ jetzt nur auf ein Bild in einer Shared Image Gallery verweisen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="cd17d-513">Wenn Sie einen Pool mit „New-AzBatchPool“ erstellen, kann der Pool mit der Eigenschaft „PublicIPAddressConfiguration“ von „PSNetworkConfiguration“ ohne eine öffentliche IP-Adresse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="cd17d-514">Die Eigenschaft „PublicIPs“ von „PSNetworkConfiguration“ wurde ebenfalls in „PSPublicIPAddressConfiguration“ verschoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="cd17d-515">Diese Eigenschaft kann nur angegeben werden, wenn „IPAddressProvisioningType“ den Wert „UserManaged“ hat.</span><span class="sxs-lookup"><span data-stu-id="cd17d-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-516">Az.Compute</span></span>
* <span data-ttu-id="cd17d-517">HostId-Parameter zum Cmdlet „Update-AzVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="cd17d-518">Hilfedokumente für die Cmdlets „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVmss“, „Set-AzVMOperatingSystem“ und „Set-AzVmssOsProfile“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="cd17d-519">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="cd17d-519">Breaking changes</span></span>
    - <span data-ttu-id="cd17d-520">Der FilterExpression-Parameter wurde aus dem Cmdlet „Get-AzVMImage“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="cd17d-521">Der AssignIdentity-Parameter wurde aus den Cmdlets „New-AzVmssConfig“, „New-AzVMConfig“ und „Update-AzVM“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="cd17d-522">AutomaticRepairMaxInstanceRepairsPercent wurde aus den Cmdlets „New-AzVmssConfig“ und „Update-AzVmss“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="cd17d-523">Die Eigenschaften AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus und VirtualMachineScaleSetsColocationStatus wurden aus ProximityPlacementGroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="cd17d-524">Die Eigenschaft MaxInstanceRepairsPercent wurde aus AutomaticRepairsPolicy entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="cd17d-525">Die Typen von AvailabilitySets, VirtualMachines und VirtualMachineScaleSets wurden von IList<SubResource> in IList<SubResourceWithColocationStatus> geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="cd17d-526">Die Beschreibung für das Cmdlet „Get-AzVM“ wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-527">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-528">CRUD von Datenfluss-Laufzeiteigenschaften in Managed IR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-529">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-530">Neue Cmdlets zum Erstellen, Aktualisieren, Abrufen und Löschen von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cd17d-531">Hilfs-Cmdlets für die Erstellung von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cd17d-532">Regelmodulverweis auf Front Door-Routingregelobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="cd17d-533">Private Link-Parameter zum Front Door-Back-End-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cd17d-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cd17d-534">Az.Functions</span></span>
* <span data-ttu-id="cd17d-535">Allgemeine Verfügbarkeit des Moduls „Az.Functions“</span><span class="sxs-lookup"><span data-stu-id="cd17d-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-536">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-537">Datenträgerverschlüsselung mit kundenseitig verwalteten Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd17d-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd17d-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd17d-539">Zugriffsrichtlinien verwenden nicht mehr den aktuellen Prinzipal als Standard.</span><span class="sxs-lookup"><span data-stu-id="cd17d-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-540">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-541">Cmdlet zum Aufrufen einer Abfrage in einem IoT-Hub zum Abrufen von Informationen mithilfe einer SQL-ähnlichen Sprache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="cd17d-542">Problem behoben, dass „Add-AzIotHubDevice“ kein Edge-aktiviertes Gerät ohne untergeordnete Geräte erstellen konnte. [#11597]</span><span class="sxs-lookup"><span data-stu-id="cd17d-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="cd17d-543">Cmdlet zum Generieren eines SAS-Tokens für IoT-Hub, -Gerät oder -Modul hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="cd17d-544">Cmdlet zum Aufrufen der Konfigurationsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="cd17d-545">Verwalten der automatischen skalierbaren Bereitstellung von IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="cd17d-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="cd17d-546">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-546">New cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-547">„Add-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd17d-548">„Get-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd17d-549">„Remove-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cd17d-550">„Set-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="cd17d-551">Cmdlet zum Hinzufügen einer IoT Edge-Bereitstellungsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="cd17d-552">Cmdlet zum Anwenden des Konfigurationsinhalts auf das angegebene Edge-Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-553">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-554">Zwei Aliase entfernt: „New-AzKeyVaultCertificateAdministratorDetails“ und „New-AzKeyVaultCertificateOrganizationDetails“</span><span class="sxs-lookup"><span data-stu-id="cd17d-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="cd17d-555">Vorläufiges Löschen ist beim Erstellen eines Schlüsseltresors standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="cd17d-556">Netzwerkregeln können so festgelegt werden, dass der Zugriff von bestimmten Netzwerkstandorten beim Erstellen eines Schlüsseltresors gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="cd17d-557">Unterstützung für BYOK (Bring Your Own Key) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="cd17d-558">„Add-AzKeyVaultKey“ unterstützt die Erstellung eines Schlüsselaustauschschlüssels.</span><span class="sxs-lookup"><span data-stu-id="cd17d-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="cd17d-559">„Get-AzKeyVaultKey“ unterstützt das Herunterladen eines öffentlichen Schlüssels im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="cd17d-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="cd17d-560">Abschnitt „KeyOps“ der Hilfedokumentation zu „Add-AzKeyVaultKey“ wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-561">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-562">Fehler bei „Set-AzDiagnosticSettings“ behoben. Aufbewahrungsrichtlinie gilt nicht für alle Kategorien. [#11589]</span><span class="sxs-lookup"><span data-stu-id="cd17d-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="cd17d-563">WebTest-Verfügbarkeitskriterien für die Metrikwarnung V2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="cd17d-564">„New-AzMetricAlertRuleV2Criteria“: Option zum Erstellen der Webtest-Verfügbarkeitskriterien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="cd17d-565">„Add-AzMetricAlertRuleV2“: Neue Webtest-Verfügbarkeitskriterien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="cd17d-566">Redundante Definition für „RetentionPolicy“ in PSLogProfile entfernt. [#7608]</span><span class="sxs-lookup"><span data-stu-id="cd17d-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="cd17d-567">Redundante in PSEventData definierte Eigenschaften entfernt. [#11353]</span><span class="sxs-lookup"><span data-stu-id="cd17d-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="cd17d-568">„Get-AzLog“ in „Get-AzActivityLog“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-569">Az.Network</span></span>
* <span data-ttu-id="cd17d-570">Breaking Change-Attribut hinzugefügt als Benachrichtigung, dass sich das Standardverhalten der Zone ändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="cd17d-571">„New-AzPublicIpAddress“</span><span class="sxs-lookup"><span data-stu-id="cd17d-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="cd17d-572">„New-AzPublicIpPrefix“</span><span class="sxs-lookup"><span data-stu-id="cd17d-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="cd17d-573">„New-AzLoadBalancerFrontendIpConfig“</span><span class="sxs-lookup"><span data-stu-id="cd17d-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="cd17d-574">Unterstützung für die neue Ressource der obersten Ebene SecurityPartnerProvider hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="cd17d-575">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-575">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd17d-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd17d-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd17d-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd17d-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd17d-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cd17d-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="cd17d-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="cd17d-580">„RequiredZoneNames“ für „PSPrivateLinkResource“ und „GroupId“ für „PSPrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="cd17d-581">Falscher Typ des Parameters SuccessThresholdRoundTripTimeMs für New-AzNetworkWatcherConnectionMonitorTestConfigurationObject korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="cd17d-582">VirtualWan-Cmdlets aktualisiert, sodass der Standardwert des Arguments AllowVnetToVnetTraffic auf True festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="cd17d-583">„New-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="cd17d-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="cd17d-584">„Update-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="cd17d-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="cd17d-585">Neue Cmdlets zur Unterstützung der DNS-Zonengruppe für den privaten Endpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="cd17d-586">„New-AzPrivateDnsZoneConfig“</span><span class="sxs-lookup"><span data-stu-id="cd17d-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="cd17d-587">„Get-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="cd17d-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd17d-588">„New-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="cd17d-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd17d-589">„Set-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="cd17d-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cd17d-590">„Remove-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="cd17d-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="cd17d-591">Parameter „DNSEnableProxy“, „DNSRequireProxyForNetworkRules“ und „DNSServers“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="cd17d-592">Parameter „EnableDnsProxy“, „DnsProxyNotRequiredForNetworkRule“ und „DnsServer“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="cd17d-593">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd17d-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="cd17d-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-596">Legacycode zum Anwenden des neuen generierten SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="cd17d-597">Cmdlets aufgrund von veralteten APIs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cd17d-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="cd17d-598">„Get-AzOperationalInsightsSavedSearchResult“ (alias „Get-AzOperationalInsightsSavedSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="cd17d-599">„Get-AzOperationalInsightsSearchResult“ (alias „Get-AzOperationalInsightsSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="cd17d-600">„Get-AzOperationalInsightsLinkTarget“ (alias „Get-AzOperationalInsightsLinkTargets“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="cd17d-601">Parameter für „Set-AzOperationalInsightsWorkspace“ und „New-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="cd17d-602">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="cd17d-603">Cmdlets für Cluster und verknüpften Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-605">Azure Site Recovery: Unterstützung für den Schutz von virtuellen Computern der Näherungsplatzierungsgruppe für den Azure-zu-Azure-Anbieter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="cd17d-606">Azure Site Recovery: Unterstützung für die Replikation zwischen Zonen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="cd17d-607">Azure Backup: Unterstützung für die langfristige Aufbewahrung von Azure FileShare-Wiederherstellungspunkten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="cd17d-608">Azure Backup: Eigenschaften für den Ausschluss von Datenträgern zur Ausgabe des Cmdlet „Get-AzRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="cd17d-609">Privater Endpunkt für Tresoranmeldeinformationen für den Site Recovery-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-610">Az.Resources</span></span>
* <span data-ttu-id="cd17d-611">Warnmeldung zur verzögerten Ansicht beim Erstellen einer neuen Rollendefinition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="cd17d-612">Richtlinien-Cmdlets geändert, sodass sie stark typisierte Objekte ausgeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="cd17d-613">Parameter „-TenantLevel“ zum Cmdlet „Get-AzResourceLock“ hinzugefügt. [#11335]</span><span class="sxs-lookup"><span data-stu-id="cd17d-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="cd17d-614">„Remove-AzResourceGroup -Id ResourceId“ korrigiert. [#9882]</span><span class="sxs-lookup"><span data-stu-id="cd17d-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="cd17d-615">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Ressourcengruppenbereich hinzugefügt: „Get-AzDeploymentResourceGroupWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="cd17d-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="cd17d-616">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Abonnementbereich hinzugefügt: „Get-AzDeploymentWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="cd17d-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="cd17d-617">Alias: „Get-AzSubscriptionDeploymentWhatIf“</span><span class="sxs-lookup"><span data-stu-id="cd17d-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="cd17d-618">Parameter „-WhatIf“ und „-Confirm“ für „New-AzDeployment“ und „New-AzResourceGroupDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cd17d-619">Meldung zur Einstellung der Unterstützung für „ApiVersion“ in Bereitstellungs-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="cd17d-620">Funktion zum Anzeigen verbesserter Fehlermeldungen für Bereitstellungsfehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="cd17d-621">Protokollierung von correlationId bei Bereitstellungsfehlern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="cd17d-622">Eigenschaft „error“ zur Bereitstellungsskriptausgabe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="cd17d-623">NuGet-Microsoft.Azure.Management.ResourceManager auf „3.7.1-preview“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="cd17d-624">Bestimmte Testfälle entfernt, da die Error-Eigenschaft in DeploymentValidateResult von NuGet 3.7.1-preview in schreibgeschützt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd17d-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="cd17d-625">GenericResourceExpanded aus dem SDK ResourceManager 3.7.1-preview importiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="cd17d-626">Tagunterstützung für alle Get-Cmdlets für die Bereitstellung hinzugefügt sowie</span><span class="sxs-lookup"><span data-stu-id="cd17d-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="cd17d-627">„New-AzDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="cd17d-628">„New-AzManagementGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="cd17d-629">„New-AzResourceGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cd17d-630">„New-AzTenantDeployment“</span><span class="sxs-lookup"><span data-stu-id="cd17d-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-632">Fehler beim Hinzufügen eines Zertifikats mithilfe von „--SecretIdentifier“ behoben, der den falschen Zertifikatfingerabdruck erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="cd17d-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-633">Az.Sql</span></span>
* <span data-ttu-id="cd17d-634">Leistungsoptimierung von:</span><span class="sxs-lookup"><span data-stu-id="cd17d-634">Enhance performance of:</span></span>
    - <span data-ttu-id="cd17d-635">„Set-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="cd17d-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd17d-636">„Set-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="cd17d-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd17d-637">„Remove-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="cd17d-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd17d-638">„Remove-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="cd17d-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cd17d-639">„Enable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="cd17d-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd17d-640">„Enable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="cd17d-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd17d-641">„Disable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="cd17d-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cd17d-642">„Disable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="cd17d-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="cd17d-643">Clientseitige Validierung des Parameters „RetentionDays“ aus dem Cmdlet „Set-AzSqlDatabaseBackupShortTermRetentionPolicy“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="cd17d-644">Fehler beim Überwachen eines Speicherkontos in Vnet und Erstellen einer Rolle für den Mitwirkenden an Speicherblobdaten behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-645">Az.Storage</span></span>
* <span data-ttu-id="cd17d-646">„-AsJob“ hinzugefügt, um das Konto für das Cmdlet „Get-AzStorageAccount“ abzurufen/aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-647">KeyVersion als optional festgelegt, wenn das Speicherkonto mit KeyvaultEncryption aktualisiert wird, um die automatische Schlüsselrotation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="cd17d-648">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-649">Fehler beim Entfernen des Azure-Dateiverzeichnisses mit der Pipeline behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="cd17d-650">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="cd17d-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cd17d-651">Behoben [#9880]: Definition des DefaultAction-Werts für NetWorkRule in Übereinstimmung mit Swagger geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="cd17d-652">„Update-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="cd17d-653">„Get-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="cd17d-654">Behoben [#11624]: Doppelte Regeln werden beim Hinzufügen von NetworkRules übersprungen, um Serverfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="cd17d-655">„Add-AzStorageAccountNetworkRule“</span><span class="sxs-lookup"><span data-stu-id="cd17d-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="cd17d-656">Microsoft.Azure.Cosmos.Table SDK auf 1.0.7 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="cd17d-657">Warnmeldung hinzugefügt, mit der der Benutzer darauf hingewiesen wird, eine erneute Auflistung mit ContinuationToken auszuführen, wenn nur ein Teil der Elemente in der Liste der DataLake Gen2-Elemente zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="cd17d-658">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cd17d-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="cd17d-659">Unterstützung für das Erstellen oder Aktualisieren eines Speicherkontos mit Active Directory Domain Service-Authentifizierung für Azure Files.</span><span class="sxs-lookup"><span data-stu-id="cd17d-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="cd17d-660">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cd17d-661">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-662">Unterstützung für das Hinzufügen und Auflisten von Kerberos-Schlüsseln des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="cd17d-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="cd17d-663">„New-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="cd17d-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="cd17d-664">„Get-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="cd17d-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cd17d-665">Unterstützung für Failover für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="cd17d-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="cd17d-666">„Invoke-AzStorageAccountFailover“</span><span class="sxs-lookup"><span data-stu-id="cd17d-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="cd17d-667">Hilfe zu „Get-AzStorageBlobCopyState“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="cd17d-668">Hilfe zu „Get-AzStorageFileCopyState“ und „Start-AzStorageBlobCopy“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="cd17d-669">Speicherclientbibliothek v12 in Cmdlets Queue und File integriert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="cd17d-670">Ausgabetyp von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cd17d-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd17d-671">„Get-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="cd17d-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="cd17d-672">„Remove-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="cd17d-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="cd17d-673">„Get-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cd17d-674">„Set-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cd17d-675">„Start-AzStorageFileCopy“</span><span class="sxs-lookup"><span data-stu-id="cd17d-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="cd17d-676">Ausgabetyp von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cd17d-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd17d-677">„New-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="cd17d-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="cd17d-678">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="cd17d-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cd17d-679">Ausgabetyp von CloudFileShare in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cd17d-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cd17d-680">„Get-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="cd17d-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="cd17d-681">„New-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="cd17d-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="cd17d-682">„Remove-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="cd17d-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="cd17d-683">Ausgabetyp von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cd17d-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="cd17d-684">„Set-AzStorageShareQuota“</span><span class="sxs-lookup"><span data-stu-id="cd17d-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cd17d-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd17d-685">Az.TrafficManager</span></span>
* <span data-ttu-id="cd17d-686">Falscher Profilname in der ausführlichen Ausgabe von „DisableAzureTrafficManagerEndpoint“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-687">Az.Websites</span></span>
* <span data-ttu-id="cd17d-688">Tippfehler in der Hilfe zu „Update-AzWebAppAccessRestrictionConfig“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="cd17d-689">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cd17d-690">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="cd17d-690">Highlights since the last release</span></span>
* <span data-ttu-id="cd17d-691">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cd17d-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-692">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-693">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="cd17d-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-694">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-695">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cd17d-696">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-697">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-698">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-700">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="cd17d-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-701">Az.Compute</span></span>
* <span data-ttu-id="cd17d-702">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="cd17d-703">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="cd17d-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-704">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-705">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-706">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cd17d-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="cd17d-707">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cd17d-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="cd17d-708">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="cd17d-709">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-710">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cd17d-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="cd17d-711">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cd17d-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="cd17d-712">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="cd17d-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="cd17d-713">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-713">New cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-714">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd17d-715">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd17d-716">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cd17d-717">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="cd17d-718">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-719">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-720">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd17d-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="cd17d-721">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="cd17d-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="cd17d-722">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="cd17d-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="cd17d-723">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cd17d-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cd17d-724">Az.Maintenance</span></span>
* <span data-ttu-id="cd17d-725">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-726">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-727">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="cd17d-728">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd17d-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd17d-729">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd17d-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd17d-730">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd17d-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd17d-731">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cd17d-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cd17d-732">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cd17d-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cd17d-733">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cd17d-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cd17d-734">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cd17d-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-735">Az.Network</span></span>
* <span data-ttu-id="cd17d-736">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="cd17d-737">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cd17d-738">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cd17d-739">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="cd17d-740">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="cd17d-741">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="cd17d-742">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="cd17d-743">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cd17d-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="cd17d-744">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="cd17d-745">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cd17d-746">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="cd17d-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="cd17d-747">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cd17d-748">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="cd17d-749">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="cd17d-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="cd17d-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-753">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="cd17d-754">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-756">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-757">Az.Sql</span></span>
* <span data-ttu-id="cd17d-758">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="cd17d-759">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="cd17d-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-760">Az.Storage</span></span>
* <span data-ttu-id="cd17d-761">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cd17d-762">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="cd17d-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="cd17d-763">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="cd17d-764">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cd17d-765">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="cd17d-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="cd17d-766">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd17d-767">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd17d-768">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cd17d-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="cd17d-769">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd17d-770">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="cd17d-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="cd17d-771">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cd17d-772">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="cd17d-773">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cd17d-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="cd17d-774">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="cd17d-775">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-775">General</span></span>
* <span data-ttu-id="cd17d-776">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd17d-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="cd17d-777">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="cd17d-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="cd17d-778">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="cd17d-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="cd17d-779">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="cd17d-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="cd17d-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd17d-780">Az.Billing</span></span>
  - <span data-ttu-id="cd17d-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-781">Az.Compute</span></span>
  - <span data-ttu-id="cd17d-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd17d-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="cd17d-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-783">Az.EventHub</span></span>
  - <span data-ttu-id="cd17d-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-784">Az.IotHub</span></span>
  - <span data-ttu-id="cd17d-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-785">Az.KeyVault</span></span>
  - <span data-ttu-id="cd17d-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-786">Az.Monitor</span></span>
  - <span data-ttu-id="cd17d-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-787">Az.Network</span></span>
  - <span data-ttu-id="cd17d-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-788">Az.Resources</span></span>
  - <span data-ttu-id="cd17d-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-789">Az.Storage</span></span>
  - <span data-ttu-id="cd17d-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-790">Az.Websites</span></span>
* <span data-ttu-id="cd17d-791">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="cd17d-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="cd17d-792">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="cd17d-793">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="cd17d-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="cd17d-794">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-795">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-796">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="cd17d-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-797">Az.Compute</span></span>
* <span data-ttu-id="cd17d-798">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="cd17d-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="cd17d-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="cd17d-800">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="cd17d-801">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="cd17d-802">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="cd17d-802">[#11354]</span></span>
* <span data-ttu-id="cd17d-803">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="cd17d-804">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cd17d-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd17d-805">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cd17d-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd17d-806">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cd17d-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cd17d-807">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cd17d-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="cd17d-808">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="cd17d-809">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="cd17d-810">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="cd17d-811">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="cd17d-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-812">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-813">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="cd17d-814">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-816">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="cd17d-817">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-818">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-819">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="cd17d-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-820">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-821">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="cd17d-822">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-823">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cd17d-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="cd17d-824">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cd17d-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-825">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-826">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-827">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-828">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-829">Az.Network</span></span>
* <span data-ttu-id="cd17d-830">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="cd17d-831">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd17d-832">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cd17d-833">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="cd17d-834">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cd17d-835">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-837">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="cd17d-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-839">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="cd17d-840">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="cd17d-841">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="cd17d-842">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="cd17d-843">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="cd17d-844">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-845">Az.Resources</span></span>
* <span data-ttu-id="cd17d-846">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="cd17d-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="cd17d-847">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="cd17d-848">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="cd17d-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="cd17d-849">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-849">Added example.</span></span>
* <span data-ttu-id="cd17d-850">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="cd17d-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="cd17d-851">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-852">Az.Sql</span></span>
* <span data-ttu-id="cd17d-853">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="cd17d-854">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cd17d-855">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="cd17d-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="cd17d-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="cd17d-856">Az.Support</span></span>
* <span data-ttu-id="cd17d-857">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="cd17d-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-858">Az.Websites</span></span>
* <span data-ttu-id="cd17d-859">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="cd17d-860">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cd17d-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd17d-861">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cd17d-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd17d-862">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cd17d-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cd17d-863">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cd17d-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="cd17d-864">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-865">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-866">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="cd17d-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="cd17d-867">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="cd17d-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="cd17d-868">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-869">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-870">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="cd17d-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="cd17d-871">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="cd17d-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="cd17d-872">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="cd17d-873">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="cd17d-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-875">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-876">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-877">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cd17d-878">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-879">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-880">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-881">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-882">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="cd17d-883">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="cd17d-884">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-885">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="cd17d-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd17d-886">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="cd17d-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd17d-887">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="cd17d-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="cd17d-888">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="cd17d-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="cd17d-889">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cd17d-890">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cd17d-891">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="cd17d-892">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-893">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="cd17d-894">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="cd17d-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="cd17d-895">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-896">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-897">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="cd17d-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-898">Az.Network</span></span>
* <span data-ttu-id="cd17d-899">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="cd17d-900">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="cd17d-901">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="cd17d-902">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-903">Az.Resources</span></span>
* <span data-ttu-id="cd17d-904">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="cd17d-905">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="cd17d-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="cd17d-906">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="cd17d-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="cd17d-907">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="cd17d-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="cd17d-908">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="cd17d-909">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="cd17d-910">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="cd17d-911">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="cd17d-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd17d-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cd17d-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd17d-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cd17d-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd17d-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="cd17d-915">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="cd17d-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd17d-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="cd17d-917">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="cd17d-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-918">Az.Sql</span></span>
* <span data-ttu-id="cd17d-919">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cd17d-920">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="cd17d-921">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="cd17d-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="cd17d-922">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="cd17d-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="cd17d-923">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="cd17d-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="cd17d-924">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="cd17d-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="cd17d-925">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="cd17d-926">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="cd17d-927">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="cd17d-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-928">Az.Storage</span></span>
* <span data-ttu-id="cd17d-929">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="cd17d-930">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="cd17d-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="cd17d-931">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="cd17d-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="cd17d-932">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="cd17d-933">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="cd17d-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-934">Az.Websites</span></span>
* <span data-ttu-id="cd17d-935">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="cd17d-936">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="cd17d-937">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="cd17d-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="cd17d-938">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="cd17d-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="cd17d-939">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="cd17d-940">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-941">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-941">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-942">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="cd17d-943">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="cd17d-944">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-945">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-946">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-947">Az.Automation</span></span>
* <span data-ttu-id="cd17d-948">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-950">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="cd17d-951">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="cd17d-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-952">Az.Compute</span></span>
* <span data-ttu-id="cd17d-953">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="cd17d-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-954">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-955">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="cd17d-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-956">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-957">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cd17d-958">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-959">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-960">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-961">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cd17d-962">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cd17d-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-963">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-964">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-965">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-966">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="cd17d-967">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="cd17d-968">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-969">Az.Network</span></span>
* <span data-ttu-id="cd17d-970">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="cd17d-971">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cd17d-972">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cd17d-973">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="cd17d-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="cd17d-974">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-974">No new cmdlets are added.</span></span> <span data-ttu-id="cd17d-975">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-977">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-978">Az.Resources</span></span>
* <span data-ttu-id="cd17d-979">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="cd17d-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="cd17d-980">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="cd17d-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="cd17d-981">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="cd17d-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="cd17d-982">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="cd17d-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="cd17d-983">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="cd17d-984">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="cd17d-985">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="cd17d-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="cd17d-986">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-987">Az.Sql</span></span>
* <span data-ttu-id="cd17d-988">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="cd17d-989">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="cd17d-990">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="cd17d-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cd17d-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd17d-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cd17d-992">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd17d-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd17d-993">Az.StorageSync</span></span>
* <span data-ttu-id="cd17d-994">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="cd17d-995">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-996">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-996">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-997">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="cd17d-998">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-999">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1000">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="cd17d-1001">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="cd17d-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-1003">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="cd17d-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="cd17d-1004">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="cd17d-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="cd17d-1005">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="cd17d-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="cd17d-1006">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1007">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1008">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="cd17d-1009">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="cd17d-1010">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="cd17d-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="cd17d-1012">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1013">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1014">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cd17d-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cd17d-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="cd17d-1016">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="cd17d-1017">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-1018">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-1019">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-1020">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-1021">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1022">Az.Network</span></span>
* <span data-ttu-id="cd17d-1023">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="cd17d-1024">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="cd17d-1025">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1026">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="cd17d-1027">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="cd17d-1028">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="cd17d-1029">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="cd17d-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="cd17d-1030">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="cd17d-1031">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="cd17d-1033">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="cd17d-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="cd17d-1035">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-1037">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="cd17d-1038">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="cd17d-1039">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="cd17d-1040">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1042">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="cd17d-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="cd17d-1043">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1044">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1045">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="cd17d-1046">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1047">Az.Sql</span></span>
<span data-ttu-id="cd17d-1048">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1049">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1050">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="cd17d-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="cd17d-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd17d-1052">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="cd17d-1053">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1054">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1055">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="cd17d-1056">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="cd17d-1057">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="cd17d-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1058">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1059">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-1060">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-1061">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1062">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1063">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cd17d-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd17d-1065">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cd17d-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd17d-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cd17d-1067">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd17d-1068">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="cd17d-1069">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd17d-1070">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="cd17d-1071">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd17d-1072">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="cd17d-1073">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cd17d-1074">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="cd17d-1075">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd17d-1076">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="cd17d-1077">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd17d-1078">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="cd17d-1079">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cd17d-1080">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="cd17d-1081">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="cd17d-1082">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="cd17d-1083">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="cd17d-1084">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1085">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1086">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="cd17d-1087">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="cd17d-1088">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="cd17d-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cd17d-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="cd17d-1090">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1091">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-1092">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-1093">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-1094">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cd17d-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd17d-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="cd17d-1096">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="cd17d-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd17d-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd17d-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="cd17d-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd17d-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd17d-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd17d-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd17d-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd17d-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="cd17d-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="cd17d-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="cd17d-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1104">Az.Network</span></span>
* <span data-ttu-id="cd17d-1105">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1107">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="cd17d-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="cd17d-1108">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="cd17d-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cd17d-1109">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="cd17d-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cd17d-1110">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="cd17d-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1111">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1112">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1113">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1114">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="cd17d-1115">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cd17d-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cd17d-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cd17d-1117">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1118">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1119">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="cd17d-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="cd17d-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="cd17d-1121">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="cd17d-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="cd17d-1123">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="cd17d-1124">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-1124">General</span></span>
* <span data-ttu-id="cd17d-1125">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1126">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1127">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="cd17d-1128">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-1129">Az.Batch</span></span>
* <span data-ttu-id="cd17d-1130">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1131">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1132">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-1134">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="cd17d-1135">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd17d-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd17d-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd17d-1137">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="cd17d-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-1138">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-1139">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="cd17d-1140">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="cd17d-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="cd17d-1141">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1142">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-1143">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="cd17d-1144">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="cd17d-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="cd17d-1145">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1146">Az.Network</span></span>
* <span data-ttu-id="cd17d-1147">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="cd17d-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1148">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1149">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="cd17d-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="cd17d-1150">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1151">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1152">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1153">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1154">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cd17d-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="cd17d-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="cd17d-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="cd17d-1157">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="cd17d-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="cd17d-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="cd17d-1159">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="cd17d-1160">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="cd17d-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="cd17d-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="cd17d-1163">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="cd17d-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="cd17d-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="cd17d-1165">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="cd17d-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="cd17d-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="cd17d-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="cd17d-1167">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-1168">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-1169">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="cd17d-1170">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1171">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1172">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="cd17d-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="cd17d-1173">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="cd17d-1174">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="cd17d-1175">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd17d-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="cd17d-1176">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="cd17d-1177">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd17d-1178">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="cd17d-1179">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="cd17d-1180">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="cd17d-1181">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="cd17d-1182">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cd17d-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cd17d-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cd17d-1184">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd17d-1185">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1185">Get the Order</span></span>
* <span data-ttu-id="cd17d-1186">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd17d-1187">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1187">Create new Order</span></span>
* <span data-ttu-id="cd17d-1188">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cd17d-1189">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1189">Remove the Order</span></span>
* <span data-ttu-id="cd17d-1190">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="cd17d-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="cd17d-1191">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="cd17d-1191">Now creates Local Share</span></span>
* <span data-ttu-id="cd17d-1192">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="cd17d-1193">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="cd17d-1194">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="cd17d-1195">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="cd17d-1196">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd17d-1197">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="cd17d-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="cd17d-1198">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd17d-1199">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1199">Create new Triggers</span></span>
* <span data-ttu-id="cd17d-1200">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cd17d-1201">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1202">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1203">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="cd17d-1204">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-1206">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1207">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-1208">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-1210">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="cd17d-1211">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="cd17d-1212">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="cd17d-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="cd17d-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1214">Az.Network</span></span>
* <span data-ttu-id="cd17d-1215">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cd17d-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cd17d-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="cd17d-1217">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1219">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="cd17d-1220">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="cd17d-1221">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd17d-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd17d-1222">Az.RedisCache</span></span>
* <span data-ttu-id="cd17d-1223">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="cd17d-1224">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="cd17d-1225">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1226">Az.Resources</span></span>
- <span data-ttu-id="cd17d-1227">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="cd17d-1228">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="cd17d-1229">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="cd17d-1230">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="cd17d-1231">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1232">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1233">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="cd17d-1234">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="cd17d-1235">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="cd17d-1236">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-1236">General</span></span>
* <span data-ttu-id="cd17d-1237">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1238">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1239">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cd17d-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1240">Az.Advisor</span></span>
* <span data-ttu-id="cd17d-1241">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-1242">Az.Batch</span></span>
* <span data-ttu-id="cd17d-1243">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="cd17d-1244">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="cd17d-1245">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="cd17d-1246">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="cd17d-1247">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="cd17d-1248">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="cd17d-1249">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="cd17d-1250">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="cd17d-1251">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="cd17d-1252">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cd17d-1253">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="cd17d-1254">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="cd17d-1255">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cd17d-1256">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="cd17d-1257">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="cd17d-1258">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="cd17d-1259">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="cd17d-1260">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="cd17d-1261">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="cd17d-1262">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="cd17d-1263">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cd17d-1264">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cd17d-1265">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="cd17d-1266">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="cd17d-1267">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="cd17d-1268">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="cd17d-1269">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="cd17d-1270">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="cd17d-1271">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="cd17d-1272">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="cd17d-1273">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="cd17d-1274">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="cd17d-1275">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="cd17d-1276">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="cd17d-1277">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="cd17d-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="cd17d-1278">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="cd17d-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-1279">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-1280">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="cd17d-1281">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1282">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1283">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="cd17d-1284">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="cd17d-1285">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cd17d-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="cd17d-1286">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd17d-1287">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="cd17d-1288">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="cd17d-1289">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd17d-1290">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1290">Breaking changes</span></span>
    - <span data-ttu-id="cd17d-1291">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="cd17d-1292">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1293">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1294">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-1296">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="cd17d-1297">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="cd17d-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="cd17d-1298">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="cd17d-1299">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="cd17d-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="cd17d-1300">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="cd17d-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="cd17d-1301">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="cd17d-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-1303">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-1304">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-1305">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="cd17d-1306">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="cd17d-1307">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="cd17d-1308">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="cd17d-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd17d-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd17d-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd17d-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd17d-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cd17d-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cd17d-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd17d-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="cd17d-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd17d-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="cd17d-1314">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="cd17d-1315">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cd17d-1316">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cd17d-1317">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="cd17d-1318">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="cd17d-1319">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="cd17d-1320">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="cd17d-1321">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="cd17d-1322">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="cd17d-1323">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="cd17d-1324">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="cd17d-1325">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="cd17d-1326">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1327">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-1328">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1328">Breaking changes:</span></span>
    - <span data-ttu-id="cd17d-1329">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd17d-1330">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd17d-1331">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd17d-1332">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd17d-1333">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="cd17d-1334">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="cd17d-1335">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="cd17d-1336">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="cd17d-1337">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd17d-1338">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cd17d-1339">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cd17d-1340">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1342">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1343">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="cd17d-1344">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="cd17d-1345">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1346">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1347">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1348">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1349">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-1350">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1351">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1352">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1353">Az.Network</span></span>
* <span data-ttu-id="cd17d-1354">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="cd17d-1355">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cd17d-1361">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="cd17d-1362">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1362">New cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="cd17d-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="cd17d-1364">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="cd17d-1365">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="cd17d-1366">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="cd17d-1367">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="cd17d-1368">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="cd17d-1369">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="cd17d-1370">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="cd17d-1371">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="cd17d-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd17d-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd17d-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cd17d-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="cd17d-1377">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="cd17d-1378">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd17d-1379">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cd17d-1380">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cd17d-1381">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="cd17d-1382">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="cd17d-1383">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="cd17d-1384">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="cd17d-1386">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd17d-1387">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd17d-1388">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd17d-1389">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd17d-1390">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cd17d-1391">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="cd17d-1392">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="cd17d-1393">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cd17d-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="cd17d-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="cd17d-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="cd17d-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cd17d-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="cd17d-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cd17d-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="cd17d-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="cd17d-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="cd17d-1400">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd17d-1401">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="cd17d-1402">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="cd17d-1403">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="cd17d-1404">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="cd17d-1405">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cd17d-1406">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="cd17d-1407">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="cd17d-1408">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="cd17d-1409">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="cd17d-1410">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="cd17d-1411">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="cd17d-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="cd17d-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="cd17d-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-1417">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1418">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1419">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="cd17d-1420">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="cd17d-1421">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="cd17d-1422">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="cd17d-1423">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="cd17d-1424">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cd17d-1425">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="cd17d-1426">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="cd17d-1427">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1428">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1429">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="cd17d-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cd17d-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cd17d-1432">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="cd17d-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd17d-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="cd17d-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd17d-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="cd17d-1435">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="cd17d-1436">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-1436">General</span></span>
* <span data-ttu-id="cd17d-1437">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cd17d-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1438">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1439">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-1441">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="cd17d-1442">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="cd17d-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-1443">Az.Automation</span></span>
* <span data-ttu-id="cd17d-1444">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-1445">Az.Batch</span></span>
* <span data-ttu-id="cd17d-1446">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1447">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1448">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cd17d-1449">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="cd17d-1450">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="cd17d-1451">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1452">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1453">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="cd17d-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="cd17d-1454">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="cd17d-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="cd17d-1455">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-1457">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="cd17d-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cd17d-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cd17d-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="cd17d-1459">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="cd17d-1460">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="cd17d-1461">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="cd17d-1462">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1463">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-1464">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="cd17d-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="cd17d-1465">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1466">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-1467">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="cd17d-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="cd17d-1468">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="cd17d-1469">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="cd17d-1470">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1471">Az.Network</span></span>
* <span data-ttu-id="cd17d-1472">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="cd17d-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="cd17d-1473">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="cd17d-1474">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="cd17d-1476">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cd17d-1477">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="cd17d-1478">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="cd17d-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd17d-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd17d-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cd17d-1482">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="cd17d-1483">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="cd17d-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="cd17d-1484">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="cd17d-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="cd17d-1485">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="cd17d-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd17d-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd17d-1486">Az.RedisCache</span></span>
* <span data-ttu-id="cd17d-1487">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1488">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1489">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1490">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1491">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="cd17d-1492">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cd17d-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cd17d-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="cd17d-1494">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cd17d-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd17d-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd17d-1496">Az.StorageSync</span></span>
* <span data-ttu-id="cd17d-1497">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1498">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1499">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="cd17d-1500">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-1502">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="cd17d-1503">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="cd17d-1504">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-1505">Az.Automation</span></span>
* <span data-ttu-id="cd17d-1506">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="cd17d-1507">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="cd17d-1508">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1509">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1510">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="cd17d-1511">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd17d-1512">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="cd17d-1513">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="cd17d-1514">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="cd17d-1515">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="cd17d-1516">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="cd17d-1517">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="cd17d-1518">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1519">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1520">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="cd17d-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="cd17d-1521">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-1522">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-1523">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1524">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-1525">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="cd17d-1526">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="cd17d-1527">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="cd17d-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd17d-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd17d-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd17d-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd17d-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd17d-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cd17d-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="cd17d-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1532">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-1533">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="cd17d-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="cd17d-1534">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="cd17d-1535">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="cd17d-1536">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="cd17d-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="cd17d-1537">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="cd17d-1538">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="cd17d-1539">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="cd17d-1540">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="cd17d-1541">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cd17d-1542">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="cd17d-1543">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cd17d-1544">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="cd17d-1545">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="cd17d-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="cd17d-1546">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="cd17d-1547">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="cd17d-1548">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="cd17d-1549">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="cd17d-1550">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="cd17d-1551">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="cd17d-1552">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1552">Overall improved help files</span></span>
* <span data-ttu-id="cd17d-1553">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1554">Az.Network</span></span>
* <span data-ttu-id="cd17d-1555">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="cd17d-1556">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="cd17d-1557">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="cd17d-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="cd17d-1558">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="cd17d-1559">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="cd17d-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="cd17d-1560">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="cd17d-1561">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="cd17d-1562">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="cd17d-1563">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="cd17d-1564">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="cd17d-1565">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="cd17d-1566">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="cd17d-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="cd17d-1567">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1567">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cd17d-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="cd17d-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="cd17d-1570">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cd17d-1571">New-VpnSite</span></span>
        - <span data-ttu-id="cd17d-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="cd17d-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="cd17d-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="cd17d-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="cd17d-1575">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1577">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="cd17d-1578">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1579">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1580">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="cd17d-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-1582">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="cd17d-1583">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="cd17d-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd17d-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd17d-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd17d-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd17d-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd17d-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd17d-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="cd17d-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd17d-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd17d-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd17d-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd17d-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd17d-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd17d-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd17d-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd17d-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="cd17d-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="cd17d-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cd17d-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd17d-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cd17d-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="cd17d-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cd17d-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="cd17d-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="cd17d-1597">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="cd17d-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd17d-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-1598">Az.SignalR</span></span>
* <span data-ttu-id="cd17d-1599">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1600">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1601">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="cd17d-1602">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="cd17d-1603">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cd17d-1604">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="cd17d-1605">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1606">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1607">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cd17d-1608">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="cd17d-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="cd17d-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="cd17d-1611">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="cd17d-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="cd17d-1613">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="cd17d-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="cd17d-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd17d-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd17d-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cd17d-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd17d-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1618">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1619">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="cd17d-1620">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="cd17d-1621">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="cd17d-1622">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="cd17d-1623">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-1623">General</span></span>
* <span data-ttu-id="cd17d-1624">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1625">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1626">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-1627">Az.Aks</span></span>
* <span data-ttu-id="cd17d-1628">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="cd17d-1629">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="cd17d-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-1631">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="cd17d-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="cd17d-1632">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="cd17d-1633">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="cd17d-1634">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="cd17d-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="cd17d-1635">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="cd17d-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-1636">Az.Batch</span></span>
* <span data-ttu-id="cd17d-1637">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-1638">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-1639">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1640">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1641">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="cd17d-1642">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="cd17d-1643">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="cd17d-1644">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="cd17d-1645">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="cd17d-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="cd17d-1646">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="cd17d-1647">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="cd17d-1648">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1649">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1650">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="cd17d-1651">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="cd17d-1652">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="cd17d-1653">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-1655">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1656">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-1657">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="cd17d-1658">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="cd17d-1659">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="cd17d-1660">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="cd17d-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cd17d-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cd17d-1662">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1663">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-1664">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1665">Az.Network</span></span>
* <span data-ttu-id="cd17d-1666">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="cd17d-1667">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="cd17d-1668">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="cd17d-1669">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="cd17d-1670">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="cd17d-1671">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="cd17d-1672">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-1674">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="cd17d-1675">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1675">Added example</span></span>
    - <span data-ttu-id="cd17d-1676">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="cd17d-1677">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="cd17d-1678">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1680">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1681">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1682">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="cd17d-1683">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="cd17d-1684">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="cd17d-1685">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-1687">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="cd17d-1688">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="cd17d-1689">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-1691">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="cd17d-1692">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="cd17d-1693">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="cd17d-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="cd17d-1694">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="cd17d-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="cd17d-1695">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="cd17d-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="cd17d-1696">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1697">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1698">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1699">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1700">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="cd17d-1701">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="cd17d-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="cd17d-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="cd17d-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd17d-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="cd17d-1704">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="cd17d-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="cd17d-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd17d-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1706">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1707">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="cd17d-1708">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1709">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1710">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cd17d-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cd17d-1712">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-1713">Az.Automation</span></span>
* <span data-ttu-id="cd17d-1714">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-1716">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1717">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1718">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd17d-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd17d-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd17d-1720">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="cd17d-1721">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1722">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1723">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="cd17d-1724">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1725">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-1726">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cd17d-1727">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-1728">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-1729">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd17d-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd17d-1730">Az.LogicApp</span></span>
* <span data-ttu-id="cd17d-1731">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="cd17d-1732">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cd17d-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="cd17d-1734">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1735">Az.Network</span></span>
* <span data-ttu-id="cd17d-1736">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="cd17d-1737">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1737">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd17d-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd17d-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd17d-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cd17d-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="cd17d-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="cd17d-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="cd17d-1746">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd17d-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="cd17d-1747">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="cd17d-1748">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="cd17d-1749">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="cd17d-1750">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="cd17d-1751">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="cd17d-1752">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="cd17d-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd17d-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cd17d-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cd17d-1756">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cd17d-1757">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="cd17d-1758">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cd17d-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cd17d-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="cd17d-1762">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="cd17d-1763">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="cd17d-1764">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-1766">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="cd17d-1767">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1769">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cd17d-1770">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="cd17d-1771">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="cd17d-1772">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cd17d-1773">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="cd17d-1774">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cd17d-1775">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="cd17d-1776">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cd17d-1777">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="cd17d-1778">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1779">Az.Resources</span></span>
- <span data-ttu-id="cd17d-1780">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="cd17d-1781">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-1783">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cd17d-1784">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1785">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1786">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="cd17d-1787">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="cd17d-1788">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1789">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1790">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd17d-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd17d-1791">Az.StorageSync</span></span>
* <span data-ttu-id="cd17d-1792">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="cd17d-1793">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1794">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1795">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="cd17d-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="cd17d-1796">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="cd17d-1797">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="cd17d-1798">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1799">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1800">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cd17d-1801">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cd17d-1802">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cd17d-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1803">Az.Advisor</span></span>
* <span data-ttu-id="cd17d-1804">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cd17d-1805">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-1807">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="cd17d-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cd17d-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cd17d-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cd17d-1809">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cd17d-1810">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cd17d-1811">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="cd17d-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cd17d-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cd17d-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cd17d-1813">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-1814">Az.Automation</span></span>
* <span data-ttu-id="cd17d-1815">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1816">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1817">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-1818">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-1819">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd17d-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd17d-1820">Az.EventGrid</span></span>
* <span data-ttu-id="cd17d-1821">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1822">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-1823">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1824">Az.Network</span></span>
* <span data-ttu-id="cd17d-1825">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cd17d-1826">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-1828">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="cd17d-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cd17d-1829">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="cd17d-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-1831">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1833">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="cd17d-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1834">Az.Resources</span></span>
    - <span data-ttu-id="cd17d-1835">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cd17d-1836">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cd17d-1837">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cd17d-1838">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-1840">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="cd17d-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1841">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1842">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cd17d-1843">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cd17d-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd17d-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd17d-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cd17d-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cd17d-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cd17d-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cd17d-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cd17d-1850">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1851">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1852">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cd17d-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd17d-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cd17d-1854">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cd17d-1855">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cd17d-1856">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cd17d-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cd17d-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cd17d-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cd17d-1859">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="cd17d-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cd17d-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd17d-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cd17d-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cd17d-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cd17d-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cd17d-1862">Az.StorageSync</span></span>
* <span data-ttu-id="cd17d-1863">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cd17d-1864">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-1865">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-1866">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cd17d-1867">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="cd17d-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cd17d-1868">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cd17d-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cd17d-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cd17d-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="cd17d-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1871">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1872">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cd17d-1873">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cd17d-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cd17d-1874">Az.Dns</span></span>
* <span data-ttu-id="cd17d-1875">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd17d-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd17d-1876">Az.EventGrid</span></span>
* <span data-ttu-id="cd17d-1877">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cd17d-1878">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1878">New cmdlets:</span></span>
    - <span data-ttu-id="cd17d-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd17d-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd17d-1880">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd17d-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd17d-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd17d-1882">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cd17d-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cd17d-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cd17d-1884">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd17d-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cd17d-1886">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cd17d-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cd17d-1888">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cd17d-1889">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cd17d-1890">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cd17d-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cd17d-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cd17d-1892">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="cd17d-1893">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cd17d-1894">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cd17d-1895">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="cd17d-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cd17d-1897">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cd17d-1898">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cd17d-1899">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cd17d-1900">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cd17d-1901">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="cd17d-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cd17d-1902">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="cd17d-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cd17d-1903">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cd17d-1904">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="cd17d-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cd17d-1906">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cd17d-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cd17d-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cd17d-1908">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cd17d-1909">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cd17d-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cd17d-1912">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cd17d-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd17d-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cd17d-1914">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1915">Az.Network</span></span>
* <span data-ttu-id="cd17d-1916">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cd17d-1917">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1917">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cd17d-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cd17d-1919">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cd17d-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cd17d-1920">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1920">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cd17d-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cd17d-1922">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cd17d-1923">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1923">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd17d-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd17d-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cd17d-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cd17d-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cd17d-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cd17d-1929">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cd17d-1930">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-1930">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd17d-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd17d-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd17d-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd17d-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cd17d-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cd17d-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cd17d-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cd17d-1935">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="cd17d-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cd17d-1936">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="cd17d-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cd17d-1937">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="cd17d-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cd17d-1938">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cd17d-1939">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cd17d-1940">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cd17d-1941">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cd17d-1942">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="cd17d-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cd17d-1943">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cd17d-1944">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cd17d-1945">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cd17d-1946">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cd17d-1947">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cd17d-1948">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cd17d-1949">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="cd17d-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cd17d-1950">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cd17d-1951">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cd17d-1952">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cd17d-1953">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="cd17d-1954">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="cd17d-1955">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cd17d-1956">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cd17d-1957">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-1959">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-1960">Az.Resources</span></span>
* <span data-ttu-id="cd17d-1961">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cd17d-1962">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cd17d-1963">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cd17d-1964">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-1966">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-1967">Az.Sql</span></span>
* <span data-ttu-id="cd17d-1968">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cd17d-1969">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cd17d-1970">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cd17d-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd17d-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd17d-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cd17d-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cd17d-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cd17d-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cd17d-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cd17d-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-1976">Az.Storage</span></span>
* <span data-ttu-id="cd17d-1977">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="cd17d-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cd17d-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd17d-1979">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="cd17d-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cd17d-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-1981">Az.Websites</span></span>
* <span data-ttu-id="cd17d-1982">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="cd17d-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cd17d-1983">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cd17d-1984">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cd17d-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-1985">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-1986">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-1987">Az.Compute</span></span>
* <span data-ttu-id="cd17d-1988">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="cd17d-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cd17d-1989">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cd17d-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-1990">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-1991">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="cd17d-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cd17d-1992">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="cd17d-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-1993">Az.Network</span></span>
* <span data-ttu-id="cd17d-1994">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cd17d-1995">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-1997">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="cd17d-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-1999">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-2001">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="cd17d-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-2003">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cd17d-2004">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2005">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2006">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cd17d-2007">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cd17d-2008">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cd17d-2009">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="cd17d-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2010">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2011">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cd17d-2012">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cd17d-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-2014">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cd17d-2015">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cd17d-2016">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="cd17d-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cd17d-2017">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="cd17d-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cd17d-2018">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cd17d-2019">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="cd17d-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cd17d-2020">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="cd17d-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cd17d-2021">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="cd17d-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cd17d-2022">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cd17d-2023">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="cd17d-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cd17d-2024">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="cd17d-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cd17d-2025">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="cd17d-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cd17d-2026">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="cd17d-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cd17d-2027">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cd17d-2028">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="cd17d-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cd17d-2029">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="cd17d-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cd17d-2030">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="cd17d-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cd17d-2031">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="cd17d-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cd17d-2032">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="cd17d-2033">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="cd17d-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cd17d-2034">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cd17d-2035">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cd17d-2036">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cd17d-2037">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="cd17d-2038">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cd17d-2039">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cd17d-2040">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cd17d-2041">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cd17d-2042">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cd17d-2043">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cd17d-2044">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="cd17d-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cd17d-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cd17d-2046">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cd17d-2047">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd17d-2048">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cd17d-2049">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cd17d-2050">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cd17d-2051">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cd17d-2052">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cd17d-2053">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd17d-2054">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="cd17d-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cd17d-2055">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cd17d-2056">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cd17d-2057">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="cd17d-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cd17d-2058">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cd17d-2059">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="cd17d-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cd17d-2060">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cd17d-2061">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="cd17d-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cd17d-2062">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cd17d-2063">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cd17d-2064">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="cd17d-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cd17d-2065">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cd17d-2066">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="cd17d-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cd17d-2067">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cd17d-2068">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cd17d-2069">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cd17d-2070">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cd17d-2071">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cd17d-2072">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cd17d-2073">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cd17d-2074">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cd17d-2075">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cd17d-2076">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cd17d-2077">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cd17d-2078">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cd17d-2079">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cd17d-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cd17d-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cd17d-2081">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cd17d-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cd17d-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cd17d-2083">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cd17d-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cd17d-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cd17d-2085">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cd17d-2086">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cd17d-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cd17d-2088">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="cd17d-2089">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cd17d-2090">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="cd17d-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2091">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2092">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cd17d-2093">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="cd17d-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cd17d-2094">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="cd17d-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cd17d-2095">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cd17d-2096">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="cd17d-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cd17d-2097">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cd17d-2098">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2099">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2100">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cd17d-2101">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2103">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2104">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-2105">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2106">Az.Network</span></span>
* <span data-ttu-id="cd17d-2107">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cd17d-2108">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="cd17d-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cd17d-2110">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd17d-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2111">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2112">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2113">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2114">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cd17d-2115">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2116">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2117">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-2119">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="cd17d-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cd17d-2120">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="cd17d-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2121">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2122">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="cd17d-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cd17d-2123">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cd17d-2124">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cd17d-2125">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cd17d-2126">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cd17d-2127">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="cd17d-2128">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2128">Breaking changes</span></span>
    - <span data-ttu-id="cd17d-2129">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cd17d-2130">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cd17d-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cd17d-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="cd17d-2132">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cd17d-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cd17d-2133">Az.Dns</span></span>
* <span data-ttu-id="cd17d-2134">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="cd17d-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cd17d-2135">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cd17d-2136">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="cd17d-2138">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cd17d-2139">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-2140">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-2141">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cd17d-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd17d-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cd17d-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cd17d-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cd17d-2144">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cd17d-2145">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cd17d-2146">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cd17d-2147">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2148">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-2149">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="cd17d-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cd17d-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cd17d-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd17d-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cd17d-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cd17d-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cd17d-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cd17d-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cd17d-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cd17d-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cd17d-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cd17d-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd17d-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd17d-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd17d-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd17d-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cd17d-2161">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="cd17d-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cd17d-2162">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2163">Az.Network</span></span>
* <span data-ttu-id="cd17d-2164">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cd17d-2165">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-2165">New cmdlets</span></span>
        - <span data-ttu-id="cd17d-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="cd17d-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cd17d-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cd17d-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cd17d-2170">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="cd17d-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cd17d-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cd17d-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cd17d-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cd17d-2173">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cd17d-2174">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cd17d-2175">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-2177">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="cd17d-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cd17d-2178">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cd17d-2179">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-2181">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="cd17d-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cd17d-2182">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="cd17d-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cd17d-2183">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="cd17d-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cd17d-2184">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="cd17d-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cd17d-2185">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="cd17d-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cd17d-2186">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cd17d-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cd17d-2187">Az.Relay</span></span>
* <span data-ttu-id="cd17d-2188">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-2190">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2191">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2192">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="cd17d-2193">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cd17d-2194">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cd17d-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="cd17d-2196">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cd17d-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cd17d-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cd17d-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2200">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2201">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cd17d-2202">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cd17d-2203">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-2204">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-2205">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="cd17d-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="cd17d-2206">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd17d-2207">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd17d-2208">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd17d-2209">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd17d-2210">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd17d-2211">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2212">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2213">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cd17d-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-2214">Az.Batch</span></span>
* <span data-ttu-id="cd17d-2215">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-2216">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-2217">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-2219">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2220">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2221">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cd17d-2222">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2223">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-2224">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-2225">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2227">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd17d-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd17d-2228">Az.EventGrid</span></span>
* <span data-ttu-id="cd17d-2229">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-2230">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-2231">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cd17d-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cd17d-2232">Az.HDInsight</span></span>
* <span data-ttu-id="cd17d-2233">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-2234">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-2235">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-2236">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-2237">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2238">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cd17d-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd17d-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="cd17d-2240">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cd17d-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd17d-2241">Az.Media</span></span>
* <span data-ttu-id="cd17d-2242">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2243">Az.Monitor</span></span>
  * <span data-ttu-id="cd17d-2244">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cd17d-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cd17d-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cd17d-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cd17d-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cd17d-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd17d-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd17d-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd17d-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cd17d-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cd17d-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cd17d-2250">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2251">Az.Network</span></span>
* <span data-ttu-id="cd17d-2252">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2253">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cd17d-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cd17d-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="cd17d-2255">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-2257">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cd17d-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cd17d-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cd17d-2259">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-2261">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2262">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cd17d-2263">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cd17d-2264">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd17d-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd17d-2265">Az.RedisCache</span></span>
* <span data-ttu-id="cd17d-2266">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2267">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2268">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2269">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2270">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cd17d-2271">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2272">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cd17d-2273">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cd17d-2274">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="cd17d-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cd17d-2275">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="cd17d-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cd17d-2276">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2277">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2278">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cd17d-2279">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cd17d-2280">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cd17d-2281">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cd17d-2282">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-2283">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-2284">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="cd17d-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="cd17d-2285">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd17d-2286">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd17d-2287">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd17d-2288">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd17d-2289">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd17d-2290">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2291">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2292">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="cd17d-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd17d-2294">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cd17d-2295">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2296">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2297">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cd17d-2298">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cd17d-2299">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="cd17d-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2300">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2301">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cd17d-2302">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cd17d-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd17d-2304">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="cd17d-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-2305">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-2306">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cd17d-2307">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2308">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2309">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cd17d-2310">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cd17d-2311">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="cd17d-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cd17d-2312">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd17d-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cd17d-2313">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cd17d-2314">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="cd17d-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2315">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2316">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2317">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2318">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="cd17d-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cd17d-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd17d-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="cd17d-2320">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="cd17d-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cd17d-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd17d-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd17d-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd17d-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cd17d-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cd17d-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cd17d-2325">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="cd17d-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cd17d-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd17d-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cd17d-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cd17d-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cd17d-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cd17d-2330">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cd17d-2331">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="cd17d-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="cd17d-2332">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="cd17d-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="cd17d-2333">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cd17d-2334">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cd17d-2335">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cd17d-2336">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd17d-2337">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cd17d-2338">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2339">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2340">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cd17d-2341">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="cd17d-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="cd17d-2342">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2342">Pre-Post script</span></span>
    * <span data-ttu-id="cd17d-2343">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="cd17d-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2344">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2345">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cd17d-2346">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-2347">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-2348">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2349">Az.Network</span></span>
* <span data-ttu-id="cd17d-2350">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cd17d-2351">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-2353">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cd17d-2354">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2355">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2356">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cd17d-2357">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2358">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2359">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2360">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2361">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cd17d-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd17d-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd17d-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cd17d-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cd17d-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cd17d-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cd17d-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cd17d-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2368">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2369">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="cd17d-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="cd17d-2370">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2371">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2372">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cd17d-2373">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2374">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2375">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="cd17d-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd17d-2376">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cd17d-2377">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-2378">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-2379">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2380">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2381">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-2382">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-2383">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd17d-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd17d-2384">Az.LogicApp</span></span>
* <span data-ttu-id="cd17d-2385">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2386">Az.Network</span></span>
* <span data-ttu-id="cd17d-2387">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-2389">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cd17d-2390">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="cd17d-2390">SDK Update</span></span>
* <span data-ttu-id="cd17d-2391">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cd17d-2392">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2393">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2394">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cd17d-2395">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="cd17d-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cd17d-2396">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cd17d-2397">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="cd17d-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cd17d-2398">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cd17d-2399">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="cd17d-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2400">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2401">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cd17d-2402">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2403">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2404">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd17d-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cd17d-2405">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd17d-2407">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2408">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2409">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cd17d-2410">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cd17d-2411">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-2413">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2414">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2415">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cd17d-2416">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="cd17d-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cd17d-2417">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cd17d-2418">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2420">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cd17d-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-2421">Az.EventHub</span></span>
* <span data-ttu-id="cd17d-2422">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-2423">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-2424">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd17d-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd17d-2425">Az.LogicApp</span></span>
* <span data-ttu-id="cd17d-2426">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cd17d-2427">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cd17d-2428">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="cd17d-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cd17d-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd17d-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd17d-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd17d-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd17d-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd17d-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cd17d-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="cd17d-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cd17d-2433">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cd17d-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd17d-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd17d-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cd17d-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cd17d-2438">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cd17d-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2439">Az.Monitor</span></span>
* <span data-ttu-id="cd17d-2440">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2441">Az.Network</span></span>
* <span data-ttu-id="cd17d-2442">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="cd17d-2444">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cd17d-2445">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="cd17d-2446">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2447">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2448">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cd17d-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd17d-2449">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cd17d-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cd17d-2450">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="cd17d-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cd17d-2451">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2452">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2453">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cd17d-2454">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="cd17d-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2455">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2456">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cd17d-2457">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2458">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2459">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="cd17d-2461">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="cd17d-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2462">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2463">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cd17d-2464">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cd17d-2465">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="cd17d-2467">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2468">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2469">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="cd17d-2470">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="cd17d-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cd17d-2471">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="cd17d-2472">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="cd17d-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2473">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2474">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cd17d-2475">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cd17d-2476">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cd17d-2477">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2478">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2479">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cd17d-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cd17d-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="cd17d-2481">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="cd17d-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="cd17d-2483">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="cd17d-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cd17d-2484">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2485">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2486">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cd17d-2487">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd17d-2488">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cd17d-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cd17d-2489">Az.Aks</span></span>
* <span data-ttu-id="cd17d-2490">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cd17d-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2491">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2492">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cd17d-2493">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cd17d-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cd17d-2494">Az.Cdn</span></span>
* <span data-ttu-id="cd17d-2495">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2496">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2497">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cd17d-2498">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cd17d-2499">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cd17d-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd17d-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cd17d-2501">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cd17d-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd17d-2502">Az.DataFactory</span></span>
* <span data-ttu-id="cd17d-2503">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2505">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cd17d-2506">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="cd17d-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cd17d-2507">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-2508">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-2509">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cd17d-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-2510">Az.KeyVault</span></span>
* <span data-ttu-id="cd17d-2511">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2512">Az.Network</span></span>
* <span data-ttu-id="cd17d-2513">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2514">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2515">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cd17d-2516">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cd17d-2517">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cd17d-2518">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="cd17d-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cd17d-2519">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="cd17d-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cd17d-2520">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cd17d-2521">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="cd17d-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-2523">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="cd17d-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cd17d-2524">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2524">Fix some error messages.</span></span>
* <span data-ttu-id="cd17d-2525">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cd17d-2526">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd17d-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-2527">Az.SignalR</span></span>
* <span data-ttu-id="cd17d-2528">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2529">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2530">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd17d-2531">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cd17d-2532">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="cd17d-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cd17d-2533">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="cd17d-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2534">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2535">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd17d-2536">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cd17d-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cd17d-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cd17d-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cd17d-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cd17d-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd17d-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="cd17d-2540">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2541">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2542">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cd17d-2543">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cd17d-2544">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cd17d-2545">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="cd17d-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cd17d-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2546">Az.Accounts</span></span>
* <span data-ttu-id="cd17d-2547">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2548">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2549">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cd17d-2550">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cd17d-2551">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2553">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cd17d-2554">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cd17d-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd17d-2555">Az.EventGrid</span></span>
* <span data-ttu-id="cd17d-2556">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cd17d-2557">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="cd17d-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cd17d-2558">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd17d-2559">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="cd17d-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd17d-2560">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cd17d-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd17d-2561">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cd17d-2562">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cd17d-2563">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="cd17d-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cd17d-2564">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="cd17d-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cd17d-2565">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cd17d-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="cd17d-2566">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cd17d-2567">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="cd17d-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cd17d-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cd17d-2568">Az.IotHub</span></span>
* <span data-ttu-id="cd17d-2569">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cd17d-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cd17d-2570">Az.LogicApp</span></span>
* <span data-ttu-id="cd17d-2571">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="cd17d-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2572">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2573">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cd17d-2574">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="cd17d-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cd17d-2575">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd17d-2576">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cd17d-2577">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cd17d-2578">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="cd17d-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cd17d-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-2579">Az.SignalR</span></span>
* <span data-ttu-id="cd17d-2580">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2581">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2582">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cd17d-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2583">Az.Storage</span></span>
* <span data-ttu-id="cd17d-2584">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cd17d-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd17d-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="cd17d-2586">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="cd17d-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cd17d-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cd17d-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2588">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2589">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cd17d-2590">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cd17d-2591">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cd17d-2592">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-2592">General</span></span>

- <span data-ttu-id="cd17d-2593">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="cd17d-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="cd17d-2594">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="cd17d-2594">Online help for each module</span></span>
- <span data-ttu-id="cd17d-2595">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cd17d-2596">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cd17d-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cd17d-2597">Az.Accounts</span></span>
- <span data-ttu-id="cd17d-2598">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="cd17d-2599">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd17d-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="cd17d-2601">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="cd17d-2601">Fixes for #7002</span></span>
- <span data-ttu-id="cd17d-2602">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cd17d-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cd17d-2603">Az.Batch</span></span>
- <span data-ttu-id="cd17d-2604">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cd17d-2605">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cd17d-2606">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cd17d-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cd17d-2607">Az.Billing</span></span>
- <span data-ttu-id="cd17d-2608">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cd17d-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="cd17d-2610">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cd17d-2611">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd17d-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="cd17d-2613">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cd17d-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cd17d-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cd17d-2615">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="cd17d-2617">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cd17d-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2618">Az.Monitor</span></span>
- <span data-ttu-id="cd17d-2619">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cd17d-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd17d-2620">Az.KeyVault</span></span>
- <span data-ttu-id="cd17d-2621">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cd17d-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cd17d-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="cd17d-2623">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cd17d-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cd17d-2624">Az.Media</span></span>
- <span data-ttu-id="cd17d-2625">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd17d-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2626">Az.Network</span></span>
<span data-ttu-id="cd17d-2627">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cd17d-2628">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="cd17d-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cd17d-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cd17d-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cd17d-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd17d-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cd17d-2637">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cd17d-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd17d-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cd17d-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd17d-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cd17d-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cd17d-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cd17d-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cd17d-2643">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cd17d-2644">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cd17d-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cd17d-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd17d-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd17d-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd17d-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cd17d-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd17d-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cd17d-2648">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cd17d-2649">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cd17d-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="cd17d-2651">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cd17d-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2652">Az.Profile</span></span>
- <span data-ttu-id="cd17d-2653">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="cd17d-2655">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cd17d-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2656">Az.Resources</span></span>
- <span data-ttu-id="cd17d-2657">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd17d-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="cd17d-2659">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="cd17d-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cd17d-2660">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cd17d-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="cd17d-2662">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cd17d-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cd17d-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2663">Az.Sql</span></span>
- <span data-ttu-id="cd17d-2664">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cd17d-2665">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cd17d-2666">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd17d-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2667">Az.Storage</span></span>
- <span data-ttu-id="cd17d-2668">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd17d-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2669">Az.Websites</span></span>
- <span data-ttu-id="cd17d-2670">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="cd17d-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cd17d-2671">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cd17d-2672">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-2672">General</span></span>

* <span data-ttu-id="cd17d-2673">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="cd17d-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd17d-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2674">Az.Compute</span></span>

* <span data-ttu-id="cd17d-2675">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="cd17d-2677">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cd17d-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cd17d-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="cd17d-2679">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="cd17d-2680">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cd17d-2681">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cd17d-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="cd17d-2683">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cd17d-2684">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd17d-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2685">Az.Resources</span></span>

* <span data-ttu-id="cd17d-2686">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="cd17d-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cd17d-2687">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cd17d-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2688">Az.Sql</span></span>

* <span data-ttu-id="cd17d-2689">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="cd17d-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cd17d-2690">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cd17d-2691">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cd17d-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2692">Az.Storage</span></span>

* <span data-ttu-id="cd17d-2693">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cd17d-2694">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cd17d-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd17d-2696">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="cd17d-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd17d-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cd17d-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cd17d-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cd17d-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2699">Az.Websites</span></span>

* <span data-ttu-id="cd17d-2700">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cd17d-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="cd17d-2701">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cd17d-2702">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cd17d-2703">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cd17d-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd17d-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="cd17d-2705">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cd17d-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cd17d-2706">Az.Automation</span></span>
* <span data-ttu-id="cd17d-2707">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd17d-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cd17d-2708">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cd17d-2709">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cd17d-2710">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cd17d-2711">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cd17d-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2712">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2713">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cd17d-2714">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cd17d-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="cd17d-2716">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cd17d-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cd17d-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cd17d-2718">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cd17d-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2719">Az.Network</span></span>
* <span data-ttu-id="cd17d-2720">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="cd17d-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cd17d-2721">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cd17d-2722">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="cd17d-2723">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cd17d-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd17d-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cd17d-2725">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cd17d-2726">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cd17d-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cd17d-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cd17d-2728">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cd17d-2729">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cd17d-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cd17d-2730">Az.Relay</span></span>
* <span data-ttu-id="cd17d-2731">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cd17d-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2732">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2733">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cd17d-2734">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cd17d-2735">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="cd17d-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cd17d-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-2737">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cd17d-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2738">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2739">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cd17d-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd17d-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd17d-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd17d-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="cd17d-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cd17d-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd17d-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd17d-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd17d-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd17d-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd17d-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cd17d-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="cd17d-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cd17d-2748">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cd17d-2749">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="cd17d-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cd17d-2750">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cd17d-2751">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="cd17d-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd17d-2752">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="cd17d-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cd17d-2753">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="cd17d-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cd17d-2754">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="cd17d-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cd17d-2755">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cd17d-2756">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cd17d-2757">Allgemein</span><span class="sxs-lookup"><span data-stu-id="cd17d-2757">General</span></span>
* <span data-ttu-id="cd17d-2758">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cd17d-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2759">Az.Profile</span></span>
* <span data-ttu-id="cd17d-2760">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cd17d-2761">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cd17d-2762">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cd17d-2763">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cd17d-2764">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cd17d-2765">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cd17d-2766">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="cd17d-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-2768">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2769">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2770">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cd17d-2771">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="cd17d-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cd17d-2772">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2774">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="cd17d-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cd17d-2775">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cd17d-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2776">Az.Insights</span></span>
* <span data-ttu-id="cd17d-2777">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cd17d-2778">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cd17d-2779">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cd17d-2780">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2781">Az.Network</span></span>
* <span data-ttu-id="cd17d-2782">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="cd17d-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cd17d-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cd17d-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cd17d-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd17d-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cd17d-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cd17d-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cd17d-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cd17d-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cd17d-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cd17d-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd17d-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="cd17d-2790">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2791">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2792">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="cd17d-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cd17d-2793">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="cd17d-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cd17d-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd17d-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="cd17d-2795">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="cd17d-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cd17d-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd17d-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="cd17d-2797">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cd17d-2798">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="cd17d-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cd17d-2799">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cd17d-2800">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="cd17d-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cd17d-2801">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cd17d-2802">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cd17d-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2803">Az.Profile</span></span>
* <span data-ttu-id="cd17d-2804">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cd17d-2805">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2806">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2807">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="cd17d-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cd17d-2808">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cd17d-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd17d-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="cd17d-2810">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cd17d-2811">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cd17d-2812">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd17d-2813">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cd17d-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2815">Az.Network</span></span>
* <span data-ttu-id="cd17d-2816">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cd17d-2817">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2818">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2819">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cd17d-2820">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cd17d-2821">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cd17d-2822">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2822">Azure.Storage</span></span>
* <span data-ttu-id="cd17d-2823">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cd17d-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cd17d-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cd17d-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cd17d-2826">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cd17d-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cd17d-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cd17d-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cd17d-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="cd17d-2829">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cd17d-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cd17d-2830">Az.Compute</span></span>
* <span data-ttu-id="cd17d-2831">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="cd17d-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cd17d-2832">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cd17d-2833">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cd17d-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cd17d-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cd17d-2835">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cd17d-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cd17d-2836">Az.Network</span></span>
* <span data-ttu-id="cd17d-2837">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cd17d-2838">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2838">new cmdlets added</span></span>
    - <span data-ttu-id="cd17d-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd17d-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd17d-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd17d-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cd17d-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cd17d-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cd17d-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd17d-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cd17d-2845">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cd17d-2846">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cd17d-2847">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cd17d-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cd17d-2848">Az.RedisCache</span></span>
* <span data-ttu-id="cd17d-2849">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="cd17d-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cd17d-2850">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cd17d-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cd17d-2851">Az.Resources</span></span>
* <span data-ttu-id="cd17d-2852">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="cd17d-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cd17d-2853">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="cd17d-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cd17d-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cd17d-2854">Az.Sql</span></span>
* <span data-ttu-id="cd17d-2855">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="cd17d-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cd17d-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cd17d-2856">Az.Websites</span></span>
* <span data-ttu-id="cd17d-2857">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="cd17d-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cd17d-2858">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="cd17d-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cd17d-2859">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="cd17d-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cd17d-2860">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="cd17d-2860">Initial Release</span></span>
