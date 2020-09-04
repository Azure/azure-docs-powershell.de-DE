---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244227"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="3f978-103">Versionshinweise zu Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3f978-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="3f978-104">4.6.1: August 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="3f978-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-105">Az.Compute</span></span>
* <span data-ttu-id="3f978-106">Patch für Parameter „-EncryptionAtHost“ in „New-AzVm“, um den Standardwert „false“ zu entfernen [Nr. 12776]</span><span class="sxs-lookup"><span data-stu-id="3f978-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="3f978-107">4.6.0: August 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-108">Az.Accounts</span></span>
* <span data-ttu-id="3f978-109">Alle öffentlichen Cloudumgebungen geladen, wenn der Ermittlungsendpunkt keine standardmäßigen AzureCloud-Umgebungen oder anderen öffentlichen Umgebungen zurückgibt [Nr. 12633]</span><span class="sxs-lookup"><span data-stu-id="3f978-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="3f978-110">SubscriptionPolicies in „Get-AzSubscription“ verfügbar gemacht [Nr. 12551]</span><span class="sxs-lookup"><span data-stu-id="3f978-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-111">Az.Automation</span></span>
* <span data-ttu-id="3f978-112">Parameter „-RunOn“ zu „Set-AzAutomationWebhook“ hinzugefügt, um eine Hybrid Worker-Gruppe anzugeben</span><span class="sxs-lookup"><span data-stu-id="3f978-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-113">Az.Compute</span></span>
* <span data-ttu-id="3f978-114">Parameter „-EncryptionAtHost“ zu „New-AzVm“, „New-AzVmss“, „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="3f978-115">„SecurityProfile“ zu Rückgabeobjekt „Get-AzVM“ und „Get-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="3f978-116">Switch „-InstanceView“ als optionalen Parameter zu „Get-AzHostGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="3f978-117">Neues Cmdlet „Invoke-AzVmPatchAssessment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-118">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-119">Fehlende Eigenschaften zur PSPipelineRun-Klasse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-120">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-121">Unterstützung für das Erstellen eines Clusters mit dem Feature für Verschlüsselung auf dem Host</span><span class="sxs-lookup"><span data-stu-id="3f978-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-122">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-123">Warnmeldungen für geplante Deaktivierung des vorläufigen Löschens hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="3f978-124">Warnmeldungen für die geplante Entfernung des Attributs „SecretValueText“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="3f978-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="3f978-125">Az.Maintenance</span></span>
* <span data-ttu-id="3f978-126">Optionale zeitplanbezogene Felder zu „New-AzMaintenanceConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="3f978-127">Neues Cmdlet für „Get-AzMaintenancePublicConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3f978-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3f978-128">Az.ManagedServices</span></span>
* <span data-ttu-id="3f978-129">Breaking Change-Warnungen zu Cmdlets für die Zuweisung und Definition von verwalteten Diensten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-130">Az.Monitor</span></span>
* <span data-ttu-id="3f978-131">Parametersatz in „Set-AzDiagnosticSetting“ zur Trennung der Aktivierung von Protokollen und Metriken erweitert [Nr. 12482]</span><span class="sxs-lookup"><span data-stu-id="3f978-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="3f978-132">Fehler für „Add-AzMetricAlertRuleV2“ behoben, der beim Abrufen einer Metrikwarnung aus der Pipeline auftrat</span><span class="sxs-lookup"><span data-stu-id="3f978-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-133">Az.Resources</span></span>
* <span data-ttu-id="3f978-134">Antwort auf „Get-AzPolicyAlias“ aktualisiert. Sie enthält nun Informationen dazu, ob der Alias von Azure Policy geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f978-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="3f978-135">Neues Cmdlet „Set-AzRoleAssignment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="3f978-136">„Get-AzDeploymentManagementGroupWhatIfResult“ zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Verwaltungsgruppenbereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="3f978-137">Neues Cmdlet „Get-AzTenantWhatIfResult“ zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Mandantenbereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="3f978-138">Parameter „-WhatIf“ und „-Confirm“ für „New-AzManagementGroupDeployment“ und „New-AzTenantDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben</span><span class="sxs-lookup"><span data-stu-id="3f978-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="3f978-139">Verhalten von „-WhatIf“ und „-Confirm“ für neue Bereitstellungs-Cmdlets korrigiert (abgestimmt auf „False“ und</span><span class="sxs-lookup"><span data-stu-id="3f978-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="3f978-140">Serialisierungsfehler für „-TemplateObject“ und „TemplateParameterObject“ behoben [Nr. 1528] [Nr. 6292]</span><span class="sxs-lookup"><span data-stu-id="3f978-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="3f978-141">Breaking Change-Attribut zu „Get-AzResourceGroupDeploymentOperation“ für anstehende Ausgabetypänderung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3f978-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3f978-142">Az.SignalR</span></span>
* <span data-ttu-id="3f978-143">Fehler in Hilfedateien für „Restart-AzSignalR“ und „Update-AzSignalR behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="3f978-144">Cmdlets „Update-AzSignalRNetworkAcl“ und „Set-AzSignalRUpstream“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-145">Az.Storage</span></span>
* <span data-ttu-id="3f978-146">Unterstützung für die Beschleunigung von Blobabfragen</span><span class="sxs-lookup"><span data-stu-id="3f978-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="3f978-147">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="3f978-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="3f978-148">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="3f978-149">Hilfedatei aktualisiert, ausführlichere Beschreibung hinzugefügt und Tippfehler korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="3f978-150">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="3f978-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="3f978-151">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="3f978-152">Fehler beim Blobdownload behoben, der auftrat, wenn das zugehörige Unterverzeichnis nicht vorhanden ist [Nr. 12592]</span><span class="sxs-lookup"><span data-stu-id="3f978-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="3f978-153">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="3f978-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="3f978-154">Unterstützung für das Festlegen/Abrufen/Entfernen der Objektreplikationsrichtlinie für Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="3f978-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="3f978-155">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3f978-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="3f978-156">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="3f978-157">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="3f978-158">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="3f978-159">Unterstützung für das Aktivieren/Deaktivieren des Änderungsfeeds für den Blobdienst eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="3f978-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="3f978-160">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="3f978-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="3f978-161">4.5.0: August 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-162">Az.Accounts</span></span>
* <span data-ttu-id="3f978-163">„Connect-AzAccount“ wurde aktualisiert und akzeptiert nun den Parameter „MaxContextPopulation“. [Nr. 9865]</span><span class="sxs-lookup"><span data-stu-id="3f978-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="3f978-164">SubscriptionClient-Version auf 2019-06-01 aktualisiert und Anzeigen von Mandantendomänen [Nr. 9838]</span><span class="sxs-lookup"><span data-stu-id="3f978-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="3f978-165">Unterstützung für Informationen des Home- und des managedBy-Mandanten des Abonnements</span><span class="sxs-lookup"><span data-stu-id="3f978-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="3f978-166">Modulname, Versionsinformationen in Telemetriedaten korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="3f978-167">SqlDatabaseDnsSuffix und ServiceManagementUrl angepasst, wenn Umgebungsmetadatenendpunkt inkompatiblen Wert zurückgibt</span><span class="sxs-lookup"><span data-stu-id="3f978-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-168">Az.Aks</span></span>
* <span data-ttu-id="3f978-169">„ClientIdAndSecret“ bis „ServicePrincipalIdAndSecret“ entfernt und „ClientIdAndSecret“ als Alias festgelegt [Nr. 12381].</span><span class="sxs-lookup"><span data-stu-id="3f978-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="3f978-170">„Get-AzAks“/„New-AzAks“/“Remove-AzAks“/„Set-AzAks“ bis „Get-AzAksCluster“/„New-AzAksCluster“/„Remove-AzAksCluster“/„Set-AzAksCluster“ entfernt und ursprüngliche Cmdlets als Alias festgelegt [Nr. 12373].</span><span class="sxs-lookup"><span data-stu-id="3f978-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-171">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-172">Neues Cmdlet „Add-AzApiManagementApiToGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-173">Neues Cmdlet „Get-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-174">Neues Cmdlet „Get-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3f978-175">Neues Cmdlet „Get-AzApiManagementGatewayKey“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="3f978-176">Neues Cmdlet „New-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-177">Neues Cmdlet „New-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3f978-178">Neues Cmdlet „New-AzApiManagementResourceLocationObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="3f978-179">Neues Cmdlet „Remove-AzApiManagementApiFromGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-180">Neues Cmdlet „Remove-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-181">Neues Cmdlet „Remove-AzApiManagementGatewayHostnameConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="3f978-182">Neues Cmdlet „Update-AzApiManagementGateway“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="3f978-183">Neuer optionaler Parameter „[-GatewayId]“ zum Cmdlet „Get-AzApiManagementApi“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-185">„Deny“ speziell als NetworkRules-Standardaktion verwendet</span><span class="sxs-lookup"><span data-stu-id="3f978-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-186">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-187">Problem behoben, aufgrund dessen eine Ausnahme ausgelöst wird, wenn Enum.Parse versucht, einen NULL-Wert in Enumerationswerte vom Typ „Enabled“ oder „Disabled“ umzuwandeln [Nr. 12344]</span><span class="sxs-lookup"><span data-stu-id="3f978-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-188">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-189">Unterstützung für das Erstellen eines Clusters mit dem Feature für Verschlüsselung während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="3f978-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="3f978-190">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="3f978-191">Neuer Parameter „EncryptionInTransit“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="3f978-192">Unterstützung für das Erstellen eines Clusters mit der Funktion für private Links:</span><span class="sxs-lookup"><span data-stu-id="3f978-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="3f978-193">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightCluster“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="3f978-194">Neue Parameter „PublicNetworkAccessType“ und „OutboundPublicNetworkAccessType“ zum Cmdlet „New-AzHDInsightClusterConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="3f978-195">Beim Aufruf von „New-AzHDInsightCluster“ oder „Get-AzHDInsightCluster“ werden Informationen zum virtuellen Netzwerk zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-196">Az.Network</span></span>
* <span data-ttu-id="3f978-197">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="3f978-198">Nonbreaking Changes hinzugefügt: PeerAddressType-Funktion für privates Peering in „Remove-AzExpressRouteCircutPeeringConfig“</span><span class="sxs-lookup"><span data-stu-id="3f978-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="3f978-199">Code geändert, um die Groß-/Kleinschreibung für die Parameter „AddressPrefixType“ und „PeerAddressType“ zu ignorieren</span><span class="sxs-lookup"><span data-stu-id="3f978-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="3f978-200">Warnmeldung für „New-AzLoadBalancerFrontendIpConfig“, „New-AzPublicIpAddress“ und „New-AzPublicIpPrefix“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-202">Option „-ForceDelete“ für „Remove-AzOperationalInsightsworkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="3f978-203">Neues Cmdlet „Get-AzOperationalInsightsDeletedWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="3f978-204">Neues Cmdlet „Restore-AzOperationalInsightsWorkspace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-206">Ermittlung von Azure Backup-Containern/-Elementen verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-207">Az.Resources</span></span>
* <span data-ttu-id="3f978-208">Eigenschaften „Condition“, „ConditionVersion“ und „Description“ zu „New-AzRoleAssignment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="3f978-209">Dies enthielt alle relevanten Änderungen an den Datenmodellen.</span><span class="sxs-lookup"><span data-stu-id="3f978-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-210">Az.Sql</span></span>
* <span data-ttu-id="3f978-211">Potenzieller Fehler aufgrund der Nichtbeachtung von Groß-/Kleinschreibung beim Servernamen in „New-AzSqlServer“ und „Set-AzSqlServer“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="3f978-212">Fehler behoben, aufgrund dessen in „New-AzSqlDatabaseSecondary“ ein falscher Datenbankname für eine vorhandene Datenbank zurückgegeben wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-213">Az.Storage</span></span>
* <span data-ttu-id="3f978-214">Erstellen von Container-/Blob-SAS-Token mit neuer Berechtigung x,t unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="3f978-215">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="3f978-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="3f978-216">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="3f978-217">Erstellen von Konto-SAS-Token mit neuer Berechtigung x,t,f unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="3f978-218">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="3f978-219">Abrufen der Nutzung einer einzelnen Dateifreigabe unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="3f978-220">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="3f978-221">4.4.0 – Juli 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-222">Az.Accounts</span></span>
* <span data-ttu-id="3f978-223">Neues Cmdlet „Invoke-AzRestMethod“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="3f978-224">Ein Problem wurde behoben, das Authentifizierungsfehler in Szenarien mit mehreren Prozessen verursachen konnte, z. B. beim Ausführen mehrerer Azure PowerShell-Cmdlets mithilfe von „Start-Job“ [Nr. 9448].</span><span class="sxs-lookup"><span data-stu-id="3f978-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-225">Az.Aks</span></span>
* <span data-ttu-id="3f978-226">Fehler behoben: „Get-AzAks“ ruft nicht alle Cluster ab [Nr. 12296]</span><span class="sxs-lookup"><span data-stu-id="3f978-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="3f978-228">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-229">Az.Automation</span></span>
* <span data-ttu-id="3f978-230">Das Problem wurde behoben, dass die Zeichenfolge mit Escapezeichen nicht in das JSON-Objekt konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f978-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-231">Az.Compute</span></span>
* <span data-ttu-id="3f978-232">Beim Verwenden von „New-azvmss“ ohne die Imageversion „latest“ wurde eine Warnung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-233">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-234">Globale Parameter zu Data Factory hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3f978-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3f978-235">Az.EventGrid</span></span>
* <span data-ttu-id="3f978-236">Zur Verwendung der API-Version 2020-06-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="3f978-237">Neue Funktionen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-237">Added new features:</span></span>
    - <span data-ttu-id="3f978-238">Eingabezuordnung</span><span class="sxs-lookup"><span data-stu-id="3f978-238">Input mapping</span></span>
    - <span data-ttu-id="3f978-239">Schema für Ereignisbereitstellung</span><span class="sxs-lookup"><span data-stu-id="3f978-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="3f978-240">Private Link</span><span class="sxs-lookup"><span data-stu-id="3f978-240">Private Link</span></span>
    - <span data-ttu-id="3f978-241">Cloud Event V10-Schema</span><span class="sxs-lookup"><span data-stu-id="3f978-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="3f978-242">Service Bus-Thema as Ziel</span><span class="sxs-lookup"><span data-stu-id="3f978-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="3f978-243">Azure-Funktion als Ziel</span><span class="sxs-lookup"><span data-stu-id="3f978-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="3f978-244">WebHook-Batchverarbeitung</span><span class="sxs-lookup"><span data-stu-id="3f978-244">WebHook Batching</span></span>
    - <span data-ttu-id="3f978-245">Sicherer Webhook (AAD-Unterstützung)</span><span class="sxs-lookup"><span data-stu-id="3f978-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="3f978-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="3f978-246">IpFiltering</span></span>
* <span data-ttu-id="3f978-247">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="3f978-248">„New-AzEventGridSubscription“/„Update-AzEventGridSubscription“:</span><span class="sxs-lookup"><span data-stu-id="3f978-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="3f978-249">Neue optionale Parameter zur Unterstützung der Webhook-Batchverarbeitung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="3f978-250">Neue optionale Parameter zur Unterstützung der Batchverarbeitung gesicherter Webhooks mithilfe von AAD hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="3f978-251">Neue Enumeration für den EndpointType-Parameter hinzufügen, um das Azure-Funktions-und Service Bus-Thema als neue Ziele zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="3f978-252">Neuen optionalen Parameter für das Zustellungsschema hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="3f978-253">„New-AzEventGridTopic“/„Update-AzEventGridTopic“ und „New-AzEventGridDomain“/„Update-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="3f978-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="3f978-254">Neue optionale Parameter zur Unterstützung von IpFiltering hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="3f978-255">„New-AzEventGridTopic“/„New-AzEventGridDomain“:</span><span class="sxs-lookup"><span data-stu-id="3f978-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="3f978-256">Neue optionale Parameter zur Unterstützung von Eingabezuordnung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-257">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-258">Modul zur Verwendung von API 2020-05-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="3f978-259">Unterstützung für private Links für Storage-, Keyvault- und Web App Service-Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-260">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-261">Erstellen eines Clusters mit ADLSGen1/2-Speicher in nationalen Clouds unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-262">Az.Monitor</span></span>
* <span data-ttu-id="3f978-263">Fehler für „Get-AzDiagnosticSetting“ behoben, wenn Metriken oder Protokolle NULL sind [Nr. 12272]</span><span class="sxs-lookup"><span data-stu-id="3f978-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-264">Az.Network</span></span>
* <span data-ttu-id="3f978-265">Austausch von Parametern in VWan-HubVnet-Verbindung-korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="3f978-266">Neue Cmdlets für Sites von virtuellen Azure-Netzwerkgeräten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="3f978-267">„Get-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="3f978-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3f978-268">„New-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="3f978-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3f978-269">„Remove-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="3f978-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3f978-270">„Update-AzVirtualApplianceSite“</span><span class="sxs-lookup"><span data-stu-id="3f978-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="3f978-271">„New-AzOffice365PolicyProperty“</span><span class="sxs-lookup"><span data-stu-id="3f978-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="3f978-272">Neue Cmdlets für virtuelle Azure-Netzwerkgeräte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="3f978-273">„Get-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="3f978-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3f978-274">„New-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="3f978-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3f978-275">„Remove-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="3f978-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3f978-276">„Update-AzNetworkVirtualAppliance“</span><span class="sxs-lookup"><span data-stu-id="3f978-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="3f978-277">„Get-AzNetworkVirtualApplianceSku“</span><span class="sxs-lookup"><span data-stu-id="3f978-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="3f978-278">„New-AzVirtualApplianceSkuProperty“</span><span class="sxs-lookup"><span data-stu-id="3f978-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="3f978-279">Onboarding für Application Gateway für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="3f978-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="3f978-280">Onboarding für StorageSync für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="3f978-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="3f978-281">Onboarding für SignalR für gemeinsam verwendete Private Link-Cmdlets durchgeführt</span><span class="sxs-lookup"><span data-stu-id="3f978-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-283">Projektverweis auf Authentifizierung entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="3f978-284">Azure Backup hat Cmdlets optimiert, um den Text genauer zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="3f978-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="3f978-285">Azure Backup hat Unterstützung für das Abrufen von MAB-Agent-Aufträgen mithilfe des Cmdlets „Get-AzRecoveryServicesBackupJob“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-286">Az.Resources</span></span>
* <span data-ttu-id="3f978-287">„Save-azresourcegroupdeploymenttemplate“ auf Verwendung des SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="3f978-288">Cmdlet „Unregister-AzResourceProvider“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-289">Az.Sql</span></span>
* <span data-ttu-id="3f978-290">Unterstützung für Dienstprinzipal und Gastbenutzer im Cmdlet „Set-AzSqlInstanceActiveDirectoryAdministrator“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="3f978-291">Problem in Data Classification-Cmdlets behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="3f978-292">Unterstützung für Azure SQL Managed Instance-Failover hinzugefügt: „Invoke-AzSqlInstanceFailover“</span><span class="sxs-lookup"><span data-stu-id="3f978-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-293">Az.Storage</span></span>
* <span data-ttu-id="3f978-294">Problem behoben, dass UserAgent für einige Datenebenen-Cmdlets nicht hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="3f978-295">Erstellen/Aktualisieren eines Storage-Kontos mit „MinimumTlsVersion“ und „AllowBlobPublicAccess“ unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="3f978-296">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="3f978-297">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-298">Aktivieren/Deaktivieren der Versionsverwaltung für Blobdienst eines Storage-Kontos unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="3f978-299">„Update-AzStorageBlobServiceProperty“</span><span class="sxs-lookup"><span data-stu-id="3f978-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="3f978-300">Auflisten von Blobs mit Blobversionen unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="3f978-301">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="3f978-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="3f978-302">Abrufen/Entfernen einer einzelnen Blob-Momentaufnahme oder Blobversion unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="3f978-303">„Get-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="3f978-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="3f978-304">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="3f978-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="3f978-305">Pipeline aus Blobobjekt unterstützen, das aus Azure.Storage.Blobs V12 generiert wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="3f978-306">„Get-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="3f978-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="3f978-307">„New-AzStorageBlobSASToken“</span><span class="sxs-lookup"><span data-stu-id="3f978-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="3f978-308">„Remove-AzStorageBlob“</span><span class="sxs-lookup"><span data-stu-id="3f978-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="3f978-309">„Set-AzStorageBlobContent“</span><span class="sxs-lookup"><span data-stu-id="3f978-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="3f978-310">„Start-AzStorageBlobCopy“</span><span class="sxs-lookup"><span data-stu-id="3f978-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3f978-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3f978-311">Az.StorageSync</span></span>
* <span data-ttu-id="3f978-312">Neue Version von StorageSync SDK für ApiVersion 2020-03-01 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="3f978-313">Cmdlet „Update Storage Sync Service“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="3f978-314">„Set-AzStorageSyncService“</span><span class="sxs-lookup"><span data-stu-id="3f978-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="3f978-315">„IncomingTrafficPolicy“ und „PrivateEndpointConnections“ zu StorageSyncService-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-316">Az.Websites</span></span>
* <span data-ttu-id="3f978-317">Unterstützung zur Durchführung von Vorgängen für Slots hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="3f978-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="3f978-318">4.3.0 – Juni 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-319">Az.Accounts</span></span>
* <span data-ttu-id="3f978-320">Standardmäßige Unterstützung der Einstellung der Erkennungsumgebung und das Hinzufügen der Umgebung über „Add-AzEnvironment“</span><span class="sxs-lookup"><span data-stu-id="3f978-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="3f978-321">Aktualisieren von vorgeladenen Assemblys [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="3f978-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="3f978-322">Assembly „Azure.Core“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="3f978-323">Fehler behoben, der dazu führen konnte, dass „Connect-AzAccount“ in der Multithread-Ausführung fehlschlägt [#11201]</span><span class="sxs-lookup"><span data-stu-id="3f978-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-324">Az.Aks</span></span>
* <span data-ttu-id="3f978-325">Ersetzen der Verwendung der alten [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) durch Aufrufe der [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials)- und [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)-APIs</span><span class="sxs-lookup"><span data-stu-id="3f978-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-326">Az.Batch</span></span>
* <span data-ttu-id="3f978-327">Az.Batch für die Verwendung der Microsoft.Azure.Management.Batch-SDK-Version auf 11.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="3f978-328">Möglichkeit zum Festlegen der BatchAccount-Identität im Cmdlet „New-AzBatchAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-330">Anzeige von Kontofunktionen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="3f978-331">Ändern von PublicNetworkAccess wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-332">Az.Compute</span></span>
* <span data-ttu-id="3f978-333">Parameter „SimulateEviction“ wurde den Cmdlets „Set-AzVM“ und „Set-AzVmssVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="3f978-334">„Premium_LRS“ wurde zur Argumentvervollständigung des StorageAccountType-Parameters für das Cmdlet „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="3f978-335">Unterstatus zu VMCustomScriptExtension hinzugefügt [#11297]</span><span class="sxs-lookup"><span data-stu-id="3f978-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="3f978-336">„Delete“ wurde zur Argumentvervollständigung des EvictionPolicy-Parameters für die Cmdlets „New-AzVM“ und „New-AzVMConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="3f978-337">Name der neuen VM-Erweiterung für SAP korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-338">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-339">ADF .Net-SDK-Version auf 4.9.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-340">Az.EventHub</span></span>
* <span data-ttu-id="3f978-341">Parameter der verwalteten Identität zu Cmdlets „New-AzEventHubNamespace“ und „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="3f978-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="3f978-342">Az.Functions</span></span>
* <span data-ttu-id="3f978-343">Unterstützung zum Erstellen von PowerShell 7.0- und Java 11-Funktions-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-344">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-345">Listenhosts unterstützt und bestimmte Hosts des HDInsight-Clusters neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="3f978-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3f978-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3f978-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="3f978-347">SDK-Version auf 1.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="3f978-348">Unterstützung für Exporteinstellungen und verwaltete Identität hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-349">Az.Monitor</span></span>
* <span data-ttu-id="3f978-350">Eingabeobjektparameter für „Set-AzActivityLogAlert“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="3f978-351">InputObject-Parameter für „Set-AzActionGroup“ korrigiert [#10868]</span><span class="sxs-lookup"><span data-stu-id="3f978-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-352">Az.Network</span></span>
* <span data-ttu-id="3f978-353">Unterstützung für den AddressPrefixType-Parameter zu „Remove-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="3f978-354">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="3f978-355">„New-AzFirewallPolicyDnsSetting“</span><span class="sxs-lookup"><span data-stu-id="3f978-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="3f978-356">Unterstützung für Ziel-FQDN in Netzwerkregeln für Firewallrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3f978-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="3f978-357">Unterstützung für Back-End-Adresspool-Vorgänge hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="3f978-358">„New-AzLoadBalancerBackendAddressConfig“</span><span class="sxs-lookup"><span data-stu-id="3f978-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="3f978-359">„New-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="3f978-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3f978-360">„Set-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="3f978-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3f978-361">„Remove-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="3f978-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="3f978-362">„Get-AzLoadBalancerBackendAddressPool“</span><span class="sxs-lookup"><span data-stu-id="3f978-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="3f978-363">Namensvalidierung für „New-AzIpGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="3f978-364">Neue Cmdlets für „Azure FirewallPolicy“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="3f978-365">„New-AzFirewallPolicyThreatIntelWhitelist“</span><span class="sxs-lookup"><span data-stu-id="3f978-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="3f978-366">Folgende Befehle für das Feature aktualisiert: Festlegen/Entfernen von benutzerdefinierten DNS-Servern auf „VirtualWan P2SVpnGateway“.</span><span class="sxs-lookup"><span data-stu-id="3f978-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="3f978-367">„New-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="3f978-368">„Update-AzP2sVpnGateway“ aktualisiert: Der optionale Parameter „-CustomDnsServer“ wurde hinzugefügt, damit Kunden ihre DNS-Server angeben können, die auf „P2SVpnGateway“ festgelegt werden. Diese können von Point-to-Site-Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="3f978-369">„Update-AzVpnGateway“ aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="3f978-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="3f978-370">Der optionale Parameter „-BgpPeeringAddress“ wurde hinzugefügt, damit Kunden ihre benutzerdefinierten BGSs angeben können, die auf „VpnGateway“ festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="3f978-371">Neues Cmdlet hinzugefügt, um das Zurücksetzen des Routingstatus einer VirtualHub-Ressource zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="3f978-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="3f978-372">„Reset-AzHubRouter“</span><span class="sxs-lookup"><span data-stu-id="3f978-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="3f978-373">Folgendes wurde basierend auf der aktuellen Swagger-Änderung für die Firewallrichtlinie aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="3f978-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="3f978-374">Namen für „RuleGroup“, „RuleCollectionGroup“ und „RuleType“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="3f978-375">Unterstützung für NAT-Regelsammlungen der Firewallrichtlinie zur Unterstützung mehrerer NAT-Regelsammlungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="3f978-376">[Breaking Change] Obligatorischer Parameter „SourceIpGroup“ für „New-AzFirewallPolicyApplicationRule“ und „New-AzFirewallPolicyNetworkRule“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="3f978-377">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="3f978-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="3f978-378">[Breaking Change] Parameter „New-AzFirewallPolicyApplicationRule“ korrigiert, „SourceAddress“ ist jetzt obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="3f978-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="3f978-379">[Breaking Change] Obligatorische Parameter entfernt: „TranslatedAddress“, „TranslatedPort“ für „New-AzFirewallPolicyNatRuleCollection“.</span><span class="sxs-lookup"><span data-stu-id="3f978-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="3f978-380">Neue Cmdlets zur Unterstützung von „PrivateLink“ auf Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="3f978-381">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3f978-382">„Get-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3f978-383">„New-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3f978-384">„Set-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3f978-385">„Remove-AzApplicationGatewayPrivateLinkConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="3f978-386">„New-AzApplicationGatewayPrivateLinkIpConfiguration“</span><span class="sxs-lookup"><span data-stu-id="3f978-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="3f978-387">Neue Cmdlets für untergeordnete Ressource „HubRouteTables“ von „VirtualHub“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="3f978-388">„New-AzVHubRoute“</span><span class="sxs-lookup"><span data-stu-id="3f978-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="3f978-389">„New-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3f978-390">„Get-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3f978-391">„Update-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="3f978-392">„Remove-AzVHubRouteTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="3f978-393">Vorhandene Cmdlets aktualisiert, sodass sie den optionalen Eingabeparameter „RoutingConfiguration“ für benutzerdefiniertes Routing in „VirtualWan“ unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="3f978-394">„New-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="3f978-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="3f978-395">„Set-AzExpressRouteConnection“</span><span class="sxs-lookup"><span data-stu-id="3f978-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="3f978-396">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3f978-397">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3f978-398">„New-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="3f978-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="3f978-399">„Update-AzVpnConnection“</span><span class="sxs-lookup"><span data-stu-id="3f978-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="3f978-400">„New-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="3f978-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="3f978-401">„Update-AzP2sVpnGateway“</span><span class="sxs-lookup"><span data-stu-id="3f978-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-403">Fehler behoben: „PSWorkspace“ implementiert „IOperationalInsightsWorkspace“ nicht [#12135]</span><span class="sxs-lookup"><span data-stu-id="3f978-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="3f978-404">„pergb2018“ wurde dem gültigen Satz des Parameters „Sku“ in „Set-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="3f978-405">Der Alias „FunctionParameters“ für den Parameter „FunctionParameter“ wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="3f978-406">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3f978-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="3f978-407">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3f978-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-409">Azure Backup hat Unterstützung für das Abrufen von MAB-Elementen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="3f978-410">Azure Site Recovery unterstützt Datenträgertyp „StandardSSD_LRS“.</span><span class="sxs-lookup"><span data-stu-id="3f978-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-411">Az.Resources</span></span>
* <span data-ttu-id="3f978-412">„UsageLocation“, „GivenName“, „Surname“, „AccountEnabled“, „MailNickname“, „Mail“ in „PSADUser“ hinzugefügt [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="3f978-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="3f978-413">Problem behoben, dass „-Mail“ für „Get-AzADUser“ nicht funktioniert [#11981]</span><span class="sxs-lookup"><span data-stu-id="3f978-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="3f978-414">Parameter „-ExcludeChangeType“ zu „Get-AzDeploymentWhatIfResult“ und „Get-AzResourceGroupDeploymentWhatIfResult“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="3f978-415">Parameter „-WhatIfExcludeChangeType“ zu „New-AzDeployment“ und „New-AzResourceGroupDeployment“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="3f978-416">Cmdlets von „Test-Az\*Deployment“, sodass bessere Fehlermeldungen angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="3f978-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="3f978-417">Hilfemeldung für Parameter „-Name“ der Cmdlets „deployment create“ und „What-If“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-418">Az.Sql</span></span>
* <span data-ttu-id="3f978-419">Unterstützung für Dienstprinzipal für Cmdlet „Set SQL Server Azure Active Directory Admin“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="3f978-420">Synchronisierungsproblem in Datenklassifizierungs-Cmdlets wurde behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="3f978-421">Suchen von Benutzern nach E-Mail wird für „Set-AzSqlServerActiveDirectoryAdministrator“ unterstützt [#12192]</span><span class="sxs-lookup"><span data-stu-id="3f978-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-422">Az.Storage</span></span>
* <span data-ttu-id="3f978-423">Erstellen eines Speicherkontos mit „RequireInfrastructureEncryption“ wird unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="3f978-424">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-425">Logik zum Laden von „Azure.Core to Az.Accounts“ verschoben</span><span class="sxs-lookup"><span data-stu-id="3f978-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-426">Az.Websites</span></span>
* <span data-ttu-id="3f978-427">Schutz zum Löschen der erstellten Web-App hinzugefügt, wenn die Wiederherstellung in „Restore-AzDeletedWebApp“ fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="3f978-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3f978-428">„SourceWebApp.Location“ für „New-AzWebApp“ und „New-AzWebAppSlot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="3f978-429">Fehler behoben, der das Ändern von Containereinstellungen in „Set-AzWebApp“ und „Set-AzWebAppSlot“ verhindert hat.</span><span class="sxs-lookup"><span data-stu-id="3f978-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="3f978-430">Fehler beim Abrufen von „SiteConfig“ behoben, wenn „-Name“ für „Get-AzWebApp“ nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3f978-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="3f978-431">Unterstützung zum Erstellen von ASP für Linux-Apps hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="3f978-432">Ausnahmen für den Ressourcengruppen übergreifenden Klonvorgang hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="3f978-433">4.2.0: Juni 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-434">Az.Accounts</span></span>
* <span data-ttu-id="3f978-435">Problem behoben, das unter Umständen dazu geführt hat, dass Az Protokolle in Azure Automation- oder PowerShell-Aufträgen übersprungen hat [Nr. 11492]</span><span class="sxs-lookup"><span data-stu-id="3f978-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="3f978-437">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-438">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-439">Assemblyversion der Dienstverwaltungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="3f978-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3f978-440">Az.Billing</span></span>
* <span data-ttu-id="3f978-441">Assemblyversion der Nutzungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-443">Unterstützung des PrivateEndpoint- und des PublicNetworkAccess-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="3f978-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-444">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-445">Assemblyversion der Data Factory v2-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="3f978-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="3f978-446">Az.DataShare</span></span>
* <span data-ttu-id="3f978-447">Allgemeine Verfügbarkeit des Moduls „Az.DataShare“</span><span class="sxs-lookup"><span data-stu-id="3f978-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="3f978-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="3f978-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="3f978-449">Allgemeine Verfügbarkeit des Moduls „Az.DesktopVirtualization“</span><span class="sxs-lookup"><span data-stu-id="3f978-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-451">SDK auf 0.21.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="3f978-452">Optionale Parameter hinzugefügt zu:</span><span class="sxs-lookup"><span data-stu-id="3f978-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="3f978-453">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3f978-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="3f978-454">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3f978-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-456">Beispiel 3 für „Start-AzPolicyComplianceScan“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3f978-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3f978-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3f978-458">Assemblyversion der PowerBI-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="3f978-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="3f978-459">Az.PrivateDns</span></span>
* <span data-ttu-id="3f978-460">Formatierung der ausführlichen Ausgabezeichenfolge für „Remove-AzPrivateDnsRecordSet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-462">Azure Site Recovery-Unterstützung für die Erstellung eines Wiederherstellungsplans für die Replikation zwischen Zonen per XML-Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f978-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="3f978-463">Assemblyversion der SiteRecovery- und Backup-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-464">Az.Resources</span></span>
* <span data-ttu-id="3f978-465">Tail-Parameter zu den Cmdlets „Get-AzDeploymentScriptLog“ und „Save-AzDeploymentScriptLog“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="3f978-466">Die Output-Eigenschaft wurde formatiert und wird nun in der Ausgabe des Cmdlets „Get-AzDeploymentScript“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f978-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="3f978-467">Parameter „-DeploymentScriptInputObject“ in „-DeploymentScriptObject“ umbenannt</span><span class="sxs-lookup"><span data-stu-id="3f978-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="3f978-468">Fehlender Datei-/Zielname in Cmdlet-Meldungen korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="3f978-469">Assemblyversion der Resource Manager- und Tags-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-470">Az.Sql</span></span>
* <span data-ttu-id="3f978-471">„UsePrivateLinkConnection“ zu „New-AzSqlSyncGroup“, „Update-AzSqlSyncGroup“, „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="3f978-472">„SyncMemberAzureDatabaseResourceId“ zu „New-AzSqlSyncMember“ und „Update-AzSqlSyncMember“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="3f978-473">Unterstützung für die Gastbenutzersuche zum SQL Server-Cmdlet für den Azure Active Directory-Administrator hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-474">Az.Storage</span></span>
* <span data-ttu-id="3f978-475">Assemblyversion der Cmdlets der Datenebene aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="3f978-476">4.1.0 – Mai 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="3f978-477">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="3f978-477">Highlights since the last release</span></span>
* <span data-ttu-id="3f978-478">Unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="3f978-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="3f978-479">Allgemeine Verfügbarkeit von Az.Functions</span><span class="sxs-lookup"><span data-stu-id="3f978-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="3f978-480">Veröffentlichung von Hauptversionen von Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources und Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-481">Az.Accounts</span></span>
* <span data-ttu-id="3f978-482">„Add-AzEnvironment“ und „Set-AzEnvironment“ akzeptieren jetzt die Parameter „AzureSynapseAnalyticsEndpointResourceId“ und „AzureSynapseAnalyticsEndpointSuffix“.</span><span class="sxs-lookup"><span data-stu-id="3f978-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="3f978-483">Assemblys zu Azure.Core wurden Az.Accounts hinzugefügt. Unterstützte PowerShell-Plattformen sind u. a. Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="3f978-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-484">Az.Aks</span></span>
* <span data-ttu-id="3f978-485">API-Version wurde auf 2019-10-01 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="3f978-486">Unterstützung für die Erstellung von AKS mit einem Windows-Container</span><span class="sxs-lookup"><span data-stu-id="3f978-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="3f978-487">Neu verfügbare Cmdlets: „New-AzAksNodePool“, „Update-AzAksNodePool“, „Remove-AzAksNodePool“, „Get-AzAksNodePool“, „Install-AzAksKubectl“, „Get-AzAksVersion“</span><span class="sxs-lookup"><span data-stu-id="3f978-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-488">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-489">„New-AzApiManagement“ und „Set-AzApiManagement“: Parameter [-AssignIdentity] wurde in [-SystemAssignedIdentity] umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="3f978-490">„New-AzApiManagement“ und „Set-AzApiManagement“: Neuer Parameter hinzugefügt: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="3f978-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="3f978-491">„Get-AzApiManagementProperty“ wurde in „Get-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3f978-492">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3f978-493">„New-AzApiManagementProperty“ wurde in „New-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3f978-494">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="3f978-495">„Set-AzApiManagementProperty“ wurde in „Set-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3f978-496">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3f978-497">„Remove-AzApiManagementProperty“ wurde in „Remove-AzApiManagementNamedValue“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="3f978-498">Der Parameter PropertyId wurde in NamedValueId umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="3f978-499">Neues Cmdlet „Get-AzApiManagementAuthorizationServerClientSecret“ hinzugefügt. „Get-AzApiManagementAuthorizationServer“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="3f978-500">Neues Cmdlet „Get-AzApiManagementNamedValueSecretValue“ hinzugefügt. „Get-AzApiManagementNamedValue“ gibt keinen Geheimniswert zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="3f978-501">Neues Cmdlet „Get-AzApiManagementOpenIdConnectProviderClientSecret“ hinzugefügt. „Get-AzApiManagementOpenIdConnectProvider“ gibt keinen geheimen Clientschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="3f978-502">Neues Cmdlet „Get-AzApiManagementSubscriptionKey“ hinzugefügt. „Get-AzApiManagementSubscription“ gibt keine Abonnementschlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="3f978-503">Neues Cmdlet „Get-AzApiManagementTenantAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="3f978-504">Neues Cmdlet „Get-AzApiManagementTenantGitAccessSecret“ hinzugefügt. „Get-AzApiManagementTenantGitAccess“ gibt keine Schlüssel mehr zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3f978-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3f978-506">Parameter hinzugefügt: „RetentionInDays“, „PublicNetworkAccessForIngestion“, „PublicNetworkAccessForQuery“ für „New-AzApplicationInsights“</span><span class="sxs-lookup"><span data-stu-id="3f978-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="3f978-507">Cmdlet „Update-AzApplicationInsights“ erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f978-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="3f978-508">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f978-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-509">Az.Batch</span></span>
* <span data-ttu-id="3f978-510">Az.Batch für die Verwendung der Microsoft.Azure.Batch-SDK-Version 13.0.0 und der Microsoft.Azure.Management.Batch-SDK-Version 9.0.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="3f978-511">Die Möglichkeit zum Auswählen der Art des hinzugefügten Zertifikats mithilfe des neuen Parameters „-CertificateKind“ wurde zu „New-AzBatchCertificate“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="3f978-512">Eigenschaft „ApplicationPackages“ aus „PSApplication“ entfernt, die bislang immer „“ war.</span><span class="sxs-lookup"><span data-stu-id="3f978-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="3f978-513">Die spezifischen Pakete in einer Anwendung können jetzt mit „Get-AzBatchApplicationPackage“ abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="3f978-514">Beispiel: „Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication“</span><span class="sxs-lookup"><span data-stu-id="3f978-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="3f978-515">Beim Erstellen eines Pools mit „New-AzBatchPool“ kann die Eigenschaft „VirtualMachineImageId“ von „PSImageReference“ jetzt nur auf ein Bild in einer Shared Image Gallery verweisen.</span><span class="sxs-lookup"><span data-stu-id="3f978-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="3f978-516">Wenn Sie einen Pool mit „New-AzBatchPool“ erstellen, kann der Pool mit der Eigenschaft „PublicIPAddressConfiguration“ von „PSNetworkConfiguration“ ohne eine öffentliche IP-Adresse bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="3f978-517">Die Eigenschaft „PublicIPs“ von „PSNetworkConfiguration“ wurde ebenfalls in „PSPublicIPAddressConfiguration“ verschoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="3f978-518">Diese Eigenschaft kann nur angegeben werden, wenn „IPAddressProvisioningType“ den Wert „UserManaged“ hat.</span><span class="sxs-lookup"><span data-stu-id="3f978-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-519">Az.Compute</span></span>
* <span data-ttu-id="3f978-520">HostId-Parameter zum Cmdlet „Update-AzVM“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="3f978-521">Hilfedokumente für die Cmdlets „New-AzVMConfig“, „New-AzVmssConfig“, „Update-AzVmss“, „Set-AzVMOperatingSystem“ und „Set-AzVmssOsProfile“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="3f978-522">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="3f978-522">Breaking changes</span></span>
    - <span data-ttu-id="3f978-523">Der FilterExpression-Parameter wurde aus dem Cmdlet „Get-AzVMImage“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="3f978-524">Der AssignIdentity-Parameter wurde aus den Cmdlets „New-AzVmssConfig“, „New-AzVMConfig“ und „Update-AzVM“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="3f978-525">AutomaticRepairMaxInstanceRepairsPercent wurde aus den Cmdlets „New-AzVmssConfig“ und „Update-AzVmss“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="3f978-526">Die Eigenschaften AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus und VirtualMachineScaleSetsColocationStatus wurden aus ProximityPlacementGroup entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="3f978-527">Die Eigenschaft MaxInstanceRepairsPercent wurde aus AutomaticRepairsPolicy entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="3f978-528">Die Typen von AvailabilitySets, VirtualMachines und VirtualMachineScaleSets wurden von IList<SubResource> in IList<SubResourceWithColocationStatus> geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="3f978-529">Die Beschreibung für das Cmdlet „Get-AzVM“ wurde verbessert.</span><span class="sxs-lookup"><span data-stu-id="3f978-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-530">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-531">CRUD von Datenfluss-Laufzeiteigenschaften in Managed IR unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-532">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-533">Neue Cmdlets zum Erstellen, Aktualisieren, Abrufen und Löschen von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="3f978-534">Hilfs-Cmdlets für die Erstellung von Front Door-Regelmodulobjekten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="3f978-535">Regelmodulverweis auf Front Door-Routingregelobjekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="3f978-536">Private Link-Parameter zum Front Door-Back-End-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="3f978-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="3f978-537">Az.Functions</span></span>
* <span data-ttu-id="3f978-538">Allgemeine Verfügbarkeit des Moduls „Az.Functions“</span><span class="sxs-lookup"><span data-stu-id="3f978-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-539">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-540">Datenträgerverschlüsselung mit kundenseitig verwalteten Schlüsseln unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3f978-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3f978-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="3f978-542">Zugriffsrichtlinien verwenden nicht mehr den aktuellen Prinzipal als Standard.</span><span class="sxs-lookup"><span data-stu-id="3f978-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-543">Az.IotHub</span></span>
* <span data-ttu-id="3f978-544">Cmdlet zum Aufrufen einer Abfrage in einem IoT-Hub zum Abrufen von Informationen mithilfe einer SQL-ähnlichen Sprache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="3f978-545">Problem behoben, dass „Add-AzIotHubDevice“ kein Edge-aktiviertes Gerät ohne untergeordnete Geräte erstellen konnte. [#11597]</span><span class="sxs-lookup"><span data-stu-id="3f978-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="3f978-546">Cmdlet zum Generieren eines SAS-Tokens für IoT-Hub, -Gerät oder -Modul hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="3f978-547">Cmdlet zum Aufrufen der Konfigurationsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="3f978-548">Verwalten der automatischen skalierbaren Bereitstellung von IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="3f978-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="3f978-549">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-549">New cmdlets are:</span></span>
    - <span data-ttu-id="3f978-550">„Add-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3f978-551">„Get-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3f978-552">„Remove-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="3f978-553">„Set-AzIotHubDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="3f978-554">Cmdlet zum Hinzufügen einer IoT Edge-Bereitstellungsmetrikenabfrage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="3f978-555">Cmdlet zum Anwenden des Konfigurationsinhalts auf das angegebene Edge-Gerät hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-556">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-557">Zwei Aliase entfernt: „New-AzKeyVaultCertificateAdministratorDetails“ und „New-AzKeyVaultCertificateOrganizationDetails“</span><span class="sxs-lookup"><span data-stu-id="3f978-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="3f978-558">Vorläufiges Löschen ist beim Erstellen eines Schlüsseltresors standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3f978-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="3f978-559">Netzwerkregeln können so festgelegt werden, dass der Zugriff von bestimmten Netzwerkstandorten beim Erstellen eines Schlüsseltresors gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="3f978-560">Unterstützung für BYOK (Bring Your Own Key) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="3f978-561">„Add-AzKeyVaultKey“ unterstützt die Erstellung eines Schlüsselaustauschschlüssels.</span><span class="sxs-lookup"><span data-stu-id="3f978-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="3f978-562">„Get-AzKeyVaultKey“ unterstützt das Herunterladen eines öffentlichen Schlüssels im PEM-Format.</span><span class="sxs-lookup"><span data-stu-id="3f978-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="3f978-563">Abschnitt „KeyOps“ der Hilfedokumentation zu „Add-AzKeyVaultKey“ wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-564">Az.Monitor</span></span>
* <span data-ttu-id="3f978-565">Fehler bei „Set-AzDiagnosticSettings“ behoben. Aufbewahrungsrichtlinie gilt nicht für alle Kategorien. [#11589]</span><span class="sxs-lookup"><span data-stu-id="3f978-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="3f978-566">WebTest-Verfügbarkeitskriterien für die Metrikwarnung V2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="3f978-567">„New-AzMetricAlertRuleV2Criteria“: Option zum Erstellen der Webtest-Verfügbarkeitskriterien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="3f978-568">„Add-AzMetricAlertRuleV2“: Neue Webtest-Verfügbarkeitskriterien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="3f978-569">Redundante Definition für „RetentionPolicy“ in PSLogProfile entfernt. [#7608]</span><span class="sxs-lookup"><span data-stu-id="3f978-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="3f978-570">Redundante in PSEventData definierte Eigenschaften entfernt. [#11353]</span><span class="sxs-lookup"><span data-stu-id="3f978-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="3f978-571">„Get-AzLog“ in „Get-AzActivityLog“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-572">Az.Network</span></span>
* <span data-ttu-id="3f978-573">Breaking Change-Attribut hinzugefügt als Benachrichtigung, dass sich das Standardverhalten der Zone ändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="3f978-574">„New-AzPublicIpAddress“</span><span class="sxs-lookup"><span data-stu-id="3f978-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="3f978-575">„New-AzPublicIpPrefix“</span><span class="sxs-lookup"><span data-stu-id="3f978-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="3f978-576">„New-AzLoadBalancerFrontendIpConfig“</span><span class="sxs-lookup"><span data-stu-id="3f978-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="3f978-577">Unterstützung für die neue Ressource der obersten Ebene SecurityPartnerProvider hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="3f978-578">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-578">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3f978-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3f978-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3f978-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3f978-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3f978-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="3f978-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="3f978-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="3f978-583">„RequiredZoneNames“ für „PSPrivateLinkResource“ und „GroupId“ für „PSPrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="3f978-584">Falscher Typ des Parameters SuccessThresholdRoundTripTimeMs für New-AzNetworkWatcherConnectionMonitorTestConfigurationObject korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="3f978-585">VirtualWan-Cmdlets aktualisiert, sodass der Standardwert des Arguments AllowVnetToVnetTraffic auf True festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="3f978-586">„New-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="3f978-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="3f978-587">„Update-AzVirtualWan“</span><span class="sxs-lookup"><span data-stu-id="3f978-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="3f978-588">Neue Cmdlets zur Unterstützung der DNS-Zonengruppe für den privaten Endpunkt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="3f978-589">„New-AzPrivateDnsZoneConfig“</span><span class="sxs-lookup"><span data-stu-id="3f978-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="3f978-590">„Get-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="3f978-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3f978-591">„New-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="3f978-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3f978-592">„Set-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="3f978-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="3f978-593">„Remove-AzPrivateDnsZoneGroup“</span><span class="sxs-lookup"><span data-stu-id="3f978-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="3f978-594">Parameter „DNSEnableProxy“, „DNSRequireProxyForNetworkRules“ und „DNSServers“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="3f978-595">Parameter „EnableDnsProxy“, „DnsProxyNotRequiredForNetworkRule“ und „DnsServer“ zu „AzureFirewall“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="3f978-596">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="3f978-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3f978-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-599">Legacycode zum Anwenden des neuen generierten SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="3f978-600">Cmdlets aufgrund von veralteten APIs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3f978-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="3f978-601">„Get-AzOperationalInsightsSavedSearchResult“ (alias „Get-AzOperationalInsightsSavedSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="3f978-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="3f978-602">„Get-AzOperationalInsightsSearchResult“ (alias „Get-AzOperationalInsightsSearchResults“)</span><span class="sxs-lookup"><span data-stu-id="3f978-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="3f978-603">„Get-AzOperationalInsightsLinkTarget“ (alias „Get-AzOperationalInsightsLinkTargets“)</span><span class="sxs-lookup"><span data-stu-id="3f978-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="3f978-604">Parameter für „Set-AzOperationalInsightsWorkspace“ und „New-AzOperationalInsightsWorkspace“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="3f978-605">Cmdlets für verknüpftes Speicherkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f978-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="3f978-606">Cmdlets für Cluster und verknüpften Dienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f978-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-608">Azure Site Recovery: Unterstützung für den Schutz von virtuellen Computern der Näherungsplatzierungsgruppe für den Azure-zu-Azure-Anbieter hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="3f978-609">Azure Site Recovery: Unterstützung für die Replikation zwischen Zonen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="3f978-610">Azure Backup: Unterstützung für die langfristige Aufbewahrung von Azure FileShare-Wiederherstellungspunkten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="3f978-611">Azure Backup: Eigenschaften für den Ausschluss von Datenträgern zur Ausgabe des Cmdlet „Get-AzRecoveryServicesBackupItem“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="3f978-612">Privater Endpunkt für Tresoranmeldeinformationen für den Site Recovery-Dienst hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-613">Az.Resources</span></span>
* <span data-ttu-id="3f978-614">Warnmeldung zur verzögerten Ansicht beim Erstellen einer neuen Rollendefinition hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="3f978-615">Richtlinien-Cmdlets geändert, sodass sie stark typisierte Objekte ausgeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="3f978-616">Parameter „-TenantLevel“ zum Cmdlet „Get-AzResourceLock“ hinzugefügt. [#11335]</span><span class="sxs-lookup"><span data-stu-id="3f978-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="3f978-617">„Remove-AzResourceGroup -Id ResourceId“ korrigiert. [#9882]</span><span class="sxs-lookup"><span data-stu-id="3f978-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="3f978-618">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Ressourcengruppenbereich hinzugefügt: „Get-AzDeploymentResourceGroupWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="3f978-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="3f978-619">Neues Cmdlet zum Abrufen von Was-wäre-wenn-Ergebnissen der ARM-Vorlage im Abonnementbereich hinzugefügt: „Get-AzDeploymentWhatIfResult“</span><span class="sxs-lookup"><span data-stu-id="3f978-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="3f978-620">Alias: „Get-AzSubscriptionDeploymentWhatIf“</span><span class="sxs-lookup"><span data-stu-id="3f978-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="3f978-621">Parameter „-WhatIf“ und „-Confirm“ für „New-AzDeployment“ und „New-AzResourceGroupDeployment“ für die Verwendung von Was-wäre-wenn-Ergebnissen der ARM-Vorlage überschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f978-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="3f978-622">Meldung zur Einstellung der Unterstützung für „ApiVersion“ in Bereitstellungs-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="3f978-623">Funktion zum Anzeigen verbesserter Fehlermeldungen für Bereitstellungsfehler hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="3f978-624">Protokollierung von correlationId bei Bereitstellungsfehlern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="3f978-625">Eigenschaft „error“ zur Bereitstellungsskriptausgabe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="3f978-626">NuGet-Microsoft.Azure.Management.ResourceManager auf „3.7.1-preview“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="3f978-627">Bestimmte Testfälle entfernt, da die Error-Eigenschaft in DeploymentValidateResult von NuGet 3.7.1-preview in schreibgeschützt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="3f978-628">GenericResourceExpanded aus dem SDK ResourceManager 3.7.1-preview importiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="3f978-629">Tagunterstützung für alle Get-Cmdlets für die Bereitstellung hinzugefügt sowie</span><span class="sxs-lookup"><span data-stu-id="3f978-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="3f978-630">„New-AzDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="3f978-631">„New-AzManagementGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="3f978-632">„New-AzResourceGroupDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3f978-633">„New-AzTenantDeployment“</span><span class="sxs-lookup"><span data-stu-id="3f978-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-635">Fehler beim Hinzufügen eines Zertifikats mithilfe von „--SecretIdentifier“ behoben, der den falschen Zertifikatfingerabdruck erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="3f978-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-636">Az.Sql</span></span>
* <span data-ttu-id="3f978-637">Leistungsoptimierung von:</span><span class="sxs-lookup"><span data-stu-id="3f978-637">Enhance performance of:</span></span>
    - <span data-ttu-id="3f978-638">„Set-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="3f978-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3f978-639">„Set-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="3f978-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3f978-640">„Remove-AzSqlDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="3f978-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3f978-641">„Remove-AzSqlInstanceDatabaseSensitivityClassification“</span><span class="sxs-lookup"><span data-stu-id="3f978-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="3f978-642">„Enable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="3f978-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3f978-643">„Enable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="3f978-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3f978-644">„Disable-AzSqlDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="3f978-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="3f978-645">„Disable-AzSqlInstanceDatabaseSensitivityRecommendation“</span><span class="sxs-lookup"><span data-stu-id="3f978-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="3f978-646">Clientseitige Validierung des Parameters „RetentionDays“ aus dem Cmdlet „Set-AzSqlDatabaseBackupShortTermRetentionPolicy“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="3f978-647">Fehler beim Überwachen eines Speicherkontos in Vnet und Erstellen einer Rolle für den Mitwirkenden an Speicherblobdaten behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-648">Az.Storage</span></span>
* <span data-ttu-id="3f978-649">„-AsJob“ hinzugefügt, um das Konto für das Cmdlet „Get-AzStorageAccount“ abzurufen/aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="3f978-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-650">KeyVersion als optional festgelegt, wenn das Speicherkonto mit KeyvaultEncryption aktualisiert wird, um die automatische Schlüsselrotation zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="3f978-651">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-652">Fehler beim Entfernen des Azure-Dateiverzeichnisses mit der Pipeline behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="3f978-653">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="3f978-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="3f978-654">Behoben [#9880]: Definition des DefaultAction-Werts für NetWorkRule in Übereinstimmung mit Swagger geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="3f978-655">„Update-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="3f978-656">„Get-AzStorageAccountNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="3f978-657">Behoben [#11624]: Doppelte Regeln werden beim Hinzufügen von NetworkRules übersprungen, um Serverfehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3f978-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="3f978-658">„Add-AzStorageAccountNetworkRule“</span><span class="sxs-lookup"><span data-stu-id="3f978-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="3f978-659">Microsoft.Azure.Cosmos.Table SDK auf 1.0.7 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="3f978-660">Warnmeldung hinzugefügt, mit der der Benutzer darauf hingewiesen wird, eine erneute Auflistung mit ContinuationToken auszuführen, wenn nur ein Teil der Elemente in der Liste der DataLake Gen2-Elemente zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="3f978-661">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="3f978-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="3f978-662">Unterstützung für das Erstellen oder Aktualisieren eines Speicherkontos mit Active Directory Domain Service-Authentifizierung für Azure Files.</span><span class="sxs-lookup"><span data-stu-id="3f978-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="3f978-663">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="3f978-664">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-665">Unterstützung für das Hinzufügen und Auflisten von Kerberos-Schlüsseln des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="3f978-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="3f978-666">„New-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="3f978-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="3f978-667">„Get-AzStorageAccountKey“</span><span class="sxs-lookup"><span data-stu-id="3f978-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3f978-668">Unterstützung für Failover für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="3f978-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="3f978-669">„Invoke-AzStorageAccountFailover“</span><span class="sxs-lookup"><span data-stu-id="3f978-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="3f978-670">Hilfe zu „Get-AzStorageBlobCopyState“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="3f978-671">Hilfe zu „Get-AzStorageFileCopyState“ und „Start-AzStorageBlobCopy“ aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="3f978-672">Speicherclientbibliothek v12 in Cmdlets Queue und File integriert.</span><span class="sxs-lookup"><span data-stu-id="3f978-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="3f978-673">Ausgabetyp von CloudFile in AzureStorageFile geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3f978-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3f978-674">„Get-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="3f978-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="3f978-675">„Remove-AzStorageFile“</span><span class="sxs-lookup"><span data-stu-id="3f978-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="3f978-676">„Get-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="3f978-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="3f978-677">„Set-AzStorageFileContent“</span><span class="sxs-lookup"><span data-stu-id="3f978-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="3f978-678">„Start-AzStorageFileCopy“</span><span class="sxs-lookup"><span data-stu-id="3f978-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="3f978-679">Ausgabetyp von CloudFileDirectory in AzureStorageFileDirectory geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3f978-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3f978-680">„New-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="3f978-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="3f978-681">„Remove-AzStorageDirectory“</span><span class="sxs-lookup"><span data-stu-id="3f978-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="3f978-682">Ausgabetyp von CloudFileShare in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3f978-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="3f978-683">„Get-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="3f978-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="3f978-684">„New-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="3f978-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="3f978-685">„Remove-AzStorageShare“</span><span class="sxs-lookup"><span data-stu-id="3f978-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="3f978-686">Ausgabetyp von FileShareProperties in AzureStorageFileShare geändert. Die ursprüngliche Ausgabe wird zu einer untergeordneten Eigenschaft der neuen Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3f978-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="3f978-687">„Set-AzStorageShareQuota“</span><span class="sxs-lookup"><span data-stu-id="3f978-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3f978-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3f978-688">Az.TrafficManager</span></span>
* <span data-ttu-id="3f978-689">Falscher Profilname in der ausführlichen Ausgabe von „DisableAzureTrafficManagerEndpoint“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-690">Az.Websites</span></span>
* <span data-ttu-id="3f978-691">Tippfehler in der Hilfe zu „Update-AzWebAppAccessRestrictionConfig“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="3f978-692">3.8.0: April 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="3f978-693">Highlights seit dem letzten Release</span><span class="sxs-lookup"><span data-stu-id="3f978-693">Highlights since the last release</span></span>
* <span data-ttu-id="3f978-694">Von Az.Storage unterstützte PowerShell-Versionen: Windows PowerShell 5.1, PowerShell Core 6.2.4 oder höher, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="3f978-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-695">Az.Accounts</span></span>
* <span data-ttu-id="3f978-696">Azure PowerShell-Umfrage-URL in „Resolve-AzError“ aktualisiert [#11507]</span><span class="sxs-lookup"><span data-stu-id="3f978-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-697">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-698">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="3f978-699">„Set-AzApiManagementGroup“: Dokumentation zur Angabe des Parameters „GroupId“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-700">Az.Cdn</span></span>
* <span data-ttu-id="3f978-701">Anzeige der Preis-SKU für ChinaCDN korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-703">Unterstützung für „Identity“, „Encryption“ und „UserOwnedStorage“</span><span class="sxs-lookup"><span data-stu-id="3f978-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-704">Az.Compute</span></span>
* <span data-ttu-id="3f978-705">Cmdlet „Set-AzVmssOrchestrationServiceState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="3f978-706">„Get-AzVmss“ mit „-InstanceView“ zeigt die OrchestrationService-Zustände.</span><span class="sxs-lookup"><span data-stu-id="3f978-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-707">Az.IotHub</span></span>
* <span data-ttu-id="3f978-708">Verwalten der Konfiguration von IoT-Gerätezwillingen. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="3f978-709">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3f978-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="3f978-710">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3f978-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="3f978-711">Cmdlet zum Aufrufen der direkten Methode auf einem Gerät in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="3f978-712">Verwalten der Konfiguration von Modulzwillingen der IoT-Geräte. Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="3f978-713">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3f978-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="3f978-714">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3f978-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="3f978-715">Verwalten Sie die Konfiguration für die automatische Verwaltung von IoT-Geräten im großen Stil.</span><span class="sxs-lookup"><span data-stu-id="3f978-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="3f978-716">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-716">New cmdlets are:</span></span>
    - <span data-ttu-id="3f978-717">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3f978-718">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3f978-719">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="3f978-720">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="3f978-721">Cmdlet zum Aufrufen einer Edge-Modulmethode in einer IoT Hub-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-722">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-723">Neues Cmdlet „Update-AzKeyVault“ hinzugefügt, mit dem für einen Tresor der Schutz vor vorläufigem Löschen und vor Bereinigung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3f978-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="3f978-724">Unterstützung zu Microsoft.PowerShell.SecretManagement hinzugefügt [Nr. 11178]</span><span class="sxs-lookup"><span data-stu-id="3f978-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="3f978-725">Fehler in den Beispielen von „Remove-AzKeyVaultManagedStorageSasDefinition“ behoben [Nr. 11479]</span><span class="sxs-lookup"><span data-stu-id="3f978-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="3f978-726">Unterstützung zu privatem Endpunkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="3f978-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="3f978-727">Az.Maintenance</span></span>
* <span data-ttu-id="3f978-728">Veröffentlichen einer allgemein verfügbaren Releaseversion der Wartungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-729">Az.Monitor</span></span>
* <span data-ttu-id="3f978-730">Cmdlets für Private Link-Bereich hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="3f978-731">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3f978-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3f978-732">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3f978-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3f978-733">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3f978-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3f978-734">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="3f978-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="3f978-735">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3f978-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="3f978-736">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3f978-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="3f978-737">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="3f978-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-738">Az.Network</span></span>
* <span data-ttu-id="3f978-739">Cmdlets aktualisiert, um die Verbindung für die private IP-Adresse für das Virtual Network-Gateway zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="3f978-740">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="3f978-741">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="3f978-742">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="3f978-743">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="3f978-744">Cmdlets zum Aktivieren von FQDN-basierten LocalNetworkGateways- und VpnSites-Elementen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="3f978-745">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="3f978-746">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3f978-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="3f978-747">Unterstützung für die IPv6-Adressfamilie in ExpressRouteCircuitConnectionConfig (Global Reach) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="3f978-748">„Set-AzExpressRouteCircuitConnectionConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="3f978-749">Ermöglicht das Festlegen aller vorhandener Eigenschaften, einschließlich IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="3f978-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="3f978-750">„Add-AzExpressRouteCircuitConnectionConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="3f978-751">Weiterer optionaler Parameter (AddressPrefixType) zur Angabe der Adressfamilie des Adresspräfixes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="3f978-752">Cmdlets aktualisiert, um das Festlegen des DPD-Timeouts für Virtual Network-Gatewayverbindungen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="3f978-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="3f978-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-756">Cmdlet „Start-AzPolicyComplianceScan“ für das Auslösen von Richtlinienkonformitätsprüfungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="3f978-757">Richtliniendefinition, Richtliniensatzdefinition und Zuweisungsversionen zur Ausgabe „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-759">Codeformatierung und Verwendbarkeit von Beispielen für „New-AzServiceFabricCluster“ verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-760">Az.Sql</span></span>
* <span data-ttu-id="3f978-761">Cmdlets „Get-AzSqlInstanceOperation“ und „Stop-AzSqlInstanceOperation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="3f978-762">Unterstützte Überwachung eines Speicherkontos im VNET</span><span class="sxs-lookup"><span data-stu-id="3f978-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-763">Az.Storage</span></span>
* <span data-ttu-id="3f978-764">Breaking Change-Hinweis im Zusammenhang mit der Änderung der Ausgabe von Azure File-Cmdlets in einem zukünftigen Release hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="3f978-765">Unterstützter neuer SKU-Name (StandardGZRS und StandardRAGZRS) beim Erstellen/Aktualisieren eines Storage-Kontos</span><span class="sxs-lookup"><span data-stu-id="3f978-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="3f978-766">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="3f978-767">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="3f978-768">Unterstützung für DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="3f978-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="3f978-769">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3f978-770">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3f978-771">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="3f978-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="3f978-772">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3f978-773">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="3f978-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="3f978-774">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="3f978-775">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="3f978-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="3f978-776">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3f978-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="3f978-777">0.10.0-preview: April 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="3f978-778">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-778">General</span></span>
* <span data-ttu-id="3f978-779">Az-Module sind nun als Vorschauversionen in Azure Stack Hub verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f978-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="3f978-780">Dies ermöglicht eine plattformübergreifende Kompatibilität mit Linux und macOs.</span><span class="sxs-lookup"><span data-stu-id="3f978-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="3f978-781">Azure Stack Hub unterstützt jetzt PowerShell Core mit den Az-Modulen. Weitere Informationen finden Sie [hier](https://aka.ms/az4AzureStack).</span><span class="sxs-lookup"><span data-stu-id="3f978-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="3f978-782">Az-Module unterstützen das Supportprofil 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="3f978-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="3f978-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3f978-783">Az.Billing</span></span>
  - <span data-ttu-id="3f978-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-784">Az.Compute</span></span>
  - <span data-ttu-id="3f978-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3f978-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="3f978-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-786">Az.EventHub</span></span>
  - <span data-ttu-id="3f978-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-787">Az.IotHub</span></span>
  - <span data-ttu-id="3f978-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-788">Az.KeyVault</span></span>
  - <span data-ttu-id="3f978-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-789">Az.Monitor</span></span>
  - <span data-ttu-id="3f978-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-790">Az.Network</span></span>
  - <span data-ttu-id="3f978-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-791">Az.Resources</span></span>
  - <span data-ttu-id="3f978-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-792">Az.Storage</span></span>
  - <span data-ttu-id="3f978-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-793">Az.Websites</span></span>
* <span data-ttu-id="3f978-794">Für Az wurden neue PowerShell-Module (Az.Databox, Az.IotHub und Az.EventHub) eingeführt, die mit Azure Stack Hub verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3f978-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="3f978-795">Die Befehle bleiben ungefähr gleich und enthalten nur minimale Änderungen. Beispielsweise wird „AzureRM“ in „Az“ geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="3f978-796">Den aktualisierten Link zur PowerShell-Dokumentation für Azure Stack Hub finden Sie [hier](https://aka.ms/InstallASHPowerShell).</span><span class="sxs-lookup"><span data-stu-id="3f978-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="3f978-797">3.7.0: März 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-798">Az.Accounts</span></span>
* <span data-ttu-id="3f978-799">„Get-AzTenant“/„Get-AzDefault“/„Set-AzDefault“: Bei fehlender Anmeldung ausgelöste Ausnahme „NullReferenceException“ korrigiert [Nr. 10292]</span><span class="sxs-lookup"><span data-stu-id="3f978-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-800">Az.Compute</span></span>
* <span data-ttu-id="3f978-801">Folgende Parameter zum Cmdlet „New-AzDiskConfig“ hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="3f978-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="3f978-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="3f978-803">Verschlüsselungseigenschaft für Zielparameter des Cmdlets „New-AzGalleryImageVersion“ zugelassen</span><span class="sxs-lookup"><span data-stu-id="3f978-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="3f978-804">Problem „tempDisk“ für Cmdlets „Set-AzVmss' -Reimage“ und „Invoke-AzVMReimage“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="3f978-805">[Nr. 11354]</span><span class="sxs-lookup"><span data-stu-id="3f978-805">[#11354]</span></span>
* <span data-ttu-id="3f978-806">Unterstützung für die folgenden Cmdlets für die neue SAP-Erweiterung hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="3f978-807">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3f978-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3f978-808">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3f978-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3f978-809">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3f978-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="3f978-810">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="3f978-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="3f978-811">Fehler in Beispielen im Hilfedokument korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="3f978-812">Der genaue Zeichenfolgenwert für den VM-Energiezustand (PowerState) wurde im Tabellenformat angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f978-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="3f978-813">New-AzVmssConfig: Serialisierung der Eigenschaft „AutomaticRepairs“ korrigiert, wenn „SinglePlacementGroup“d deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="3f978-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="3f978-814">[Nr. 11257]</span><span class="sxs-lookup"><span data-stu-id="3f978-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-815">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-816">Version des ADF .NET SDK auf 4.8.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="3f978-817">Optionale Parameter zum Befehl „Invoke-AzDataFactoryV2Pipeline“ zur Unterstützung der erneuten Ausführung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-819">Breaking Change-Beschreibung für „Export-AzDataLakeStoreItem“ und „Import-AzDataLakeStoreItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="3f978-820">Option zur Bytecodierung für „New-AzDataLakeStoreItem“, „Add-AzDAtaLakeStoreItemContent“ und „Get-AzDAtaLakeStoreItemContent“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-821">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-822">Angabe der mindestens unterstützten TLS-Version bei Clustererstellung unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f978-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-823">Az.IotHub</span></span>
* <span data-ttu-id="3f978-824">Unterstützung für die Verwaltung verteilter Einstellungen pro Gerät hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="3f978-825">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="3f978-826">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3f978-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="3f978-827">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3f978-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-828">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-829">Breaking Change-Attribute zu „New-AzKeyVault“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-830">Az.Monitor</span></span>
* <span data-ttu-id="3f978-831">Dokumentation für „New-AzScheduledQueryRuleLogMetricTrigger“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-832">Az.Network</span></span>
* <span data-ttu-id="3f978-833">Cmdlets aktualisiert, um mandantenübergreifende VNET-Verbindungen virtueller Hubs (VirtualHubVnetConnections) zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="3f978-834">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3f978-835">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="3f978-836">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3f978-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="3f978-837">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3f978-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="3f978-838">Abhängigkeit vom SQL Management SDK entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-840">Verbesserte Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="3f978-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-842">Azure Site Recovery: Unterstützung für erneutes Schützen hinzugefügt und VM-Eigenschaften für VMs mit Azure-Datenträgerverschlüsselung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="3f978-843">Überwachung der Notfallwiederherstellung für VmwareToAzure-Eigenschaften von Azure Site Recovery hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="3f978-844">Azure Backup: Unterstützung für die Wiederholung des Richtlinienupdates für fehlerhafte Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="3f978-845">Azure Backup: Unterstützung für Einstellungen für den Ausschluss von Datenträgern während der Sicherung und Wiederherstellung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="3f978-846">Azure Backup: Unterstützung für die Wiederherstellung mehrerer Dateien/Ordner in AzureFileShare hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="3f978-847">Azure Backup: Unterstützung für vom Benutzer angegebene Ressourcengruppe beim Aktualisieren der IaasVM-Richtlinie hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-848">Az.Resources</span></span>
* <span data-ttu-id="3f978-849">„Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType“ korrigiert, sodass die tatsächliche API-Version (apiVersion) von Ressourcen anstelle der API-Standardversion verwendet wird [Nr. 11267]</span><span class="sxs-lookup"><span data-stu-id="3f978-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="3f978-850">Protokollierung von „correlationId“ für Fehlerszenarien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="3f978-851">Kleine Änderung an der Dokumentation für „Get-AzResourceLock“</span><span class="sxs-lookup"><span data-stu-id="3f978-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="3f978-852">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-852">Added example.</span></span>
* <span data-ttu-id="3f978-853">Einfaches Anführungszeichen im Parameterwert „Get-AzADUser“ mit Escapezeichen versehen [Nr. 11317]</span><span class="sxs-lookup"><span data-stu-id="3f978-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="3f978-854">Neue Cmdlets für Bereitstellungsskripts (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-855">Az.Sql</span></span>
* <span data-ttu-id="3f978-856">Lesbarer sekundärer Parameter zu „Invoke-AzSqlDatabaseFailover“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="3f978-857">Cmdlet „Disable-AzSqlServerActiveDirectoryOnlyAuthentication“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="3f978-858">Vertraulichkeitsrang beim Klassifizieren von Spalten in der Datenbank gespeichert</span><span class="sxs-lookup"><span data-stu-id="3f978-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="3f978-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="3f978-859">Az.Support</span></span>
* <span data-ttu-id="3f978-860">Allgemeine Verfügbarkeit des Moduls „Az.Support“</span><span class="sxs-lookup"><span data-stu-id="3f978-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-861">Az.Websites</span></span>
* <span data-ttu-id="3f978-862">Unterstützung für das Arbeiten mit Datenverkehrs-Routingregeln für Web-Apps über die folgenden neuen Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="3f978-863">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f978-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3f978-864">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f978-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3f978-865">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f978-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="3f978-866">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f978-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="3f978-867">3.6.1 – März 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-868">Az.Accounts</span></span>
* <span data-ttu-id="3f978-869">Öffnen der Azure PowerShell-Umfrageseite in „Send-Feedback“ [#11020]</span><span class="sxs-lookup"><span data-stu-id="3f978-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="3f978-870">Anzeigen der Azure PowerShell-Umfrage-URL in „Resolve-Error“ [#11021]</span><span class="sxs-lookup"><span data-stu-id="3f978-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="3f978-871">Az-Version in UserAgent hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-872">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-873">Unterstützung für das Abrufen und Konfigurieren einer benutzerdefinierten Domäne auf dem DeveloperPortal-Endpunkt hinzugefügt [#11007]</span><span class="sxs-lookup"><span data-stu-id="3f978-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="3f978-874">„Export-AzApiManagementApi“: Unterstützung für das Herunterladen der API-Definition im JSON-Format hinzugefügt [#9987]</span><span class="sxs-lookup"><span data-stu-id="3f978-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="3f978-875">„Import-AzApiManagementApi“: Unterstützung für das Importieren der OpenApi 3.0-Definition aus JSON-Dokument hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="3f978-876">„New-AzApiManagementIdentityProvider“ und „Set-AzApiManagementIdentityProvider“: Unterstützung für das Konfigurieren des Anmeldemandanten für AAD B2C-Anbieter hinzugefügt [#9784]</span><span class="sxs-lookup"><span data-stu-id="3f978-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-878">Verweis auf System.Buffers in csproj und psd1 explizit hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-879">Az.IotHub</span></span>
* <span data-ttu-id="3f978-880">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="3f978-881">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="3f978-882">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-883">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-884">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-885">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="3f978-886">Unterstützung für die Verwaltung von Modulen auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="3f978-887">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="3f978-888">„Add-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="3f978-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="3f978-889">„Get-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="3f978-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="3f978-890">„Remove-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="3f978-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="3f978-891">„Set-AzIotHubModule“</span><span class="sxs-lookup"><span data-stu-id="3f978-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="3f978-892">Cmdlet zum Abrufen der Verbindungszeichenfolge eines IoT-Zielgeräts in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="3f978-893">Cmdlet zum Abrufen der Verbindungszeichenfolge eines Moduls auf einem IoT-Zielgerät in einem IoT-Hub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="3f978-894">Unterstützung für das Abrufen/Festlegen des übergeordneten Geräts eines IoT-Geräts hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="3f978-895">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="3f978-896">„Get-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="3f978-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="3f978-897">„Set-AzIotHubDeviceParent“</span><span class="sxs-lookup"><span data-stu-id="3f978-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="3f978-898">Unterstützung für die Verwaltung der Beziehung zwischen über- und untergeordneten Geräten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-899">Az.Monitor</span></span>
* <span data-ttu-id="3f978-900">Ausgabewert für „Get-AzMetricDefinition“ korrigiert [#9714]</span><span class="sxs-lookup"><span data-stu-id="3f978-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-901">Az.Network</span></span>
* <span data-ttu-id="3f978-902">SQL Management SDK aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="3f978-903">Es wurde ein Problem mit dem Namensunterschied in der PrivateLinkServiceConnectionState-Klasse behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="3f978-904">Zuordnung des Felds „ActionsRequired“ zu „ActionRequired“.</span><span class="sxs-lookup"><span data-stu-id="3f978-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="3f978-905">PublicNetworkAccess zu „New-AzSqlServer“ und „Set-AzSqlServer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-906">Az.Resources</span></span>
* <span data-ttu-id="3f978-907">Für Nullverweisfehler in „Get-AzRoleAssignment“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="3f978-908">Switch „-Force“ und „-PassThru“ in „Remove-AzADGroup“ als optional gekennzeichnet [#10849]</span><span class="sxs-lookup"><span data-stu-id="3f978-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="3f978-909">Problem behoben, dass „MailNickname“ nicht zurückgegeben wird, in „Remove-AzADGroup“ behoben [#11167]</span><span class="sxs-lookup"><span data-stu-id="3f978-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="3f978-910">Problem behoben, dass Pipe-Vorgang „Remove-AzADGroup“ nicht funktioniert [#11171]</span><span class="sxs-lookup"><span data-stu-id="3f978-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="3f978-911">Für Nullverweisfehler in GetAzureRoleAssignmentCommand behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="3f978-912">Breaking Change-Attribute für bevorstehende Änderungen an Richtlinien-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="3f978-913">„Get-AzResourceGroup“ aktualisiert, sodass jetzt serverseitig nach Ressourcengruppentags gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="3f978-914">Tag-Cmdlets so erweitert, dass „-ResourceId“ akzeptiert wird</span><span class="sxs-lookup"><span data-stu-id="3f978-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="3f978-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f978-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="3f978-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f978-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="3f978-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f978-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="3f978-918">Neues Tag-Cmdlet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="3f978-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f978-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="3f978-920">ScopedDeployment aus SDK 3.3.0 übernommen</span><span class="sxs-lookup"><span data-stu-id="3f978-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-921">Az.Sql</span></span>
* <span data-ttu-id="3f978-922">Publicnetworkaccess wurde "New-azsqlserver" und "Set-azsqlserver" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="3f978-923">Unterstützung für die Konfiguration der Sicherung der Langzeitaufbewahrung für verwaltete Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="3f978-924">Einrichten/Festlegen der LTR-Richtlinie für eine verwaltete Datenbank</span><span class="sxs-lookup"><span data-stu-id="3f978-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="3f978-925">Abrufen von Sicherungen nach verwalteter Datenbank, verwalteter Instanz oder nach Speicherort</span><span class="sxs-lookup"><span data-stu-id="3f978-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="3f978-926">Entfernen einer LTR-Sicherung</span><span class="sxs-lookup"><span data-stu-id="3f978-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="3f978-927">Wiederherstellen einer LTR-Sicherung zum Erstellen einer neuen verwalteten Datenbank</span><span class="sxs-lookup"><span data-stu-id="3f978-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="3f978-928">MinimalTlsVersion wurde zu New-AzSqlServer und Set-AzSqlServer hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="3f978-929">MinimalTlsVersion wurde zu New-AzSqlInstance und Set-AzSqlInstance hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="3f978-930">SQL SDK-Version für Az.Network festgelegt</span><span class="sxs-lookup"><span data-stu-id="3f978-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-931">Az.Storage</span></span>
* <span data-ttu-id="3f978-932">Unterstützung von AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="3f978-933">„Set-AzRmStorageContainerImmutabilityPolicy“</span><span class="sxs-lookup"><span data-stu-id="3f978-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="3f978-934">Warnmeldung für Breaking Change hinzugefügt: Typänderung für „AzureStorageTable“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="3f978-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="3f978-935">„New-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="3f978-936">„Get-AzStorageTable“</span><span class="sxs-lookup"><span data-stu-id="3f978-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-937">Az.Websites</span></span>
* <span data-ttu-id="3f978-938">Tag-Parameter für „New-AzAppServicePlan“ und „Set-AzAppServicePlan“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="3f978-939">Beenden der Cmdlet-Ausführung, wenn beim Hinzufügen einer benutzerdefinierten Domäne zu einer Website eine Ausnahme ausgelöst wird</span><span class="sxs-lookup"><span data-stu-id="3f978-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="3f978-940">Unterstützung zur Durchführung von Vorgängen für App Services hinzugefügt, die sich nicht in der gleichen Ressourcengruppe wie der App Service-Plan befinden</span><span class="sxs-lookup"><span data-stu-id="3f978-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="3f978-941">Zugriffseinschränkung auf WebApp/Funktion in verschiedenen Ressourcengruppen angewendet</span><span class="sxs-lookup"><span data-stu-id="3f978-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="3f978-942">Problem beim Festlegen von benutzerdefinierten Hostnamen für WebAppSlots behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="3f978-943">3.5.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-944">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-944">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-945">Clientseitige Telemetrie aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="3f978-946">Cmdlets zur Unterstützung der Geräteverwaltung in Az.IotHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="3f978-947">Cmdlets für Verfügbarkeitsgruppenlistener in Az.SqlVirtualMachine hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-948">Az.Accounts</span></span>
* <span data-ttu-id="3f978-949">Abonnement-ID, Mandanten-ID und Ausführungszeit in clientseitigen Telemetriedaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-950">Az.Automation</span></span>
* <span data-ttu-id="3f978-951">Tippfehler in Beispiel 1 in der Referenzdokumentation für „New-AzAutomationSoftwareUpdateConfiguration“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-953">SDK auf 7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="3f978-954">Verbesserte Fehlermeldung, wenn der Server mit leerem Text antwortet</span><span class="sxs-lookup"><span data-stu-id="3f978-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-955">Az.Compute</span></span>
* <span data-ttu-id="3f978-956">Zulässiger leerer Wert für „ProximityPlacementGroupId“ während des Updates</span><span class="sxs-lookup"><span data-stu-id="3f978-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-957">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-958">Cmdlet zum Abrufen verwalteter Regeldefinitionen hinzugefügt, die in WAF verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="3f978-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-959">Az.IotHub</span></span>
* <span data-ttu-id="3f978-960">Unterstützung für die Verwaltung von Geräten in IoT Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="3f978-961">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="3f978-962">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-963">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-964">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="3f978-965">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="3f978-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-966">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-967">Duplizierter Text für „Add-AzKeyVaultKey.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-968">Az.Monitor</span></span>
* <span data-ttu-id="3f978-969">Beschreibung des Cmdlets „Get-AzLog cmdlet“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="3f978-970">Dem Befehl „New-AzMetricAlertRuleV2“ wurde ein Parameter namens „ActionGroupId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="3f978-971">Der Benutzer kann entweder „ActionGroupId(string)“ oder „ActionGorup(ActivityLogAlertActionGroup)“ angeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-972">Az.Network</span></span>
* <span data-ttu-id="3f978-973">Zusätzlicher Parameterhinweis für den Parameter „-EnableProxyProtocol“ für das Cmdlet „New-AzPrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="3f978-974">FilterData-Beispiel in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="3f978-975">Paketerfassungsbeispiel für die Erfassung aller inneren und äußeren Pakete in „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="3f978-976">Unterstützte Azure Firewall-Richtlinie für VNET-Firewalls</span><span class="sxs-lookup"><span data-stu-id="3f978-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="3f978-977">Keine neuen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-977">No new cmdlets are added.</span></span> <span data-ttu-id="3f978-978">Die Einschränkung für die Firewallrichtlinie für VNET-Firewalls wurde gelockert.</span><span class="sxs-lookup"><span data-stu-id="3f978-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-980">Unterstützung für „Als Dateien wiederherstellen“ für SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-981">Az.Resources</span></span>
* <span data-ttu-id="3f978-982">Cmdlets für die Vorlagenbereitstellung umgestaltet</span><span class="sxs-lookup"><span data-stu-id="3f978-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="3f978-983">Neue Cmdlets zur Verwaltung von Bereitstellungen in der Verwaltungsgruppe hinzugefügt: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3f978-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="3f978-984">Neue Cmdlets zur Verwaltung von Bereitstellungen im Mandantenbereich hinzugefügt: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="3f978-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="3f978-985">Cmdlets vom Typ „\*-AzDeployment“ für den speziellen Einsatz im Abonnementbereich umgestaltet</span><span class="sxs-lookup"><span data-stu-id="3f978-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="3f978-986">Aliase vom Typ „*-AzSubscriptionDeployment“ für Cmdlets vom Typ „*-AzDeployment“ erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="3f978-987">„Update-AzADApplication“ korrigiert, wenn der Parameter „AvailableToOtherTenants“ nicht festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="3f978-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="3f978-988">„ApplicationObjectWithoutCredentialParameterSet“ entfernt, um „AmbiguousParameterSetException“ zu vermeiden</span><span class="sxs-lookup"><span data-stu-id="3f978-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="3f978-989">Hilfedateien erneut generiert</span><span class="sxs-lookup"><span data-stu-id="3f978-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-990">Az.Sql</span></span>
* <span data-ttu-id="3f978-991">Unterstützung für abonnementübergreifende Point-in-Time-Wiederherstellung für verwaltete Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="3f978-992">Unterstützung für die Änderung der Hardwaregeneration von vorhandenen verwalteten SQL-Instanzen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="3f978-993">Hilfebeispiele für „Update-AzSqlServerVulnerabilityAssessmentSetting“ korrigiert: parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="3f978-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="3f978-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3f978-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="3f978-995">Cmdlets für Verfügbarkeitsgruppenlistener hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3f978-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3f978-996">Az.StorageSync</span></span>
* <span data-ttu-id="3f978-997">Unterstützte Zeichensätze in „Invoke-AzStorageSyncCompatibilityCheck“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="3f978-998">3.4.0: Februar 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-999">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-999">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-1000">Az.CosmosDB: erste Version 0.1.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="3f978-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="3f978-1001">Unterstützung für Az.Network ConnectionMonitor V2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1002">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1003">Deaktivieren der automatischen Kontextspeicherung, wenn „AzureRmContext.json“ nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="3f978-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="3f978-1004">Aktualisieren des Verweises auf Azure Powershell Common auf 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="3f978-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-1006">**Get-AzApiManagementApiSchema** Fehler beim Abrufen des einer API zugeordneten Open-Api-Schemas behoben   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="3f978-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="3f978-1007">**New-AzApiManagementProduct**\* und **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="3f978-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="3f978-1008">Dokumentation korrigiert für https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="3f978-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="3f978-1009">**Set-AzApiManagementApi** Beispiel hinzugefügt, das das Aktualisieren von ServiceUrl mithilfe des Cmdlets veranschaulicht</span><span class="sxs-lookup"><span data-stu-id="3f978-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1010">Az.Compute</span></span>
* <span data-ttu-id="3f978-1011">Anzahl des VM-Status auf 100 beschränkt, um die Drosselung zu vermeiden, wenn „Get-AzVM -Status“ ohne VM-Name ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="3f978-1012">Cmdlet „Update-AzDiskEncryptionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="3f978-1013">Die Parameter „EncryptionType“ und „DiskEncryptionSetId“ wurden den folgenden Cmdlets hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="3f978-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="3f978-1015">Parameter „ColocationStatus“ zum Cmdlet „Get-AzProximityPlacementGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1016">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1017">Version des ADF .NET SDK auf 4.7.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3f978-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3f978-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="3f978-1019">LIST-Vorgänge für Ressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="3f978-1020">Funktionen zum Ausführen von Vorgängen für Integritätsprüfungsschritte hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-1021">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-1022">Dokumentationsfehler für „New-AzHDInsightCluster“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-1023">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-1024">Namensalias zum VaultName-Attribut hinzugefügt, um „Remove-AzureKeyVault“ mit „New-AzureKeyVault“ konsistent zu machen</span><span class="sxs-lookup"><span data-stu-id="3f978-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1025">Az.Network</span></span>
* <span data-ttu-id="3f978-1026">Neues Beispiel zu „Set-AzNetworkWatcherConfigFlowLog.md“ hinzugefügt, um das Szenario zur Traffic Analytics-Deaktivierung zu veranschaulichen</span><span class="sxs-lookup"><span data-stu-id="3f978-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="3f978-1027">Unterstützung für die Zuweisung der IP-Verwaltungskonfiguration zu Azure Firewall hinzugefügt: ein dediziertes Subnetz und eine öffentliche IP-Adresse, die von der Firewall für den Verwaltungsdatenverkehr verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f978-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="3f978-1028">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="3f978-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3f978-1029">Parameter „-ManagementPublicIpAddress“ (nicht obligatorisch) hinzugefügt, der ein Objekt für die öffentliche IP-Adresse akzeptiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="3f978-1030">Methode „SetManagementIpConfiguration“ für Firewallobjekt hinzugefügt. Erfordert ein Subnetz und eine öffentliche IP-Adresse als Eingabe, und der Subnetzname muss „AzureFirewallManagementSubnet“ lauten.</span><span class="sxs-lookup"><span data-stu-id="3f978-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="3f978-1031">Beispiele für „Get-AzNetworkSecurityGroup“ korrigiert, um Beispiele für Netzwerksicherheitsgruppen und nicht für Netzwerkschnittstellen anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="3f978-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="3f978-1032">Tippfehler im Befehl „New-AzVpnSite“ korrigiert, der dazu führte, dass die Vervollständigung für die Ressourcen-ID einen Parameter nicht vervollständigen konnte</span><span class="sxs-lookup"><span data-stu-id="3f978-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="3f978-1033">Unterstützung für die URL-Konfiguration im Aktionssatz für Neuschreibungsregeln in Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="3f978-1034">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="3f978-1036">Cmdlets mit optionalem Parameter aktualisiert: UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="3f978-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3f978-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="3f978-1038">Unterstützung für Ressourcen der Version 2 von NetworkWatcher ConnectionMonitor hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-1040">Unterstützung der Konformitätsbewertung vor der Ermittlung der zu korrigierenden Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3f978-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="3f978-1041">Parameter „-ResourceDiscoverMode“ zu „Start-AzPolicyRemediation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="3f978-1042">Cmdlet „Get-AzPolicyMetadata“ zum Abrufen der Ressourcen für Richtlinienmetadaten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="3f978-1043">„Get-AzPolicyState“ und „Get-AzPolicyStateSummary“ für API-Version 2019-10-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1045">Azure Site Recovery-Unterstützung für das Entfernen eines replizierten Datenträgers</span><span class="sxs-lookup"><span data-stu-id="3f978-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="3f978-1046">In Azure Backup wurde Unterstützung zum Hinzufügen von Tags bei der Erstellung eines Recovery Services-Tresors hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1047">Az.Resources</span></span>
* <span data-ttu-id="3f978-1048">„-Scope“ in Cmdlets vom Typ „\*-AzPolicyAssignment“ nun optional (standardmäßig auf Abonnementkontext festgelegt)</span><span class="sxs-lookup"><span data-stu-id="3f978-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="3f978-1049">Beispiele zum Erstellen von „ADServicePrincipal“ mit Kennwort und Schlüsselanmeldeinformation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1050">Az.Sql</span></span>
<span data-ttu-id="3f978-1051">Cmdlet „New-AzSqlDatabaseSecondary“ korrigiert, um auf die Existenz von „PartnerDatabaseName“ anstelle von „DatabaseName“ zu prüfen</span><span class="sxs-lookup"><span data-stu-id="3f978-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1052">Az.Storage</span></span>
* <span data-ttu-id="3f978-1053">Unterstützung für das Festlegen des Schlüsseltyps für die Tabellen-/Warteschlangenverschlüsselung beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3f978-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="3f978-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="3f978-1055">Anzeigen der Anforderungs-ID (RequestId), wenn für „StorageException“ keine erweiterten Fehlerinformationen (ExtendedErrorInformation) vorliegen</span><span class="sxs-lookup"><span data-stu-id="3f978-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="3f978-1056">Beispiel 6 des Cmdlets „Start-AzStorageBlobCopy“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1057">Az.Websites</span></span>
* <span data-ttu-id="3f978-1058">„Set-AzWebapp“ und „Set-AzWebappSlot“ unterstützen die Eigenschaften „AlwaysOn“, „MinTls“ und „FtpsState“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="3f978-1059">Problem behoben, das dazu führte, dass beim Festlegen von „HttpsOnly“ bei gleichzeitiger Änderung von „AppservicePlan“ mit dem einzelnen Befehl „Set-AzWebApp“ „HttpsOnly“ auf den Standardwert zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="3f978-1060">3.3.0 – Januar 2020</span><span class="sxs-lookup"><span data-stu-id="3f978-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1061">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1062">„Add-AzEnvironment“ und „Set-AzEnvironment“ wurden so aktualisiert, dass sie jetzt die Parameter „AzureAttestationServiceEndpointResourceId“ und „AzureAttestationServiceEndpointSuffix“ akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3f978-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-1063">Az.Cdn</span></span>
* <span data-ttu-id="3f978-1064">Anzeigen von Fehlerantwortdetails im Cmdlet „New-AzCdnEndpoint“</span><span class="sxs-lookup"><span data-stu-id="3f978-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1065">Az.Compute</span></span>
* <span data-ttu-id="3f978-1066">Cmdlet „Set-AzVMCustomScriptExtension“ für eine VM mit verwaltetem Betriebssystemdatenträger ohne Betriebssystemprofil wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="3f978-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="3f978-1068">Im Beispiel von „New-AzContainerGroup“ verwendete Parameternamen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="3f978-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3f978-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="3f978-1070">Cmdlet „Get-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3f978-1071">Edge-Speichercontainer abrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="3f978-1072">Cmdlet „New-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3f978-1073">Neuen Edge-Speichercontainer erstellen</span><span class="sxs-lookup"><span data-stu-id="3f978-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="3f978-1074">Cmdlet „Remove-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3f978-1075">Edge-Speichercontainer entfernen</span><span class="sxs-lookup"><span data-stu-id="3f978-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="3f978-1076">Cmdlet „Invoke-AzDataBoxEdgeStorageContainer“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="3f978-1077">Aktion zum Aktualisieren von Daten in Edge-Speichercontainer aufrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="3f978-1078">Cmdlet „Get-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3f978-1079">Edge-Speicherkonto abrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="3f978-1080">Cmdlet „New-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3f978-1081">Neues Edge-Speicherkonto erstellen</span><span class="sxs-lookup"><span data-stu-id="3f978-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="3f978-1082">Cmdlet „Remove-AzDataBoxEdgeStorageAccount“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="3f978-1083">Edge-Speicherkonto entfernen</span><span class="sxs-lookup"><span data-stu-id="3f978-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="3f978-1084">Cmdlet „Invoke-AzDataBoxEdgeShare“ aufrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="3f978-1085">Aktion zum Aktualisieren von Daten auf Freigabe aufrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="3f978-1086">Cmdlet „Set-AzDataBoxEdgeStorageAccountCredential“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="3f978-1087">Festlegen der Speicherkonto-Anmeldeinformationen für „az databoxedge“</span><span class="sxs-lookup"><span data-stu-id="3f978-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1088">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1089">Eigenschaften „AutoUpdateETA“, „LatestVersion“, „PushedVersion“, „TaskQueueId“ und „VersionStatus“ für Befehl „Get-AzDataFactoryV2IntegrationRuntime“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="3f978-1090">Version des ADF .NET SDK auf 4.6.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="3f978-1091">Parameter „PublicIPs“ wurde für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um das Erstellen der Azure-SSIS Integration Runtime mit statischen öffentlichen IP-Adressen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="3f978-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="3f978-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="3f978-1093">Fehlerhafter Link in „Get-AzDtlAllowedVMSizesPolicy.md“ entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1094">Az.EventHub</span></span>
* <span data-ttu-id="3f978-1095">Behebung des Problems 10634: Verweis auf NULL-Objekt für „remove eventhubnamespace“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-1096">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-1097">Fehler in „Invoke-AzHDInsightHiveJob.md“ wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3f978-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3f978-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="3f978-1099">Die folgenden Cmdlets wurden entfernt, da „MachineLearningCompute“ nicht mehr verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f978-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="3f978-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3f978-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="3f978-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="3f978-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3f978-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="3f978-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3f978-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="3f978-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3f978-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="3f978-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="3f978-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="3f978-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="3f978-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1107">Az.Network</span></span>
* <span data-ttu-id="3f978-1108">Upgrade der Abhängigkeit von „Microsoft.Azure.Management.Sql“ von „1.36-preview“ auf „1.37-preview“</span><span class="sxs-lookup"><span data-stu-id="3f978-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1110">Änderung der Azure Site Recovery-Unterstützung für virtuelle Computer mit verwalteten Datenträgern, die im Ruhezustand mit kundenseitig verwalteten Schlüsseln für Azure-zu-Azure-Anbieter verschlüsselt sind</span><span class="sxs-lookup"><span data-stu-id="3f978-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="3f978-1111">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="3f978-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="3f978-1112">Azure Site Recovery-Unterstützung für die Eingabe der ID des Datenträgerverschlüsselungssatzes als optionale Eingabe auf Datenträgerebene beim Aktivieren des Schutzes für VMware in Azure</span><span class="sxs-lookup"><span data-stu-id="3f978-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="3f978-1113">Azure Site Recovery-Unterstützung zum Aktualisieren eines replikationsgeschützten Elements mit der Zuordnung eines Datenträgerverschlüsselungssatzes für HyperV in Azure</span><span class="sxs-lookup"><span data-stu-id="3f978-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1114">Az.Resources</span></span>
* <span data-ttu-id="3f978-1115">Fehler in Hilfedokument zu „Remove-AzTag“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1116">Az.Sql</span></span>
* <span data-ttu-id="3f978-1117">Funktionalität der Baseline-Cmdlets für einen Sicherheitsrisikobewertungssatz korrigiert, sodass sie auf der Master-Datenbank für Azure Database funktionieren und sie auf Systemdatenbanken von verwalteten Instanzen einschränken.</span><span class="sxs-lookup"><span data-stu-id="3f978-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="3f978-1118">Fehler beim Erstellen einer SQL-Instanzfailovergruppe behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="3f978-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3f978-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="3f978-1120">DR als neuer gültiger Lizenztyp hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1121">Az.Storage</span></span>
* <span data-ttu-id="3f978-1122">Warnmeldung für Breaking Change hinzugefügt: Wertänderung für „DefaultAction“ in einer zukünftigen Version</span><span class="sxs-lookup"><span data-stu-id="3f978-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="3f978-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="3f978-1124">Unterstützung für das Abrufen der letzten Synchronisierungszeit des Speicherkontos durch Ausführen von „get-AzureRMStorageAccount“ mit Parameter „-IncludeGeoReplicationStats“</span><span class="sxs-lookup"><span data-stu-id="3f978-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="3f978-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="3f978-1126">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="3f978-1127">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-1127">General</span></span>
* <span data-ttu-id="3f978-1128">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1129">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1130">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="3f978-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="3f978-1131">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="3f978-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-1132">Az.Batch</span></span>
* <span data-ttu-id="3f978-1133">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1134">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1135">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-1137">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="3f978-1138">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3f978-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3f978-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="3f978-1140">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="3f978-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-1141">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-1142">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="3f978-1143">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="3f978-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="3f978-1144">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-1145">Az.Monitor</span></span>
* <span data-ttu-id="3f978-1146">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="3f978-1147">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="3f978-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="3f978-1148">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="3f978-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1149">Az.Network</span></span>
* <span data-ttu-id="3f978-1150">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="3f978-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1151">Az.Resources</span></span>
* <span data-ttu-id="3f978-1152">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="3f978-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="3f978-1153">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="3f978-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1154">Az.Sql</span></span>
* <span data-ttu-id="3f978-1155">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1156">Az.Storage</span></span>
* <span data-ttu-id="3f978-1157">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3f978-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="3f978-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="3f978-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="3f978-1160">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="3f978-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="3f978-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="3f978-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="3f978-1162">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="3f978-1163">Unterstützung von QuotaGiB (Freigabekontingent in Gibibyte) für Werte über 5120 in der Verwaltungsebene von Dateifreigabe-Cmdlets und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="3f978-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="3f978-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="3f978-1166">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="3f978-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3f978-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="3f978-1168">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="3f978-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="3f978-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3f978-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="3f978-1170">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-1171">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-1172">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="3f978-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="3f978-1173">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="3f978-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1174">Az.Compute</span></span>
* <span data-ttu-id="3f978-1175">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="3f978-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="3f978-1176">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="3f978-1177">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="3f978-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="3f978-1178">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3f978-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="3f978-1179">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="3f978-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="3f978-1180">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3f978-1181">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="3f978-1182">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="3f978-1183">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="3f978-1184">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="3f978-1185">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="3f978-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3f978-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="3f978-1187">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3f978-1188">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="3f978-1188">Get the Order</span></span>
* <span data-ttu-id="3f978-1189">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3f978-1190">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="3f978-1190">Create new Order</span></span>
* <span data-ttu-id="3f978-1191">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3f978-1192">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="3f978-1192">Remove the Order</span></span>
* <span data-ttu-id="3f978-1193">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="3f978-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="3f978-1194">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="3f978-1194">Now creates Local Share</span></span>
* <span data-ttu-id="3f978-1195">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="3f978-1196">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="3f978-1197">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="3f978-1198">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="3f978-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="3f978-1199">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3f978-1200">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="3f978-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="3f978-1201">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3f978-1202">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="3f978-1202">Create new Triggers</span></span>
* <span data-ttu-id="3f978-1203">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3f978-1204">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="3f978-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1205">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1206">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="3f978-1207">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-1209">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1210">Az.EventHub</span></span>
* <span data-ttu-id="3f978-1211">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-1213">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="3f978-1214">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="3f978-1215">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="3f978-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="3f978-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1217">Az.Network</span></span>
* <span data-ttu-id="3f978-1218">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="3f978-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="3f978-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="3f978-1220">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1222">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="3f978-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="3f978-1223">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="3f978-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="3f978-1224">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="3f978-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3f978-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3f978-1225">Az.RedisCache</span></span>
* <span data-ttu-id="3f978-1226">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="3f978-1227">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="3f978-1228">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1229">Az.Resources</span></span>
- <span data-ttu-id="3f978-1230">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="3f978-1231">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="3f978-1232">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="3f978-1233">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="3f978-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="3f978-1234">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1235">Az.Sql</span></span>
* <span data-ttu-id="3f978-1236">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="3f978-1237">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="3f978-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="3f978-1238">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="3f978-1239">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-1239">General</span></span>
* <span data-ttu-id="3f978-1240">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3f978-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1241">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1242">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3f978-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3f978-1243">Az.Advisor</span></span>
* <span data-ttu-id="3f978-1244">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-1245">Az.Batch</span></span>
* <span data-ttu-id="3f978-1246">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="3f978-1247">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="3f978-1248">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="3f978-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="3f978-1249">Für Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="3f978-1250">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="3f978-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="3f978-1251">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="3f978-1252">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="3f978-1253">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="3f978-1254">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="3f978-1255">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3f978-1256">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="3f978-1257">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="3f978-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="3f978-1258">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3f978-1259">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="3f978-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="3f978-1260">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="3f978-1261">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="3f978-1262">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="3f978-1263">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="3f978-1264">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="3f978-1265">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="3f978-1266">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3f978-1267">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3f978-1268">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="3f978-1269">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="3f978-1270">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="3f978-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="3f978-1271">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="3f978-1272">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="3f978-1273">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="3f978-1274">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="3f978-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="3f978-1275">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="3f978-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="3f978-1276">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="3f978-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="3f978-1277">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="3f978-1278">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="3f978-1279">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="3f978-1280">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="3f978-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="3f978-1281">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="3f978-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-1282">Az.Cdn</span></span>
* <span data-ttu-id="3f978-1283">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="3f978-1284">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1285">Az.Compute</span></span>
* <span data-ttu-id="3f978-1286">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="3f978-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="3f978-1287">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3f978-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="3f978-1288">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3f978-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="3f978-1289">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3f978-1290">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="3f978-1291">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="3f978-1292">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="3f978-1293">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="3f978-1293">Breaking changes</span></span>
    - <span data-ttu-id="3f978-1294">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3f978-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="3f978-1295">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1296">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1297">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-1299">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="3f978-1300">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="3f978-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="3f978-1301">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="3f978-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="3f978-1302">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="3f978-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="3f978-1303">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="3f978-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="3f978-1304">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="3f978-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-1306">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-1307">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-1308">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="3f978-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="3f978-1309">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="3f978-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="3f978-1310">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="3f978-1311">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="3f978-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3f978-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3f978-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3f978-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3f978-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3f978-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3f978-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3f978-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="3f978-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3f978-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="3f978-1317">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="3f978-1318">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3f978-1319">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3f978-1320">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="3f978-1321">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="3f978-1322">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="3f978-1323">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="3f978-1324">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="3f978-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="3f978-1325">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="3f978-1326">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="3f978-1327">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="3f978-1328">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="3f978-1329">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1330">Az.IotHub</span></span>
* <span data-ttu-id="3f978-1331">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="3f978-1331">Breaking changes:</span></span>
    - <span data-ttu-id="3f978-1332">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3f978-1333">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3f978-1334">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3f978-1335">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3f978-1336">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="3f978-1337">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="3f978-1338">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="3f978-1339">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="3f978-1340">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3f978-1341">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3f978-1342">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3f978-1343">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1345">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1346">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="3f978-1347">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="3f978-1348">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1349">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1350">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1351">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1352">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-1353">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1354">Az.Resources</span></span>
* <span data-ttu-id="3f978-1355">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1356">Az.Network</span></span>
* <span data-ttu-id="3f978-1357">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="3f978-1358">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="3f978-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3f978-1364">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="3f978-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="3f978-1365">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-1365">New cmdlet:</span></span>
        - <span data-ttu-id="3f978-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3f978-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="3f978-1367">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="3f978-1368">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="3f978-1369">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="3f978-1370">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="3f978-1371">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="3f978-1372">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="3f978-1373">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="3f978-1374">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3f978-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="3f978-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3f978-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3f978-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3f978-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="3f978-1380">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="3f978-1381">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3f978-1382">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3f978-1383">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3f978-1384">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="3f978-1385">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="3f978-1386">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="3f978-1387">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="3f978-1389">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3f978-1390">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3f978-1391">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3f978-1392">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3f978-1393">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3f978-1394">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="3f978-1395">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="3f978-1396">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="3f978-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="3f978-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="3f978-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="3f978-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3f978-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="3f978-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3f978-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="3f978-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="3f978-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="3f978-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="3f978-1403">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3f978-1404">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="3f978-1405">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="3f978-1406">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="3f978-1407">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="3f978-1408">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3f978-1409">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="3f978-1410">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="3f978-1411">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="3f978-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="3f978-1412">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="3f978-1413">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="3f978-1414">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="3f978-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="3f978-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="3f978-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-1420">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="3f978-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1421">Az.Sql</span></span>
* <span data-ttu-id="3f978-1422">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="3f978-1423">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="3f978-1424">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="3f978-1425">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="3f978-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="3f978-1426">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="3f978-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="3f978-1427">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3f978-1428">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="3f978-1429">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="3f978-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="3f978-1430">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1431">Az.Storage</span></span>
* <span data-ttu-id="3f978-1432">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="3f978-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3f978-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3f978-1435">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="3f978-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3f978-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="3f978-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3f978-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="3f978-1438">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="3f978-1439">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-1439">General</span></span>
* <span data-ttu-id="3f978-1440">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="3f978-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1441">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1442">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-1444">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="3f978-1445">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="3f978-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-1446">Az.Automation</span></span>
* <span data-ttu-id="3f978-1447">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-1448">Az.Batch</span></span>
* <span data-ttu-id="3f978-1449">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1450">Az.Compute</span></span>
* <span data-ttu-id="3f978-1451">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3f978-1452">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="3f978-1453">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="3f978-1454">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="3f978-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1455">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1456">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="3f978-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="3f978-1457">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="3f978-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="3f978-1458">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-1460">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="3f978-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3f978-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3f978-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="3f978-1462">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="3f978-1463">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="3f978-1464">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="3f978-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="3f978-1465">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1466">Az.IotHub</span></span>
* <span data-ttu-id="3f978-1467">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="3f978-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="3f978-1468">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="3f978-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-1469">Az.Monitor</span></span>
* <span data-ttu-id="3f978-1470">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3f978-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="3f978-1471">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="3f978-1472">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="3f978-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="3f978-1473">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="3f978-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1474">Az.Network</span></span>
* <span data-ttu-id="3f978-1475">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="3f978-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="3f978-1476">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="3f978-1477">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="3f978-1479">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3f978-1480">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="3f978-1481">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="3f978-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3f978-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3f978-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3f978-1485">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="3f978-1486">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="3f978-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="3f978-1487">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="3f978-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="3f978-1488">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="3f978-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3f978-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3f978-1489">Az.RedisCache</span></span>
* <span data-ttu-id="3f978-1490">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="3f978-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1491">Az.Sql</span></span>
* <span data-ttu-id="3f978-1492">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1493">Az.Storage</span></span>
* <span data-ttu-id="3f978-1494">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="3f978-1495">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="3f978-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3f978-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f978-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="3f978-1497">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="3f978-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3f978-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3f978-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3f978-1499">Az.StorageSync</span></span>
* <span data-ttu-id="3f978-1500">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1501">Az.Websites</span></span>
* <span data-ttu-id="3f978-1502">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="3f978-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="3f978-1503">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3f978-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-1505">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="3f978-1506">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="3f978-1507">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-1508">Az.Automation</span></span>
* <span data-ttu-id="3f978-1509">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="3f978-1510">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="3f978-1511">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1512">Az.Compute</span></span>
* <span data-ttu-id="3f978-1513">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="3f978-1514">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3f978-1515">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="3f978-1516">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="3f978-1517">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="3f978-1518">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="3f978-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="3f978-1519">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="3f978-1520">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="3f978-1521">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1522">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1523">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3f978-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="3f978-1524">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-1525">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-1526">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1527">Az.IotHub</span></span>
* <span data-ttu-id="3f978-1528">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="3f978-1529">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="3f978-1530">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="3f978-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="3f978-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3f978-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3f978-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3f978-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3f978-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3f978-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3f978-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3f978-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-1535">Az.Monitor</span></span>
* <span data-ttu-id="3f978-1536">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="3f978-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="3f978-1537">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="3f978-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="3f978-1538">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3f978-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="3f978-1539">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="3f978-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="3f978-1540">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="3f978-1541">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="3f978-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="3f978-1542">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="3f978-1543">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3f978-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="3f978-1544">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3f978-1545">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3f978-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="3f978-1546">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3f978-1547">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3f978-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="3f978-1548">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="3f978-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="3f978-1549">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="3f978-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="3f978-1550">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="3f978-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="3f978-1551">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="3f978-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="3f978-1552">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="3f978-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="3f978-1553">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="3f978-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="3f978-1554">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="3f978-1555">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-1555">Overall improved help files</span></span>
* <span data-ttu-id="3f978-1556">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1557">Az.Network</span></span>
* <span data-ttu-id="3f978-1558">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="3f978-1559">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="3f978-1560">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="3f978-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="3f978-1561">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="3f978-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="3f978-1562">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="3f978-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="3f978-1563">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="3f978-1564">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="3f978-1565">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="3f978-1566">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="3f978-1567">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="3f978-1568">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="3f978-1569">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="3f978-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="3f978-1570">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1570">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3f978-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="3f978-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="3f978-1573">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="3f978-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3f978-1574">New-VpnSite</span></span>
        - <span data-ttu-id="3f978-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3f978-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="3f978-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="3f978-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="3f978-1578">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f978-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1580">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="3f978-1581">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1582">Az.Resources</span></span>
* <span data-ttu-id="3f978-1583">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="3f978-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-1585">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="3f978-1586">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="3f978-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3f978-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3f978-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3f978-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3f978-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3f978-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3f978-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3f978-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="3f978-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3f978-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3f978-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3f978-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3f978-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3f978-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3f978-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3f978-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3f978-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3f978-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="3f978-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3f978-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3f978-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3f978-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3f978-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3f978-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3f978-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="3f978-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="3f978-1600">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="3f978-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3f978-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3f978-1601">Az.SignalR</span></span>
* <span data-ttu-id="3f978-1602">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1603">Az.Sql</span></span>
* <span data-ttu-id="3f978-1604">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="3f978-1605">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="3f978-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="3f978-1606">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="3f978-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3f978-1607">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="3f978-1608">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="3f978-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1609">Az.Storage</span></span>
* <span data-ttu-id="3f978-1610">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3f978-1611">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="3f978-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3f978-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="3f978-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3f978-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="3f978-1614">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="3f978-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3f978-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="3f978-1616">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="3f978-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="3f978-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3f978-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3f978-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3f978-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f978-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1621">Az.Websites</span></span>
* <span data-ttu-id="3f978-1622">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="3f978-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="3f978-1623">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="3f978-1624">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="3f978-1625">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="3f978-1626">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-1626">General</span></span>
* <span data-ttu-id="3f978-1627">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1628">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1629">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="3f978-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-1630">Az.Aks</span></span>
* <span data-ttu-id="3f978-1631">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="3f978-1632">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="3f978-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-1634">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="3f978-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="3f978-1635">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="3f978-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="3f978-1636">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="3f978-1637">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="3f978-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="3f978-1638">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3f978-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-1639">Az.Batch</span></span>
* <span data-ttu-id="3f978-1640">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="3f978-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-1641">Az.Cdn</span></span>
* <span data-ttu-id="3f978-1642">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1643">Az.Compute</span></span>
* <span data-ttu-id="3f978-1644">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="3f978-1645">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="3f978-1646">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="3f978-1647">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="3f978-1648">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="3f978-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="3f978-1649">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="3f978-1650">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="3f978-1651">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1652">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1653">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="3f978-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="3f978-1654">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="3f978-1655">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="3f978-1656">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-1658">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1659">Az.EventHub</span></span>
* <span data-ttu-id="3f978-1660">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="3f978-1661">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="3f978-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="3f978-1662">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="3f978-1663">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="3f978-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3f978-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3f978-1665">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-1666">Az.Monitor</span></span>
* <span data-ttu-id="3f978-1667">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1668">Az.Network</span></span>
* <span data-ttu-id="3f978-1669">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="3f978-1670">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="3f978-1671">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="3f978-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="3f978-1672">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="3f978-1673">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="3f978-1674">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="3f978-1675">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="3f978-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-1677">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="3f978-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="3f978-1678">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1678">Added example</span></span>
    - <span data-ttu-id="3f978-1679">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="3f978-1680">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="3f978-1681">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1683">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1684">Az.Resources</span></span>
* <span data-ttu-id="3f978-1685">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="3f978-1686">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="3f978-1687">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3f978-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="3f978-1688">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-1690">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="3f978-1691">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="3f978-1692">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-1694">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="3f978-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="3f978-1695">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="3f978-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="3f978-1696">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="3f978-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="3f978-1697">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="3f978-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="3f978-1698">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="3f978-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="3f978-1699">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="3f978-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1700">Az.Sql</span></span>
* <span data-ttu-id="3f978-1701">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1702">Az.Storage</span></span>
* <span data-ttu-id="3f978-1703">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="3f978-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="3f978-1704">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="3f978-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="3f978-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3f978-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="3f978-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3f978-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="3f978-1707">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="3f978-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="3f978-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3f978-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1709">Az.Websites</span></span>
* <span data-ttu-id="3f978-1710">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="3f978-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="3f978-1711">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1712">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1713">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3f978-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3f978-1715">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-1716">Az.Automation</span></span>
* <span data-ttu-id="3f978-1717">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-1719">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1720">Az.Compute</span></span>
* <span data-ttu-id="3f978-1721">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3f978-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3f978-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3f978-1723">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="3f978-1724">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="3f978-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1725">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1726">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="3f978-1727">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1728">Az.EventHub</span></span>
* <span data-ttu-id="3f978-1729">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3f978-1730">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-1731">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-1732">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3f978-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3f978-1733">Az.LogicApp</span></span>
* <span data-ttu-id="3f978-1734">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="3f978-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="3f978-1735">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3f978-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="3f978-1737">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1738">Az.Network</span></span>
* <span data-ttu-id="3f978-1739">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="3f978-1740">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1740">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f978-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3f978-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f978-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3f978-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3f978-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="3f978-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="3f978-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f978-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="3f978-1749">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f978-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="3f978-1750">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="3f978-1751">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="3f978-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="3f978-1752">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="3f978-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="3f978-1753">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="3f978-1754">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="3f978-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="3f978-1755">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="3f978-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3f978-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3f978-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3f978-1759">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3f978-1760">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="3f978-1761">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="3f978-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3f978-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3f978-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="3f978-1765">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="3f978-1766">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="3f978-1767">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="3f978-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-1769">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="3f978-1770">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1772">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3f978-1773">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="3f978-1774">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="3f978-1775">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3f978-1776">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="3f978-1777">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3f978-1778">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="3f978-1779">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3f978-1780">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="3f978-1781">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1782">Az.Resources</span></span>
- <span data-ttu-id="3f978-1783">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="3f978-1784">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-1786">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3f978-1787">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1788">Az.Sql</span></span>
* <span data-ttu-id="3f978-1789">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="3f978-1790">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="3f978-1791">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1792">Az.Storage</span></span>
* <span data-ttu-id="3f978-1793">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3f978-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3f978-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3f978-1794">Az.StorageSync</span></span>
* <span data-ttu-id="3f978-1795">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="3f978-1796">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1797">Az.Websites</span></span>
* <span data-ttu-id="3f978-1798">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="3f978-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="3f978-1799">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="3f978-1800">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="3f978-1801">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1802">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1803">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="3f978-1804">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="3f978-1805">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3f978-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3f978-1806">Az.Advisor</span></span>
* <span data-ttu-id="3f978-1807">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3f978-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="3f978-1808">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f978-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3f978-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-1810">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="3f978-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="3f978-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3f978-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="3f978-1812">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="3f978-1813">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="3f978-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="3f978-1814">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="3f978-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="3f978-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3f978-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="3f978-1816">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-1817">Az.Automation</span></span>
* <span data-ttu-id="3f978-1818">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1819">Az.Compute</span></span>
* <span data-ttu-id="3f978-1820">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-1821">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-1822">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3f978-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3f978-1823">Az.EventGrid</span></span>
* <span data-ttu-id="3f978-1824">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1825">Az.IotHub</span></span>
* <span data-ttu-id="3f978-1826">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1827">Az.Network</span></span>
* <span data-ttu-id="3f978-1828">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="3f978-1829">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-1831">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="3f978-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="3f978-1832">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="3f978-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-1834">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-1836">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="3f978-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1837">Az.Resources</span></span>
    - <span data-ttu-id="3f978-1838">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="3f978-1839">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="3f978-1840">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="3f978-1841">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-1843">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="3f978-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1844">Az.Sql</span></span>
* <span data-ttu-id="3f978-1845">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="3f978-1846">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="3f978-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3f978-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3f978-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3f978-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3f978-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3f978-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3f978-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="3f978-1853">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1854">Az.Storage</span></span>
* <span data-ttu-id="3f978-1855">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="3f978-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="3f978-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3f978-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="3f978-1857">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="3f978-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="3f978-1858">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="3f978-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="3f978-1859">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3f978-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="3f978-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3f978-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3f978-1862">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="3f978-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="3f978-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3f978-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="3f978-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3f978-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3f978-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3f978-1865">Az.StorageSync</span></span>
* <span data-ttu-id="3f978-1866">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f978-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="3f978-1867">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-1868">Az.Accounts</span></span>
* <span data-ttu-id="3f978-1869">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="3f978-1870">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="3f978-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="3f978-1871">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="3f978-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3f978-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="3f978-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="3f978-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1874">Az.Compute</span></span>
* <span data-ttu-id="3f978-1875">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="3f978-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="3f978-1876">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="3f978-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3f978-1877">Az.Dns</span></span>
* <span data-ttu-id="3f978-1878">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3f978-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3f978-1879">Az.EventGrid</span></span>
* <span data-ttu-id="3f978-1880">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="3f978-1881">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1881">New cmdlets:</span></span>
    - <span data-ttu-id="3f978-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3f978-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3f978-1883">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3f978-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3f978-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3f978-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3f978-1885">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3f978-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="3f978-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3f978-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3f978-1887">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="3f978-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3f978-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3f978-1889">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="3f978-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3f978-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3f978-1891">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="3f978-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3f978-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3f978-1893">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="3f978-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="3f978-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3f978-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="3f978-1895">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3f978-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="3f978-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3f978-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3f978-1897">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="3f978-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="3f978-1898">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="3f978-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3f978-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="3f978-1900">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3f978-1901">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3f978-1902">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="3f978-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="3f978-1903">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="3f978-1904">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="3f978-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="3f978-1905">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="3f978-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="3f978-1906">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="3f978-1907">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="3f978-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="3f978-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3f978-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="3f978-1909">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="3f978-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3f978-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="3f978-1911">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="3f978-1912">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="3f978-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3f978-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="3f978-1915">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="3f978-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f978-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="3f978-1917">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1918">Az.Network</span></span>
* <span data-ttu-id="3f978-1919">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="3f978-1920">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1920">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3f978-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="3f978-1922">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3f978-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="3f978-1923">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1923">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3f978-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="3f978-1925">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="3f978-1926">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1926">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f978-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3f978-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f978-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3f978-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3f978-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3f978-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="3f978-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3f978-1932">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="3f978-1933">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-1933">New cmdlets</span></span>
        - <span data-ttu-id="3f978-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f978-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3f978-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f978-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3f978-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f978-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3f978-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3f978-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="3f978-1938">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="3f978-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="3f978-1939">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="3f978-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="3f978-1940">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="3f978-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="3f978-1941">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="3f978-1942">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="3f978-1943">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="3f978-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="3f978-1944">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="3f978-1945">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="3f978-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="3f978-1946">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="3f978-1947">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="3f978-1948">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="3f978-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="3f978-1949">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="3f978-1950">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="3f978-1951">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="3f978-1952">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="3f978-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3f978-1953">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="3f978-1954">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="3f978-1955">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="3f978-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="3f978-1956">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="3f978-1957">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="3f978-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="3f978-1958">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3f978-1959">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3f978-1960">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-1962">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="3f978-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-1963">Az.Resources</span></span>
* <span data-ttu-id="3f978-1964">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="3f978-1965">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3f978-1966">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3f978-1967">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-1969">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="3f978-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-1970">Az.Sql</span></span>
* <span data-ttu-id="3f978-1971">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="3f978-1972">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="3f978-1973">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="3f978-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3f978-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3f978-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f978-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3f978-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3f978-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="3f978-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3f978-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-1979">Az.Storage</span></span>
* <span data-ttu-id="3f978-1980">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3f978-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="3f978-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="3f978-1982">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="3f978-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="3f978-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-1984">Az.Websites</span></span>
* <span data-ttu-id="3f978-1985">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="3f978-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="3f978-1986">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="3f978-1987">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3f978-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-1988">Az.Cdn</span></span>
* <span data-ttu-id="3f978-1989">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-1990">Az.Compute</span></span>
* <span data-ttu-id="3f978-1991">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3f978-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3f978-1992">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3f978-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-1993">Az.EventHub</span></span>
* <span data-ttu-id="3f978-1994">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="3f978-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3f978-1995">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="3f978-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-1996">Az.Network</span></span>
* <span data-ttu-id="3f978-1997">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3f978-1998">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-2000">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="3f978-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2002">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-2004">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="3f978-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-2006">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3f978-2007">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2008">Az.Sql</span></span>
* <span data-ttu-id="3f978-2009">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3f978-2010">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3f978-2011">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="3f978-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3f978-2012">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="3f978-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2013">Az.Websites</span></span>
* <span data-ttu-id="3f978-2014">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3f978-2015">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3f978-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-2017">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3f978-2018">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3f978-2019">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="3f978-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3f978-2020">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="3f978-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3f978-2021">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3f978-2022">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="3f978-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3f978-2023">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="3f978-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3f978-2024">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="3f978-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3f978-2025">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3f978-2026">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="3f978-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3f978-2027">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="3f978-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3f978-2028">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="3f978-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3f978-2029">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="3f978-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3f978-2030">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3f978-2031">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="3f978-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3f978-2032">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="3f978-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3f978-2033">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="3f978-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3f978-2034">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="3f978-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3f978-2035">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="3f978-2036">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="3f978-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3f978-2037">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3f978-2038">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="3f978-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3f978-2039">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="3f978-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3f978-2040">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="3f978-2041">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3f978-2042">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3f978-2043">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="3f978-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3f978-2044">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="3f978-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3f978-2045">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3f978-2046">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="3f978-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3f978-2047">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="3f978-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="3f978-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3f978-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3f978-2049">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3f978-2050">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3f978-2051">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="3f978-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3f978-2052">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3f978-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3f978-2053">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3f978-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3f978-2054">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="3f978-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3f978-2055">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="3f978-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3f978-2056">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3f978-2057">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="3f978-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3f978-2058">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3f978-2059">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="3f978-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3f978-2060">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="3f978-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="3f978-2061">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3f978-2062">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="3f978-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3f978-2063">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="3f978-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3f978-2064">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="3f978-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="3f978-2065">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3f978-2066">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="3f978-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3f978-2067">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="3f978-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3f978-2068">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="3f978-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3f978-2069">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="3f978-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3f978-2070">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3f978-2071">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="3f978-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3f978-2072">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="3f978-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3f978-2073">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3f978-2074">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="3f978-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3f978-2075">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="3f978-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3f978-2076">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3f978-2077">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3f978-2078">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="3f978-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3f978-2079">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="3f978-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3f978-2080">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3f978-2081">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="3f978-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3f978-2082">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="3f978-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3f978-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3f978-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3f978-2084">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="3f978-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3f978-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3f978-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3f978-2086">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3f978-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3f978-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3f978-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3f978-2088">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="3f978-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3f978-2089">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="3f978-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3f978-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3f978-2091">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="3f978-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="3f978-2092">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3f978-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3f978-2093">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="3f978-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2094">Az.Automation</span></span>
* <span data-ttu-id="3f978-2095">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3f978-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3f978-2096">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="3f978-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3f978-2097">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="3f978-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3f978-2098">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="3f978-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3f978-2099">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="3f978-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3f978-2100">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="3f978-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3f978-2101">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="3f978-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2102">Az.Compute</span></span>
* <span data-ttu-id="3f978-2103">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3f978-2104">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2106">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="3f978-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-2107">Az.Monitor</span></span>
* <span data-ttu-id="3f978-2108">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="3f978-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2109">Az.Network</span></span>
* <span data-ttu-id="3f978-2110">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3f978-2111">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3f978-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="3f978-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3f978-2113">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3f978-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2114">Az.Resources</span></span>
* <span data-ttu-id="3f978-2115">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2116">Az.Sql</span></span>
* <span data-ttu-id="3f978-2117">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="3f978-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3f978-2118">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2119">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2120">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="3f978-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-2122">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="3f978-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3f978-2123">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="3f978-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2124">Az.Compute</span></span>
* <span data-ttu-id="3f978-2125">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3f978-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3f978-2126">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3f978-2127">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3f978-2128">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3f978-2129">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f978-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3f978-2130">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="3f978-2131">Aktuelle Änderungen</span><span class="sxs-lookup"><span data-stu-id="3f978-2131">Breaking changes</span></span>
    - <span data-ttu-id="3f978-2132">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3f978-2133">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3f978-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3f978-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="3f978-2135">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3f978-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3f978-2136">Az.Dns</span></span>
* <span data-ttu-id="3f978-2137">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="3f978-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3f978-2138">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="3f978-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3f978-2139">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3f978-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="3f978-2141">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3f978-2142">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="3f978-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3f978-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-2143">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-2144">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="3f978-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3f978-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3f978-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3f978-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3f978-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3f978-2147">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="3f978-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3f978-2148">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="3f978-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3f978-2149">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3f978-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3f978-2150">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="3f978-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-2151">Az.Monitor</span></span>
* <span data-ttu-id="3f978-2152">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="3f978-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="3f978-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3f978-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3f978-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3f978-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3f978-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3f978-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3f978-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3f978-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3f978-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3f978-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3f978-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3f978-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3f978-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3f978-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3f978-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3f978-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3f978-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3f978-2164">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="3f978-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3f978-2165">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="3f978-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2166">Az.Network</span></span>
* <span data-ttu-id="3f978-2167">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3f978-2168">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-2168">New cmdlets</span></span>
        - <span data-ttu-id="3f978-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="3f978-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3f978-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3f978-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3f978-2173">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="3f978-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3f978-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3f978-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3f978-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3f978-2176">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3f978-2177">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="3f978-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3f978-2178">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="3f978-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-2180">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="3f978-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3f978-2181">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3f978-2182">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="3f978-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2184">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="3f978-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3f978-2185">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="3f978-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3f978-2186">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="3f978-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3f978-2187">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="3f978-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3f978-2188">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="3f978-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3f978-2189">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="3f978-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3f978-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3f978-2190">Az.Relay</span></span>
* <span data-ttu-id="3f978-2191">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="3f978-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-2193">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2194">Az.Storage</span></span>
* <span data-ttu-id="3f978-2195">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="3f978-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3f978-2196">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3f978-2197">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3f978-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="3f978-2199">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="3f978-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3f978-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3f978-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3f978-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2203">Az.Websites</span></span>
* <span data-ttu-id="3f978-2204">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3f978-2205">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3f978-2206">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-2207">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-2208">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="3f978-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="3f978-2209">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="3f978-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3f978-2210">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="3f978-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3f978-2211">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3f978-2212">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3f978-2213">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3f978-2214">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2215">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2216">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="3f978-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3f978-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-2217">Az.Batch</span></span>
* <span data-ttu-id="3f978-2218">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-2219">Az.Cdn</span></span>
* <span data-ttu-id="3f978-2220">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-2222">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2223">Az.Compute</span></span>
* <span data-ttu-id="3f978-2224">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="3f978-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3f978-2225">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2226">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-2227">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-2228">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="3f978-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2230">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3f978-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3f978-2231">Az.EventGrid</span></span>
* <span data-ttu-id="3f978-2232">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f978-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-2233">Az.EventHub</span></span>
* <span data-ttu-id="3f978-2234">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3f978-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3f978-2235">Az.HDInsight</span></span>
* <span data-ttu-id="3f978-2236">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-2237">Az.IotHub</span></span>
* <span data-ttu-id="3f978-2238">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-2239">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-2240">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2241">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3f978-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3f978-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="3f978-2243">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3f978-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3f978-2244">Az.Media</span></span>
* <span data-ttu-id="3f978-2245">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-2246">Az.Monitor</span></span>
  * <span data-ttu-id="3f978-2247">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="3f978-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3f978-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3f978-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3f978-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3f978-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3f978-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3f978-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3f978-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3f978-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3f978-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3f978-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3f978-2253">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2254">Az.Network</span></span>
* <span data-ttu-id="3f978-2255">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2256">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3f978-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3f978-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="3f978-2258">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-2260">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3f978-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3f978-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3f978-2262">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2264">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2265">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3f978-2266">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3f978-2267">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3f978-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3f978-2268">Az.RedisCache</span></span>
* <span data-ttu-id="3f978-2269">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2270">Az.Resources</span></span>
* <span data-ttu-id="3f978-2271">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2272">Az.Sql</span></span>
* <span data-ttu-id="3f978-2273">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="3f978-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3f978-2274">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2275">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="3f978-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3f978-2276">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3f978-2277">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="3f978-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3f978-2278">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="3f978-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3f978-2279">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2280">Az.Websites</span></span>
* <span data-ttu-id="3f978-2281">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="3f978-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3f978-2282">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3f978-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3f978-2283">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3f978-2284">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3f978-2285">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-2286">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-2287">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="3f978-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="3f978-2288">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="3f978-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3f978-2289">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="3f978-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3f978-2290">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3f978-2291">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3f978-2292">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3f978-2293">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3f978-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2294">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2295">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="3f978-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="3f978-2297">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3f978-2298">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2299">Az.Automation</span></span>
* <span data-ttu-id="3f978-2300">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="3f978-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3f978-2301">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3f978-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3f978-2302">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="3f978-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2303">Az.Compute</span></span>
* <span data-ttu-id="3f978-2304">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3f978-2305">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="3f978-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="3f978-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="3f978-2307">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="3f978-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-2308">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-2309">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3f978-2310">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2311">Az.Resources</span></span>
* <span data-ttu-id="3f978-2312">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3f978-2313">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3f978-2314">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="3f978-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3f978-2315">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3f978-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3f978-2316">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="3f978-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3f978-2317">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3f978-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2318">Az.Sql</span></span>
* <span data-ttu-id="3f978-2319">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="3f978-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2320">Az.Storage</span></span>
* <span data-ttu-id="3f978-2321">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="3f978-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3f978-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f978-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="3f978-2323">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="3f978-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3f978-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3f978-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3f978-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3f978-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3f978-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3f978-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3f978-2328">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="3f978-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3f978-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3f978-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3f978-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3f978-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3f978-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3f978-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3f978-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3f978-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3f978-2333">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3f978-2334">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="3f978-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="3f978-2335">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="3f978-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="3f978-2336">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="3f978-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3f978-2337">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="3f978-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3f978-2338">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3f978-2339">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3f978-2340">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3f978-2341">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2342">Az.Automation</span></span>
* <span data-ttu-id="3f978-2343">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="3f978-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3f978-2344">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="3f978-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="3f978-2345">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="3f978-2345">Pre-Post script</span></span>
    * <span data-ttu-id="3f978-2346">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="3f978-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2347">Az.Compute</span></span>
* <span data-ttu-id="3f978-2348">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3f978-2349">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-2350">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-2351">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2352">Az.Network</span></span>
* <span data-ttu-id="3f978-2353">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3f978-2354">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2356">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="3f978-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3f978-2357">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2358">Az.Resources</span></span>
* <span data-ttu-id="3f978-2359">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3f978-2360">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3f978-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2361">Az.Sql</span></span>
* <span data-ttu-id="3f978-2362">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2363">Az.Storage</span></span>
* <span data-ttu-id="3f978-2364">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3f978-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3f978-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3f978-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3f978-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3f978-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3f978-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3f978-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3f978-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3f978-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2371">Az.Websites</span></span>
* <span data-ttu-id="3f978-2372">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="3f978-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="3f978-2373">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2374">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2375">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3f978-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3f978-2376">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2377">Az.Automation</span></span>
* <span data-ttu-id="3f978-2378">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="3f978-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3f978-2379">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3f978-2380">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-2381">Az.Cdn</span></span>
* <span data-ttu-id="3f978-2382">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="3f978-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2383">Az.Compute</span></span>
* <span data-ttu-id="3f978-2384">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-2385">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-2386">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3f978-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3f978-2387">Az.LogicApp</span></span>
* <span data-ttu-id="3f978-2388">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2389">Az.Network</span></span>
* <span data-ttu-id="3f978-2390">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2392">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="3f978-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3f978-2393">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="3f978-2393">SDK Update</span></span>
* <span data-ttu-id="3f978-2394">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3f978-2395">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2396">Az.Resources</span></span>
* <span data-ttu-id="3f978-2397">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3f978-2398">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3f978-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3f978-2399">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3f978-2400">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3f978-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3f978-2401">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3f978-2402">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3f978-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2403">Az.Sql</span></span>
* <span data-ttu-id="3f978-2404">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3f978-2405">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2406">Az.Storage</span></span>
* <span data-ttu-id="3f978-2407">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f978-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3f978-2408">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="3f978-2410">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2411">Az.Automation</span></span>
* <span data-ttu-id="3f978-2412">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3f978-2413">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3f978-2414">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="3f978-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-2416">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2417">Az.Compute</span></span>
* <span data-ttu-id="3f978-2418">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3f978-2419">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3f978-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3f978-2420">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3f978-2421">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="3f978-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2423">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3f978-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3f978-2424">Az.EventHub</span></span>
* <span data-ttu-id="3f978-2425">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-2426">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-2427">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3f978-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3f978-2428">Az.LogicApp</span></span>
* <span data-ttu-id="3f978-2429">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3f978-2430">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3f978-2431">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="3f978-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3f978-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f978-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3f978-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f978-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3f978-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f978-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3f978-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f978-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3f978-2436">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3f978-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3f978-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3f978-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3f978-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3f978-2441">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3f978-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-2442">Az.Monitor</span></span>
* <span data-ttu-id="3f978-2443">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2444">Az.Network</span></span>
* <span data-ttu-id="3f978-2445">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="3f978-2447">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3f978-2448">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="3f978-2449">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="3f978-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2450">Az.Resources</span></span>
* <span data-ttu-id="3f978-2451">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3f978-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3f978-2452">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3f978-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3f978-2453">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="3f978-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3f978-2454">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="3f978-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2455">Az.Sql</span></span>
* <span data-ttu-id="3f978-2456">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3f978-2457">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="3f978-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2458">Az.Websites</span></span>
* <span data-ttu-id="3f978-2459">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3f978-2460">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2461">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2462">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="3f978-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="3f978-2464">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="3f978-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2465">Az.Compute</span></span>
* <span data-ttu-id="3f978-2466">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3f978-2467">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3f978-2468">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="3f978-2470">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="3f978-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2471">Az.Resources</span></span>
* <span data-ttu-id="3f978-2472">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="3f978-2473">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3f978-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3f978-2474">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="3f978-2475">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3f978-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2476">Az.Sql</span></span>
* <span data-ttu-id="3f978-2477">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3f978-2478">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="3f978-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3f978-2479">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3f978-2480">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2481">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2482">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3f978-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3f978-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="3f978-2484">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="3f978-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="3f978-2486">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="3f978-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3f978-2487">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2488">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2489">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3f978-2490">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3f978-2491">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3f978-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3f978-2492">Az.Aks</span></span>
* <span data-ttu-id="3f978-2493">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3f978-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2494">Az.Automation</span></span>
* <span data-ttu-id="3f978-2495">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3f978-2496">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3f978-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3f978-2497">Az.Cdn</span></span>
* <span data-ttu-id="3f978-2498">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2499">Az.Compute</span></span>
* <span data-ttu-id="3f978-2500">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3f978-2501">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3f978-2502">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3f978-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3f978-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3f978-2504">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3f978-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3f978-2505">Az.DataFactory</span></span>
* <span data-ttu-id="3f978-2506">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2508">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3f978-2509">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3f978-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3f978-2510">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-2511">Az.IotHub</span></span>
* <span data-ttu-id="3f978-2512">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3f978-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-2513">Az.KeyVault</span></span>
* <span data-ttu-id="3f978-2514">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2515">Az.Network</span></span>
* <span data-ttu-id="3f978-2516">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2517">Az.Resources</span></span>
* <span data-ttu-id="3f978-2518">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3f978-2519">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="3f978-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3f978-2520">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="3f978-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3f978-2521">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="3f978-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3f978-2522">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="3f978-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3f978-2523">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3f978-2524">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3f978-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-2526">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="3f978-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3f978-2527">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2527">Fix some error messages.</span></span>
* <span data-ttu-id="3f978-2528">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="3f978-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3f978-2529">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3f978-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3f978-2530">Az.SignalR</span></span>
* <span data-ttu-id="3f978-2531">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2532">Az.Sql</span></span>
* <span data-ttu-id="3f978-2533">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3f978-2534">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3f978-2535">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="3f978-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3f978-2536">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="3f978-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2537">Az.Storage</span></span>
* <span data-ttu-id="3f978-2538">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3f978-2539">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3f978-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3f978-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3f978-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3f978-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3f978-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3f978-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="3f978-2543">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2544">Az.Websites</span></span>
* <span data-ttu-id="3f978-2545">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3f978-2546">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3f978-2547">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3f978-2548">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="3f978-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3f978-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2549">Az.Accounts</span></span>
* <span data-ttu-id="3f978-2550">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2551">Az.Compute</span></span>
* <span data-ttu-id="3f978-2552">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="3f978-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3f978-2553">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3f978-2554">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2556">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="3f978-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3f978-2557">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3f978-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3f978-2558">Az.EventGrid</span></span>
* <span data-ttu-id="3f978-2559">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3f978-2560">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="3f978-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3f978-2561">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3f978-2562">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="3f978-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3f978-2563">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3f978-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3f978-2564">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3f978-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3f978-2565">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="3f978-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3f978-2566">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="3f978-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3f978-2567">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="3f978-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3f978-2568">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3f978-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="3f978-2569">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3f978-2570">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="3f978-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3f978-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3f978-2571">Az.IotHub</span></span>
* <span data-ttu-id="3f978-2572">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3f978-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3f978-2573">Az.LogicApp</span></span>
* <span data-ttu-id="3f978-2574">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="3f978-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2575">Az.Resources</span></span>
* <span data-ttu-id="3f978-2576">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3f978-2577">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3f978-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3f978-2578">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3f978-2579">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3f978-2580">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="3f978-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3f978-2581">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3f978-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3f978-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3f978-2582">Az.SignalR</span></span>
* <span data-ttu-id="3f978-2583">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2584">Az.Sql</span></span>
* <span data-ttu-id="3f978-2585">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3f978-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2586">Az.Storage</span></span>
* <span data-ttu-id="3f978-2587">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3f978-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f978-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="3f978-2589">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="3f978-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3f978-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3f978-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2591">Az.Websites</span></span>
* <span data-ttu-id="3f978-2592">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3f978-2593">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3f978-2594">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3f978-2595">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-2595">General</span></span>

- <span data-ttu-id="3f978-2596">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="3f978-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="3f978-2597">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="3f978-2597">Online help for each module</span></span>
- <span data-ttu-id="3f978-2598">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="3f978-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3f978-2599">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3f978-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3f978-2600">Az.Accounts</span></span>
- <span data-ttu-id="3f978-2601">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3f978-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="3f978-2602">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="3f978-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3f978-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="3f978-2604">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="3f978-2604">Fixes for #7002</span></span>
- <span data-ttu-id="3f978-2605">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3f978-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3f978-2606">Az.Batch</span></span>
- <span data-ttu-id="3f978-2607">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3f978-2608">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="3f978-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3f978-2609">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3f978-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3f978-2610">Az.Billing</span></span>
- <span data-ttu-id="3f978-2611">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3f978-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="3f978-2613">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3f978-2614">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3f978-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="3f978-2616">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3f978-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3f978-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3f978-2618">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="3f978-2620">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3f978-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3f978-2621">Az.Monitor</span></span>
- <span data-ttu-id="3f978-2622">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3f978-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f978-2623">Az.KeyVault</span></span>
- <span data-ttu-id="3f978-2624">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3f978-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3f978-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="3f978-2626">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="3f978-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3f978-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3f978-2627">Az.Media</span></span>
- <span data-ttu-id="3f978-2628">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="3f978-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3f978-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2629">Az.Network</span></span>
<span data-ttu-id="3f978-2630">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3f978-2631">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="3f978-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3f978-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3f978-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3f978-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f978-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3f978-2640">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3f978-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f978-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3f978-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3f978-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3f978-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3f978-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3f978-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3f978-2646">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3f978-2647">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3f978-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3f978-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f978-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3f978-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f978-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3f978-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f978-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3f978-2651">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3f978-2652">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3f978-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="3f978-2654">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3f978-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3f978-2655">Az.Profile</span></span>
- <span data-ttu-id="3f978-2656">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="3f978-2658">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3f978-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2659">Az.Resources</span></span>
- <span data-ttu-id="3f978-2660">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3f978-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="3f978-2662">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="3f978-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3f978-2663">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3f978-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3f978-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="3f978-2665">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3f978-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3f978-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2666">Az.Sql</span></span>
- <span data-ttu-id="3f978-2667">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3f978-2668">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3f978-2669">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3f978-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2670">Az.Storage</span></span>
- <span data-ttu-id="3f978-2671">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3f978-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2672">Az.Websites</span></span>
- <span data-ttu-id="3f978-2673">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="3f978-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3f978-2674">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3f978-2675">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-2675">General</span></span>

* <span data-ttu-id="3f978-2676">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="3f978-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3f978-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2677">Az.Compute</span></span>

* <span data-ttu-id="3f978-2678">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="3f978-2680">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3f978-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3f978-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="3f978-2682">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="3f978-2683">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3f978-2684">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3f978-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="3f978-2686">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3f978-2687">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="3f978-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3f978-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2688">Az.Resources</span></span>

* <span data-ttu-id="3f978-2689">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="3f978-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3f978-2690">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3f978-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3f978-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2691">Az.Sql</span></span>

* <span data-ttu-id="3f978-2692">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="3f978-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3f978-2693">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3f978-2694">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3f978-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2695">Az.Storage</span></span>

* <span data-ttu-id="3f978-2696">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3f978-2697">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3f978-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3f978-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3f978-2699">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="3f978-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3f978-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3f978-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3f978-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3f978-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2702">Az.Websites</span></span>

* <span data-ttu-id="3f978-2703">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3f978-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="3f978-2704">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3f978-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3f978-2705">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="3f978-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3f978-2706">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3f978-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f978-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="3f978-2708">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3f978-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3f978-2709">Az.Automation</span></span>
* <span data-ttu-id="3f978-2710">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3f978-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3f978-2711">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3f978-2712">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3f978-2713">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3f978-2714">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3f978-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2715">Az.Compute</span></span>
* <span data-ttu-id="3f978-2716">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3f978-2717">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3f978-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="3f978-2719">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3f978-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3f978-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3f978-2721">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3f978-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2722">Az.Network</span></span>
* <span data-ttu-id="3f978-2723">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3f978-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3f978-2724">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3f978-2725">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="3f978-2726">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3f978-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3f978-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3f978-2728">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3f978-2729">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="3f978-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3f978-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3f978-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3f978-2731">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="3f978-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3f978-2732">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3f978-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3f978-2733">Az.Relay</span></span>
* <span data-ttu-id="3f978-2734">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="3f978-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3f978-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2735">Az.Resources</span></span>
* <span data-ttu-id="3f978-2736">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3f978-2737">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="3f978-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3f978-2738">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="3f978-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3f978-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-2740">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3f978-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2741">Az.Sql</span></span>
* <span data-ttu-id="3f978-2742">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3f978-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3f978-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3f978-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3f978-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3f978-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3f978-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3f978-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3f978-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3f978-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3f978-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3f978-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3f978-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3f978-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3f978-2751">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="3f978-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3f978-2752">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3f978-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3f978-2753">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f978-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3f978-2754">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="3f978-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3f978-2755">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="3f978-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3f978-2756">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3f978-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3f978-2757">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="3f978-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3f978-2758">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3f978-2759">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3f978-2760">Allgemein</span><span class="sxs-lookup"><span data-stu-id="3f978-2760">General</span></span>
* <span data-ttu-id="3f978-2761">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="3f978-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3f978-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3f978-2762">Az.Profile</span></span>
* <span data-ttu-id="3f978-2763">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3f978-2764">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3f978-2765">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3f978-2766">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3f978-2767">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3f978-2768">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3f978-2769">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="3f978-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-2771">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2772">Az.Compute</span></span>
* <span data-ttu-id="3f978-2773">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3f978-2774">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="3f978-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3f978-2775">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="3f978-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2777">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="3f978-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3f978-2778">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3f978-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3f978-2779">Az.Insights</span></span>
* <span data-ttu-id="3f978-2780">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="3f978-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3f978-2781">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="3f978-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3f978-2782">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="3f978-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3f978-2783">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2784">Az.Network</span></span>
* <span data-ttu-id="3f978-2785">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3f978-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3f978-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3f978-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3f978-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3f978-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3f978-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3f978-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3f978-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3f978-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3f978-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3f978-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3f978-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3f978-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3f978-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="3f978-2793">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2794">Az.Resources</span></span>
* <span data-ttu-id="3f978-2795">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="3f978-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3f978-2796">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="3f978-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3f978-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3f978-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="3f978-2798">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="3f978-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3f978-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3f978-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="3f978-2800">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3f978-2801">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="3f978-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3f978-2802">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="3f978-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3f978-2803">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="3f978-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3f978-2804">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3f978-2805">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3f978-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3f978-2806">Az.Profile</span></span>
* <span data-ttu-id="3f978-2807">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3f978-2808">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2809">Az.Compute</span></span>
* <span data-ttu-id="3f978-2810">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="3f978-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3f978-2811">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3f978-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3f978-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="3f978-2813">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3f978-2814">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3f978-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3f978-2815">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f978-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3f978-2816">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="3f978-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3f978-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3f978-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2818">Az.Network</span></span>
* <span data-ttu-id="3f978-2819">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="3f978-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3f978-2820">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2821">Az.Resources</span></span>
* <span data-ttu-id="3f978-2822">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f978-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3f978-2823">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3f978-2824">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3f978-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3f978-2825">Azure.Storage</span></span>
* <span data-ttu-id="3f978-2826">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="3f978-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3f978-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3f978-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3f978-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3f978-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3f978-2829">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="3f978-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3f978-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3f978-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3f978-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3f978-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="3f978-2832">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3f978-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3f978-2833">Az.Compute</span></span>
* <span data-ttu-id="3f978-2834">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="3f978-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3f978-2835">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3f978-2836">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="3f978-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3f978-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3f978-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3f978-2838">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3f978-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3f978-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3f978-2839">Az.Network</span></span>
* <span data-ttu-id="3f978-2840">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f978-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3f978-2841">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2841">new cmdlets added</span></span>
    - <span data-ttu-id="3f978-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3f978-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3f978-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3f978-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3f978-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3f978-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3f978-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3f978-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3f978-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3f978-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3f978-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3f978-2848">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3f978-2849">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3f978-2850">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3f978-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3f978-2851">Az.RedisCache</span></span>
* <span data-ttu-id="3f978-2852">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="3f978-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3f978-2853">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3f978-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3f978-2854">Az.Resources</span></span>
* <span data-ttu-id="3f978-2855">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="3f978-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3f978-2856">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="3f978-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3f978-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3f978-2857">Az.Sql</span></span>
* <span data-ttu-id="3f978-2858">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="3f978-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3f978-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3f978-2859">Az.Websites</span></span>
* <span data-ttu-id="3f978-2860">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="3f978-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3f978-2861">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="3f978-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3f978-2862">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="3f978-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3f978-2863">Erstrelease</span><span class="sxs-lookup"><span data-stu-id="3f978-2863">Initial Release</span></span>
