---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182552"
---
## <a name="320---december-2019"></a><span data-ttu-id="abf1d-103">3.2.0: Dezember 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="abf1d-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-104">General</span></span>
* <span data-ttu-id="abf1d-105">Verweise in „.psd1“ zur Verwendung des relativen Pfads für alle Module aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-106">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-107">Richtiges UserAgent-Element für clientseitige Telemetrie für Az 4.0-Vorschauversion festgelegt</span><span class="sxs-lookup"><span data-stu-id="abf1d-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="abf1d-108">Anzeigen benutzerfreundlicher Fehlermeldungen, wenn der Kontext in der Az 4.0-Vorschauversion NULL ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="abf1d-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-109">Az.Batch</span></span>
* <span data-ttu-id="abf1d-110">Problem [#10602](https://github.com/Azure/azure-powershell/issues/10602) behoben, aufgrund dessen „VirtualMachineConfiguration.ContainerConfiguration“ oder „VirtualMachineConfiguration.DataDisks“ von **New-AzBatchPool** nicht ordnungsgemäß an den Server gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-111">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-112">Version des ADF .NET SDK auf 4.5.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-113">Az.FrontDoor</span></span>
* <span data-ttu-id="abf1d-114">Unterstützung für den Ausschluss verwalteter WAF-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="abf1d-115">SocketAddr zur automatischen Vervollständigung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="abf1d-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="abf1d-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="abf1d-117">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="abf1d-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-118">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-119">Fehler im Zusammenhang mit dem Zugriff auf einen möglicherweise nicht festgelegten Wert behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="abf1d-120">Zertifikatverwaltung für Kryptografie für elliptische Kurve</span><span class="sxs-lookup"><span data-stu-id="abf1d-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="abf1d-121">Unterstützung zum Angeben der Kurve für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-122">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-123">Optionales Argument zum Befehl „Diagnoseeinstellungen hinzufügen“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="abf1d-124">Ein Optionsargument, das angibt, dass der Export in Log Analytics ein festes Schema sein muss (auch bekannt als</span><span class="sxs-lookup"><span data-stu-id="abf1d-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="abf1d-125">dedizierter Datentyp)</span><span class="sxs-lookup"><span data-stu-id="abf1d-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-126">Az.Network</span></span>
* <span data-ttu-id="abf1d-127">Unterstützung für IpGroups in der AzureFirewall-Anwendung sowie in NAT- und Netzwerkregeln</span><span class="sxs-lookup"><span data-stu-id="abf1d-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-128">Az.Resources</span></span>
* <span data-ttu-id="abf1d-129">Problem behoben, aufgrund dessen die Vorlagenbereitstellung einen Vorlagenparameter nicht lesen kann, wenn der Name einen Konflikt mit einem integrierten Parameternamen verursacht</span><span class="sxs-lookup"><span data-stu-id="abf1d-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="abf1d-130">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-09-01 aktualisiert, die Gruppierungsunterstützung in Richtliniensatzdefinitionen einführt</span><span class="sxs-lookup"><span data-stu-id="abf1d-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-131">Az.Sql</span></span>
* <span data-ttu-id="abf1d-132">Speichererstellung in automatischer Aktivierung der Sicherheitsrisikobewertung auf StorageV2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-133">Az.Storage</span></span>
* <span data-ttu-id="abf1d-134">Unterstützung der Generierung blob-/containeridentitätsbasierter SAS-Token mit Speicherkontext auf der Grundlage der OAuth-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="abf1d-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="abf1d-135">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="abf1d-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="abf1d-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="abf1d-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="abf1d-137">Unterstützung für das Widerrufen von Schlüsseln für die Speicherkonto-Benutzerdelegierung hinzugefügt, sodass alle SAS-Identitätstoken widerrufen werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="abf1d-138">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="abf1d-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="abf1d-139">Upgrade auf Microsoft.Azure.Management.Storage 14.2.0, um die neue API-Version 2019-06-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="abf1d-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="abf1d-140">Unterstützung des QuotaGiB-Freigabeelements von mindestens 5120 in Dateifreigabe-Cmdlet der Verwaltungsebene und Parameteralias „Quota“ zum Parameter „QuotaGiB“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="abf1d-141">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="abf1d-142">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="abf1d-143">Parameteralias „QuotaGiB“ zum Parameter „Quota“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="abf1d-144">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="abf1d-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="abf1d-145">Problem behoben, dass „Set-AzStorageContainerAcl“ die gespeicherte Zugriffsrichtlinie bereinigen kann</span><span class="sxs-lookup"><span data-stu-id="abf1d-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="abf1d-146">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="abf1d-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="abf1d-147">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abf1d-148">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="abf1d-148">Highlights since the last major release</span></span>
* <span data-ttu-id="abf1d-149">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="abf1d-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="abf1d-150">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="abf1d-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-151">Az.Compute</span></span>
* <span data-ttu-id="abf1d-152">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="abf1d-152">VM Reapply feature</span></span>
    - <span data-ttu-id="abf1d-153">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="abf1d-154">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="abf1d-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="abf1d-155">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="abf1d-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="abf1d-156">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="abf1d-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="abf1d-157">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="abf1d-158">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="abf1d-159">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="abf1d-160">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="abf1d-161">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="abf1d-162">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="abf1d-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="abf1d-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="abf1d-164">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="abf1d-165">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="abf1d-165">Get the Order</span></span>
* <span data-ttu-id="abf1d-166">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="abf1d-167">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="abf1d-167">Create new Order</span></span>
* <span data-ttu-id="abf1d-168">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="abf1d-169">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="abf1d-169">Remove the Order</span></span>
* <span data-ttu-id="abf1d-170">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="abf1d-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="abf1d-171">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="abf1d-171">Now creates Local Share</span></span>
* <span data-ttu-id="abf1d-172">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="abf1d-173">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="abf1d-174">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="abf1d-175">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="abf1d-176">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="abf1d-177">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="abf1d-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="abf1d-178">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="abf1d-179">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="abf1d-179">Create new Triggers</span></span>
* <span data-ttu-id="abf1d-180">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="abf1d-181">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="abf1d-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-182">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-183">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="abf1d-184">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-186">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-187">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-188">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-189">Az.FrontDoor</span></span>
* <span data-ttu-id="abf1d-190">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="abf1d-191">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="abf1d-192">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="abf1d-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="abf1d-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-194">Az.Network</span></span>
* <span data-ttu-id="abf1d-195">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="abf1d-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="abf1d-196">Az.PrivateDns</span></span>
* <span data-ttu-id="abf1d-197">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-199">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="abf1d-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="abf1d-200">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="abf1d-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="abf1d-201">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="abf1d-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abf1d-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abf1d-202">Az.RedisCache</span></span>
* <span data-ttu-id="abf1d-203">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="abf1d-204">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="abf1d-205">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-206">Az.Resources</span></span>
- <span data-ttu-id="abf1d-207">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="abf1d-208">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="abf1d-209">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="abf1d-210">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="abf1d-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="abf1d-211">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-212">Az.Sql</span></span>
* <span data-ttu-id="abf1d-213">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="abf1d-214">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="abf1d-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="abf1d-215">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="abf1d-216">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-216">General</span></span>
* <span data-ttu-id="abf1d-217">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="abf1d-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-218">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-219">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="abf1d-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="abf1d-220">Az.Advisor</span></span>
* <span data-ttu-id="abf1d-221">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="abf1d-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-222">Az.Batch</span></span>
* <span data-ttu-id="abf1d-223">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="abf1d-224">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="abf1d-225">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="abf1d-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="abf1d-226">Für den Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="abf1d-227">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="abf1d-228">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="abf1d-229">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="abf1d-230">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="abf1d-231">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="abf1d-232">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="abf1d-233">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="abf1d-234">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="abf1d-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="abf1d-235">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="abf1d-236">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="abf1d-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="abf1d-237">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="abf1d-238">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="abf1d-239">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="abf1d-240">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="abf1d-241">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="abf1d-242">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="abf1d-243">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="abf1d-244">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="abf1d-245">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="abf1d-246">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="abf1d-247">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="abf1d-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="abf1d-248">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abf1d-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="abf1d-249">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="abf1d-250">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="abf1d-251">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="abf1d-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="abf1d-252">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="abf1d-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="abf1d-253">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="abf1d-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="abf1d-254">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="abf1d-255">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="abf1d-256">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="abf1d-257">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="abf1d-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="abf1d-258">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="abf1d-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abf1d-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-259">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-260">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="abf1d-261">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-262">Az.Compute</span></span>
* <span data-ttu-id="abf1d-263">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="abf1d-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="abf1d-264">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="abf1d-265">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="abf1d-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="abf1d-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="abf1d-267">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="abf1d-268">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="abf1d-269">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="abf1d-270">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="abf1d-271">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="abf1d-271">Breaking changes</span></span>
    - <span data-ttu-id="abf1d-272">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="abf1d-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="abf1d-273">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-274">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-275">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-277">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="abf1d-278">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="abf1d-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="abf1d-279">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="abf1d-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="abf1d-280">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="abf1d-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="abf1d-281">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="abf1d-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="abf1d-282">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="abf1d-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-283">Az.FrontDoor</span></span>
* <span data-ttu-id="abf1d-284">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="abf1d-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="abf1d-285">Az.HDInsight</span></span>
* <span data-ttu-id="abf1d-286">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="abf1d-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="abf1d-287">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="abf1d-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="abf1d-288">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="abf1d-289">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="abf1d-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="abf1d-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="abf1d-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="abf1d-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="abf1d-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="abf1d-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="abf1d-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="abf1d-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="abf1d-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="abf1d-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="abf1d-295">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="abf1d-296">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="abf1d-297">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="abf1d-298">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="abf1d-299">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="abf1d-300">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="abf1d-301">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="abf1d-302">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="abf1d-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="abf1d-303">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="abf1d-304">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="abf1d-305">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="abf1d-306">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="abf1d-307">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-308">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-309">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="abf1d-309">Breaking changes:</span></span>
    - <span data-ttu-id="abf1d-310">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="abf1d-311">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="abf1d-312">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="abf1d-313">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="abf1d-314">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="abf1d-315">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="abf1d-316">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="abf1d-317">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="abf1d-318">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="abf1d-319">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="abf1d-320">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="abf1d-321">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-323">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-324">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="abf1d-325">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="abf1d-326">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-327">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-328">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-329">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-330">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-331">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-332">Az.Resources</span></span>
* <span data-ttu-id="abf1d-333">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-334">Az.Network</span></span>
* <span data-ttu-id="abf1d-335">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="abf1d-336">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="abf1d-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="abf1d-337">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-338">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-339">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-340">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="abf1d-342">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="abf1d-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="abf1d-343">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="abf1d-343">New cmdlet:</span></span>
        - <span data-ttu-id="abf1d-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="abf1d-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="abf1d-345">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="abf1d-346">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="abf1d-347">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="abf1d-348">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="abf1d-349">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="abf1d-350">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="abf1d-351">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="abf1d-352">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-352">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="abf1d-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="abf1d-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="abf1d-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="abf1d-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="abf1d-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="abf1d-358">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="abf1d-359">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="abf1d-360">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="abf1d-361">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="abf1d-362">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="abf1d-363">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="abf1d-364">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="abf1d-365">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-365">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="abf1d-367">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="abf1d-368">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="abf1d-369">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="abf1d-370">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="abf1d-371">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="abf1d-372">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="abf1d-373">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="abf1d-374">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-374">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="abf1d-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="abf1d-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="abf1d-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="abf1d-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="abf1d-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="abf1d-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="abf1d-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="abf1d-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="abf1d-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="abf1d-381">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="abf1d-382">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="abf1d-383">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="abf1d-384">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="abf1d-385">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="abf1d-386">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="abf1d-387">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="abf1d-388">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="abf1d-389">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="abf1d-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="abf1d-390">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="abf1d-391">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="abf1d-392">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-392">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="abf1d-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="abf1d-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="abf1d-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-398">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="abf1d-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-399">Az.Sql</span></span>
* <span data-ttu-id="abf1d-400">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="abf1d-401">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="abf1d-402">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="abf1d-403">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="abf1d-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="abf1d-404">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="abf1d-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="abf1d-405">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="abf1d-406">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="abf1d-407">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="abf1d-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="abf1d-408">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-409">Az.Storage</span></span>
* <span data-ttu-id="abf1d-410">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="abf1d-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="abf1d-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="abf1d-413">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="abf1d-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="abf1d-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="abf1d-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="abf1d-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="abf1d-416">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="abf1d-417">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-417">General</span></span>
* <span data-ttu-id="abf1d-418">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="abf1d-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-419">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-420">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="abf1d-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-421">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-422">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="abf1d-423">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="abf1d-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-424">Az.Automation</span></span>
* <span data-ttu-id="abf1d-425">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="abf1d-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-426">Az.Batch</span></span>
* <span data-ttu-id="abf1d-427">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-428">Az.Compute</span></span>
* <span data-ttu-id="abf1d-429">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="abf1d-430">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="abf1d-431">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="abf1d-432">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="abf1d-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-433">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-434">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="abf1d-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="abf1d-435">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="abf1d-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="abf1d-436">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-438">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="abf1d-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="abf1d-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="abf1d-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="abf1d-440">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="abf1d-441">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="abf1d-442">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="abf1d-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="abf1d-443">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-444">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-445">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="abf1d-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="abf1d-446">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="abf1d-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-447">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-448">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="abf1d-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="abf1d-449">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="abf1d-450">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="abf1d-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="abf1d-451">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="abf1d-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-452">Az.Network</span></span>
* <span data-ttu-id="abf1d-453">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="abf1d-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="abf1d-454">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="abf1d-455">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-455">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-456">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="abf1d-457">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="abf1d-458">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="abf1d-459">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="abf1d-460">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="abf1d-461">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="abf1d-462">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="abf1d-463">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="abf1d-464">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="abf1d-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="abf1d-465">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="abf1d-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="abf1d-466">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="abf1d-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abf1d-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abf1d-467">Az.RedisCache</span></span>
* <span data-ttu-id="abf1d-468">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="abf1d-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-469">Az.Sql</span></span>
* <span data-ttu-id="abf1d-470">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-471">Az.Storage</span></span>
* <span data-ttu-id="abf1d-472">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="abf1d-473">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="abf1d-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="abf1d-474">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="abf1d-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="abf1d-475">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="abf1d-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="abf1d-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="abf1d-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="abf1d-477">Az.StorageSync</span></span>
* <span data-ttu-id="abf1d-478">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-479">Az.Websites</span></span>
* <span data-ttu-id="abf1d-480">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="abf1d-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="abf1d-481">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="abf1d-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-482">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-483">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="abf1d-484">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="abf1d-485">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-486">Az.Automation</span></span>
* <span data-ttu-id="abf1d-487">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="abf1d-488">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="abf1d-489">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-490">Az.Compute</span></span>
* <span data-ttu-id="abf1d-491">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="abf1d-492">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="abf1d-493">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="abf1d-494">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="abf1d-495">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="abf1d-496">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="abf1d-497">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="abf1d-498">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="abf1d-499">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-500">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-501">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="abf1d-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="abf1d-502">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="abf1d-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="abf1d-503">Az.HDInsight</span></span>
* <span data-ttu-id="abf1d-504">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-505">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-506">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="abf1d-507">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="abf1d-508">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="abf1d-508">New cmdlets are:</span></span>
    - <span data-ttu-id="abf1d-509">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="abf1d-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="abf1d-510">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="abf1d-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="abf1d-511">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="abf1d-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="abf1d-512">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="abf1d-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-513">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-514">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="abf1d-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="abf1d-515">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="abf1d-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="abf1d-516">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="abf1d-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="abf1d-517">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="abf1d-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="abf1d-518">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="abf1d-519">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="abf1d-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="abf1d-520">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="abf1d-521">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="abf1d-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="abf1d-522">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="abf1d-523">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="abf1d-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="abf1d-524">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="abf1d-525">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="abf1d-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="abf1d-526">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="abf1d-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="abf1d-527">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="abf1d-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="abf1d-528">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="abf1d-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="abf1d-529">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="abf1d-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="abf1d-530">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="abf1d-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="abf1d-531">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="abf1d-532">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="abf1d-533">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="abf1d-533">Overall improved help files</span></span>
* <span data-ttu-id="abf1d-534">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-535">Az.Network</span></span>
* <span data-ttu-id="abf1d-536">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="abf1d-537">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="abf1d-538">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="abf1d-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="abf1d-539">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="abf1d-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="abf1d-540">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="abf1d-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="abf1d-541">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="abf1d-542">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="abf1d-543">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="abf1d-544">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="abf1d-545">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="abf1d-546">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="abf1d-547">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="abf1d-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="abf1d-548">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-548">New cmdlets</span></span>
        - <span data-ttu-id="abf1d-549">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="abf1d-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="abf1d-550">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="abf1d-551">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="abf1d-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="abf1d-552">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="abf1d-552">New-VpnSite</span></span>
        - <span data-ttu-id="abf1d-553">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="abf1d-553">Update-VpnSite</span></span>
        - <span data-ttu-id="abf1d-554">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-554">New-VpnConnection</span></span>
        - <span data-ttu-id="abf1d-555">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-555">Update-VpnConnection</span></span>
* <span data-ttu-id="abf1d-556">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-558">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="abf1d-559">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-560">Az.Resources</span></span>
* <span data-ttu-id="abf1d-561">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="abf1d-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-563">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="abf1d-564">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="abf1d-565">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="abf1d-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="abf1d-566">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="abf1d-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="abf1d-567">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="abf1d-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="abf1d-568">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="abf1d-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="abf1d-569">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="abf1d-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="abf1d-570">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="abf1d-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="abf1d-571">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="abf1d-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="abf1d-572">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="abf1d-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="abf1d-573">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="abf1d-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="abf1d-574">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="abf1d-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="abf1d-575">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="abf1d-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="abf1d-576">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="abf1d-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="abf1d-577">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="abf1d-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="abf1d-578">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="abf1d-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="abf1d-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="abf1d-579">Az.SignalR</span></span>
* <span data-ttu-id="abf1d-580">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-581">Az.Sql</span></span>
* <span data-ttu-id="abf1d-582">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="abf1d-583">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="abf1d-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="abf1d-584">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="abf1d-585">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="abf1d-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="abf1d-586">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="abf1d-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-587">Az.Storage</span></span>
* <span data-ttu-id="abf1d-588">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="abf1d-589">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="abf1d-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="abf1d-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="abf1d-592">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="abf1d-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="abf1d-594">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="abf1d-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="abf1d-595">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="abf1d-596">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="abf1d-597">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="abf1d-598">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="abf1d-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-599">Az.Websites</span></span>
* <span data-ttu-id="abf1d-600">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="abf1d-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="abf1d-601">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="abf1d-602">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="abf1d-603">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="abf1d-604">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-604">General</span></span>
* <span data-ttu-id="abf1d-605">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-606">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-607">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="abf1d-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="abf1d-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="abf1d-608">Az.Aks</span></span>
* <span data-ttu-id="abf1d-609">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="abf1d-610">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="abf1d-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="abf1d-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-611">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-612">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="abf1d-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="abf1d-613">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="abf1d-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="abf1d-614">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="abf1d-615">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="abf1d-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="abf1d-616">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="abf1d-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="abf1d-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-617">Az.Batch</span></span>
* <span data-ttu-id="abf1d-618">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="abf1d-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abf1d-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-619">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-620">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-621">Az.Compute</span></span>
* <span data-ttu-id="abf1d-622">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="abf1d-623">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="abf1d-624">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="abf1d-625">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="abf1d-626">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="abf1d-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="abf1d-627">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="abf1d-628">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="abf1d-629">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-630">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-631">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="abf1d-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="abf1d-632">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="abf1d-633">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="abf1d-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="abf1d-634">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-636">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-637">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-638">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="abf1d-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="abf1d-639">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="abf1d-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="abf1d-640">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="abf1d-641">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="abf1d-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="abf1d-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="abf1d-643">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-644">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-645">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-646">Az.Network</span></span>
* <span data-ttu-id="abf1d-647">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="abf1d-648">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="abf1d-649">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="abf1d-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="abf1d-650">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="abf1d-651">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="abf1d-652">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="abf1d-653">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="abf1d-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-655">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="abf1d-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="abf1d-656">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-656">Added example</span></span>
    - <span data-ttu-id="abf1d-657">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="abf1d-658">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="abf1d-659">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-661">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-662">Az.Resources</span></span>
* <span data-ttu-id="abf1d-663">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="abf1d-664">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="abf1d-665">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="abf1d-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="abf1d-666">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-667">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-668">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="abf1d-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="abf1d-669">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="abf1d-670">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-672">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="abf1d-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="abf1d-673">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="abf1d-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="abf1d-674">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="abf1d-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="abf1d-675">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="abf1d-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="abf1d-676">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="abf1d-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="abf1d-677">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="abf1d-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-678">Az.Sql</span></span>
* <span data-ttu-id="abf1d-679">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-680">Az.Storage</span></span>
* <span data-ttu-id="abf1d-681">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="abf1d-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="abf1d-682">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="abf1d-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="abf1d-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="abf1d-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="abf1d-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="abf1d-685">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="abf1d-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="abf1d-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="abf1d-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-687">Az.Websites</span></span>
* <span data-ttu-id="abf1d-688">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="abf1d-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="abf1d-689">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-690">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-691">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="abf1d-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="abf1d-693">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="abf1d-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-694">Az.Automation</span></span>
* <span data-ttu-id="abf1d-695">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-697">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-698">Az.Compute</span></span>
* <span data-ttu-id="abf1d-699">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="abf1d-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="abf1d-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="abf1d-701">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="abf1d-702">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="abf1d-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-703">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-704">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="abf1d-705">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-706">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-707">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="abf1d-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="abf1d-708">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-709">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-710">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abf1d-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abf1d-711">Az.LogicApp</span></span>
* <span data-ttu-id="abf1d-712">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="abf1d-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="abf1d-713">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="abf1d-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-714">Az.ManagedServices</span></span>
* <span data-ttu-id="abf1d-715">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-716">Az.Network</span></span>
* <span data-ttu-id="abf1d-717">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="abf1d-718">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-718">New cmdlets</span></span>
        - <span data-ttu-id="abf1d-719">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="abf1d-720">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abf1d-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="abf1d-721">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-722">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-723">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-724">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="abf1d-725">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="abf1d-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="abf1d-726">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abf1d-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="abf1d-727">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="abf1d-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="abf1d-728">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="abf1d-729">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="abf1d-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="abf1d-730">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="abf1d-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="abf1d-731">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="abf1d-732">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="abf1d-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="abf1d-733">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-733">Updated cmdlets</span></span>
        - <span data-ttu-id="abf1d-734">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="abf1d-735">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="abf1d-736">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="abf1d-737">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="abf1d-738">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="abf1d-739">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="abf1d-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="abf1d-740">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="abf1d-741">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="abf1d-742">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="abf1d-743">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="abf1d-744">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="abf1d-745">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="abf1d-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-747">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="abf1d-748">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-750">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="abf1d-751">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="abf1d-752">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="abf1d-753">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="abf1d-754">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="abf1d-755">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="abf1d-756">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="abf1d-757">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="abf1d-758">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="abf1d-759">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-760">Az.Resources</span></span>
- <span data-ttu-id="abf1d-761">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="abf1d-762">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-763">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-764">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="abf1d-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="abf1d-765">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-766">Az.Sql</span></span>
* <span data-ttu-id="abf1d-767">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="abf1d-768">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="abf1d-769">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-770">Az.Storage</span></span>
* <span data-ttu-id="abf1d-771">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="abf1d-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="abf1d-772">Az.StorageSync</span></span>
* <span data-ttu-id="abf1d-773">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="abf1d-774">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-775">Az.Websites</span></span>
* <span data-ttu-id="abf1d-776">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="abf1d-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="abf1d-777">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="abf1d-778">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="abf1d-779">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-780">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-781">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="abf1d-782">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="abf1d-783">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="abf1d-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="abf1d-784">Az.Advisor</span></span>
* <span data-ttu-id="abf1d-785">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="abf1d-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="abf1d-786">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="abf1d-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-787">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-788">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="abf1d-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="abf1d-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="abf1d-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="abf1d-790">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="abf1d-791">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="abf1d-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="abf1d-792">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="abf1d-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="abf1d-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="abf1d-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="abf1d-794">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-795">Az.Automation</span></span>
* <span data-ttu-id="abf1d-796">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-797">Az.Compute</span></span>
* <span data-ttu-id="abf1d-798">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-799">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-800">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="abf1d-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abf1d-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abf1d-801">Az.EventGrid</span></span>
* <span data-ttu-id="abf1d-802">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-803">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-804">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-805">Az.Network</span></span>
* <span data-ttu-id="abf1d-806">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="abf1d-807">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="abf1d-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abf1d-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="abf1d-809">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="abf1d-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="abf1d-810">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="abf1d-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-812">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-814">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="abf1d-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-815">Az.Resources</span></span>
    - <span data-ttu-id="abf1d-816">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="abf1d-817">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="abf1d-818">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="abf1d-819">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-820">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-821">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="abf1d-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-822">Az.Sql</span></span>
* <span data-ttu-id="abf1d-823">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="abf1d-824">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="abf1d-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="abf1d-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="abf1d-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="abf1d-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="abf1d-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="abf1d-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="abf1d-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="abf1d-831">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-832">Az.Storage</span></span>
* <span data-ttu-id="abf1d-833">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="abf1d-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="abf1d-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abf1d-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="abf1d-835">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="abf1d-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="abf1d-836">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="abf1d-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="abf1d-837">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="abf1d-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="abf1d-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="abf1d-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="abf1d-840">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="abf1d-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="abf1d-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="abf1d-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="abf1d-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="abf1d-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="abf1d-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="abf1d-843">Az.StorageSync</span></span>
* <span data-ttu-id="abf1d-844">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="abf1d-845">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-846">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-847">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="abf1d-848">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="abf1d-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="abf1d-849">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="abf1d-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="abf1d-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="abf1d-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="abf1d-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-852">Az.Compute</span></span>
* <span data-ttu-id="abf1d-853">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="abf1d-854">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="abf1d-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="abf1d-855">Az.Dns</span></span>
* <span data-ttu-id="abf1d-856">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abf1d-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abf1d-857">Az.EventGrid</span></span>
* <span data-ttu-id="abf1d-858">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="abf1d-859">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-859">New cmdlets:</span></span>
    - <span data-ttu-id="abf1d-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="abf1d-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="abf1d-861">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="abf1d-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="abf1d-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="abf1d-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="abf1d-863">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abf1d-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="abf1d-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="abf1d-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="abf1d-865">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="abf1d-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="abf1d-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="abf1d-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="abf1d-867">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="abf1d-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="abf1d-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="abf1d-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="abf1d-869">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="abf1d-870">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="abf1d-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="abf1d-871">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="abf1d-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="abf1d-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="abf1d-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="abf1d-873">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="abf1d-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="abf1d-874">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="abf1d-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="abf1d-875">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="abf1d-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="abf1d-876">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="abf1d-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="abf1d-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="abf1d-878">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="abf1d-879">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="abf1d-880">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="abf1d-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="abf1d-881">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="abf1d-882">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="abf1d-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="abf1d-883">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="abf1d-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="abf1d-884">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="abf1d-885">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="abf1d-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="abf1d-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="abf1d-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="abf1d-887">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="abf1d-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="abf1d-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="abf1d-889">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="abf1d-890">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="abf1d-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-891">Az.FrontDoor</span></span>
* <span data-ttu-id="abf1d-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="abf1d-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="abf1d-893">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="abf1d-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="abf1d-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="abf1d-895">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-896">Az.Network</span></span>
* <span data-ttu-id="abf1d-897">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="abf1d-898">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-898">New cmdlets</span></span>
        - <span data-ttu-id="abf1d-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="abf1d-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="abf1d-900">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="abf1d-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="abf1d-901">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-901">New cmdlets</span></span> 
        - <span data-ttu-id="abf1d-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="abf1d-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="abf1d-903">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="abf1d-904">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-904">New cmdlets</span></span> 
        - <span data-ttu-id="abf1d-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abf1d-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="abf1d-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abf1d-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="abf1d-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="abf1d-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="abf1d-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="abf1d-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="abf1d-910">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="abf1d-911">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-911">New cmdlets</span></span>
        - <span data-ttu-id="abf1d-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="abf1d-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="abf1d-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="abf1d-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="abf1d-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="abf1d-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="abf1d-916">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="abf1d-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="abf1d-917">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="abf1d-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="abf1d-918">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="abf1d-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="abf1d-919">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="abf1d-920">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="abf1d-921">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="abf1d-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="abf1d-922">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="abf1d-923">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="abf1d-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="abf1d-924">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="abf1d-925">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="abf1d-926">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="abf1d-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="abf1d-927">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="abf1d-928">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="abf1d-929">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="abf1d-930">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="abf1d-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="abf1d-931">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="abf1d-932">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="abf1d-933">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="abf1d-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="abf1d-934">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="abf1d-935">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="abf1d-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="abf1d-936">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="abf1d-937">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="abf1d-938">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-940">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-941">Az.Resources</span></span>
* <span data-ttu-id="abf1d-942">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="abf1d-943">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="abf1d-944">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="abf1d-945">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="abf1d-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-947">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="abf1d-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-948">Az.Sql</span></span>
* <span data-ttu-id="abf1d-949">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="abf1d-950">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="abf1d-951">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="abf1d-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="abf1d-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="abf1d-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="abf1d-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="abf1d-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="abf1d-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="abf1d-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="abf1d-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="abf1d-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="abf1d-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-957">Az.Storage</span></span>
* <span data-ttu-id="abf1d-958">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="abf1d-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="abf1d-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="abf1d-960">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="abf1d-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="abf1d-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-962">Az.Websites</span></span>
* <span data-ttu-id="abf1d-963">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="abf1d-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="abf1d-964">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="abf1d-965">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="abf1d-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-966">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-967">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-968">Az.Compute</span></span>
* <span data-ttu-id="abf1d-969">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="abf1d-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="abf1d-970">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="abf1d-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-971">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-972">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="abf1d-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="abf1d-973">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="abf1d-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-974">Az.Network</span></span>
* <span data-ttu-id="abf1d-975">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="abf1d-976">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abf1d-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="abf1d-978">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="abf1d-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-980">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-981">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-982">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="abf1d-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-984">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="abf1d-985">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-986">Az.Sql</span></span>
* <span data-ttu-id="abf1d-987">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="abf1d-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="abf1d-988">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="abf1d-989">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="abf1d-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="abf1d-990">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="abf1d-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-991">Az.Websites</span></span>
* <span data-ttu-id="abf1d-992">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="abf1d-993">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="abf1d-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-994">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-995">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="abf1d-996">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="abf1d-997">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="abf1d-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="abf1d-998">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="abf1d-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="abf1d-999">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="abf1d-1000">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="abf1d-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="abf1d-1001">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="abf1d-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="abf1d-1002">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="abf1d-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="abf1d-1003">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="abf1d-1004">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="abf1d-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="abf1d-1005">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="abf1d-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="abf1d-1006">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="abf1d-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="abf1d-1007">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="abf1d-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="abf1d-1008">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="abf1d-1009">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="abf1d-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="abf1d-1010">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="abf1d-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="abf1d-1011">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="abf1d-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="abf1d-1012">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="abf1d-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="abf1d-1013">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="abf1d-1014">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="abf1d-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="abf1d-1015">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="abf1d-1016">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="abf1d-1017">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="abf1d-1018">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="abf1d-1019">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="abf1d-1020">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="abf1d-1021">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="abf1d-1022">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="abf1d-1023">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="abf1d-1024">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="abf1d-1025">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="abf1d-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="abf1d-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="abf1d-1027">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="abf1d-1028">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="abf1d-1029">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="abf1d-1030">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="abf1d-1031">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="abf1d-1032">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="abf1d-1033">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="abf1d-1034">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="abf1d-1035">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="abf1d-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="abf1d-1036">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="abf1d-1037">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="abf1d-1038">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="abf1d-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="abf1d-1039">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="abf1d-1040">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="abf1d-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="abf1d-1041">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="abf1d-1042">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="abf1d-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="abf1d-1043">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="abf1d-1044">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="abf1d-1045">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="abf1d-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="abf1d-1046">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="abf1d-1047">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="abf1d-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="abf1d-1048">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="abf1d-1049">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="abf1d-1050">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="abf1d-1051">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="abf1d-1052">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="abf1d-1053">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="abf1d-1054">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="abf1d-1055">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="abf1d-1056">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="abf1d-1057">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="abf1d-1058">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="abf1d-1059">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="abf1d-1060">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="abf1d-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="abf1d-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="abf1d-1062">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="abf1d-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="abf1d-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="abf1d-1064">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="abf1d-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="abf1d-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="abf1d-1066">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="abf1d-1067">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="abf1d-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="abf1d-1069">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="abf1d-1070">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="abf1d-1071">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="abf1d-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1072">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1073">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="abf1d-1074">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="abf1d-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="abf1d-1075">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="abf1d-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="abf1d-1076">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="abf1d-1077">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="abf1d-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="abf1d-1078">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="abf1d-1079">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1080">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1081">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="abf1d-1082">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1084">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1085">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-1086">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1087">Az.Network</span></span>
* <span data-ttu-id="abf1d-1088">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="abf1d-1089">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="abf1d-1090">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="abf1d-1091">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="abf1d-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1092">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1093">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1094">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1095">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="abf1d-1096">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1097">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1098">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-1100">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="abf1d-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="abf1d-1101">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="abf1d-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1102">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1103">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="abf1d-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="abf1d-1104">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="abf1d-1105">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="abf1d-1106">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="abf1d-1107">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="abf1d-1108">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="abf1d-1109">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1109">Breaking changes</span></span>
    - <span data-ttu-id="abf1d-1110">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="abf1d-1111">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="abf1d-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="abf1d-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="abf1d-1113">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="abf1d-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="abf1d-1114">Az.Dns</span></span>
* <span data-ttu-id="abf1d-1115">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="abf1d-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="abf1d-1116">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="abf1d-1117">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="abf1d-1119">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="abf1d-1120">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="abf1d-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="abf1d-1121">Az.HDInsight</span></span>
* <span data-ttu-id="abf1d-1122">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="abf1d-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="abf1d-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="abf1d-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="abf1d-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="abf1d-1125">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="abf1d-1126">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="abf1d-1127">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="abf1d-1128">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1129">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-1130">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="abf1d-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="abf1d-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="abf1d-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="abf1d-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="abf1d-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="abf1d-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="abf1d-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="abf1d-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="abf1d-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="abf1d-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="abf1d-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="abf1d-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="abf1d-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="abf1d-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="abf1d-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="abf1d-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="abf1d-1142">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="abf1d-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="abf1d-1143">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1144">Az.Network</span></span>
* <span data-ttu-id="abf1d-1145">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="abf1d-1146">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-1146">New cmdlets</span></span>
        - <span data-ttu-id="abf1d-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="abf1d-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="abf1d-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="abf1d-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="abf1d-1151">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="abf1d-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="abf1d-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="abf1d-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="abf1d-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="abf1d-1154">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="abf1d-1155">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="abf1d-1156">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abf1d-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="abf1d-1158">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="abf1d-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="abf1d-1159">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="abf1d-1160">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-1162">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="abf1d-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="abf1d-1163">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="abf1d-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="abf1d-1164">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="abf1d-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="abf1d-1165">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="abf1d-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="abf1d-1166">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="abf1d-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="abf1d-1167">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="abf1d-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="abf1d-1168">Az.Relay</span></span>
* <span data-ttu-id="abf1d-1169">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-1171">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1172">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1173">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="abf1d-1174">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="abf1d-1175">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="abf1d-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="abf1d-1177">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="abf1d-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="abf1d-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="abf1d-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1181">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1182">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="abf1d-1183">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="abf1d-1184">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abf1d-1185">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="abf1d-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="abf1d-1186">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="abf1d-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="abf1d-1187">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abf1d-1188">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abf1d-1189">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abf1d-1190">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abf1d-1191">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abf1d-1192">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1193">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1194">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="abf1d-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-1195">Az.Batch</span></span>
* <span data-ttu-id="abf1d-1196">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abf1d-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-1197">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-1198">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-1200">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1201">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1202">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="abf1d-1203">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1204">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-1205">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-1206">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1208">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abf1d-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abf1d-1209">Az.EventGrid</span></span>
* <span data-ttu-id="abf1d-1210">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-1211">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-1212">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="abf1d-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="abf1d-1213">Az.HDInsight</span></span>
* <span data-ttu-id="abf1d-1214">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-1215">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-1216">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-1217">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-1218">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1219">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="abf1d-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="abf1d-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="abf1d-1221">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="abf1d-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="abf1d-1222">Az.Media</span></span>
* <span data-ttu-id="abf1d-1223">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1224">Az.Monitor</span></span>
  * <span data-ttu-id="abf1d-1225">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="abf1d-1226">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="abf1d-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="abf1d-1227">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="abf1d-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="abf1d-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abf1d-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="abf1d-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abf1d-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="abf1d-1230">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="abf1d-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="abf1d-1231">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1232">Az.Network</span></span>
* <span data-ttu-id="abf1d-1233">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1234">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="abf1d-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="abf1d-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="abf1d-1236">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-1238">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="abf1d-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="abf1d-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="abf1d-1240">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-1242">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1243">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="abf1d-1244">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="abf1d-1245">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abf1d-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abf1d-1246">Az.RedisCache</span></span>
* <span data-ttu-id="abf1d-1247">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1248">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1249">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1250">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1251">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="abf1d-1252">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1253">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="abf1d-1254">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="abf1d-1255">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="abf1d-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="abf1d-1256">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="abf1d-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="abf1d-1257">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1258">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1259">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="abf1d-1260">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="abf1d-1261">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="abf1d-1262">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="abf1d-1263">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abf1d-1264">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="abf1d-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="abf1d-1265">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="abf1d-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="abf1d-1266">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abf1d-1267">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abf1d-1268">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abf1d-1269">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abf1d-1270">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abf1d-1271">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1272">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1273">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="abf1d-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abf1d-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="abf1d-1275">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="abf1d-1276">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1277">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1278">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="abf1d-1279">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="abf1d-1280">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="abf1d-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1281">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1282">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="abf1d-1283">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="abf1d-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="abf1d-1285">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="abf1d-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-1286">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-1287">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="abf1d-1288">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1289">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1290">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="abf1d-1291">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="abf1d-1292">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="abf1d-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="abf1d-1293">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="abf1d-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="abf1d-1294">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="abf1d-1295">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="abf1d-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1296">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1297">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1298">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1299">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="abf1d-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="abf1d-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="abf1d-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="abf1d-1301">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="abf1d-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="abf1d-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="abf1d-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="abf1d-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="abf1d-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="abf1d-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="abf1d-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="abf1d-1306">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="abf1d-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="abf1d-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="abf1d-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="abf1d-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="abf1d-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="abf1d-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="abf1d-1311">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="abf1d-1312">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="abf1d-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="abf1d-1313">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="abf1d-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="abf1d-1314">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="abf1d-1315">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="abf1d-1316">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="abf1d-1317">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abf1d-1318">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="abf1d-1319">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1320">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1321">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="abf1d-1322">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="abf1d-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="abf1d-1323">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1323">Pre-Post script</span></span>
    * <span data-ttu-id="abf1d-1324">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="abf1d-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1325">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1326">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="abf1d-1327">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-1328">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-1329">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1330">Az.Network</span></span>
* <span data-ttu-id="abf1d-1331">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="abf1d-1332">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-1334">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="abf1d-1335">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1336">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1337">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="abf1d-1338">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1339">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1340">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1341">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1342">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="abf1d-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abf1d-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abf1d-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="abf1d-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="abf1d-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="abf1d-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="abf1d-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="abf1d-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1349">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1350">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="abf1d-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="abf1d-1351">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1352">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1353">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="abf1d-1354">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1355">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1356">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="abf1d-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="abf1d-1357">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="abf1d-1358">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abf1d-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-1359">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-1360">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1361">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1362">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-1363">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-1364">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abf1d-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abf1d-1365">Az.LogicApp</span></span>
* <span data-ttu-id="abf1d-1366">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1367">Az.Network</span></span>
* <span data-ttu-id="abf1d-1368">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-1370">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="abf1d-1371">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="abf1d-1371">SDK Update</span></span>
* <span data-ttu-id="abf1d-1372">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="abf1d-1373">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1374">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1375">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="abf1d-1376">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="abf1d-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="abf1d-1377">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="abf1d-1378">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="abf1d-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="abf1d-1379">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="abf1d-1380">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="abf1d-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1381">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1382">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="abf1d-1383">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1384">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1385">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="abf1d-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="abf1d-1386">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="abf1d-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="abf1d-1388">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1389">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1390">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="abf1d-1391">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="abf1d-1392">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-1394">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1395">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1396">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="abf1d-1397">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="abf1d-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="abf1d-1398">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="abf1d-1399">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1401">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="abf1d-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-1402">Az.EventHub</span></span>
* <span data-ttu-id="abf1d-1403">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-1404">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-1405">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abf1d-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abf1d-1406">Az.LogicApp</span></span>
* <span data-ttu-id="abf1d-1407">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="abf1d-1408">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="abf1d-1409">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="abf1d-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="abf1d-1410">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abf1d-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abf1d-1411">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abf1d-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abf1d-1412">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abf1d-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="abf1d-1413">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="abf1d-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="abf1d-1414">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="abf1d-1415">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abf1d-1416">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abf1d-1417">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="abf1d-1418">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="abf1d-1419">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="abf1d-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1420">Az.Monitor</span></span>
* <span data-ttu-id="abf1d-1421">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1422">Az.Network</span></span>
* <span data-ttu-id="abf1d-1423">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="abf1d-1425">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="abf1d-1426">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="abf1d-1427">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="abf1d-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1428">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1429">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="abf1d-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="abf1d-1430">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="abf1d-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="abf1d-1431">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="abf1d-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="abf1d-1432">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1433">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1434">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="abf1d-1435">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="abf1d-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1436">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1437">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="abf1d-1438">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1439">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1440">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abf1d-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="abf1d-1442">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="abf1d-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1443">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1444">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="abf1d-1445">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="abf1d-1446">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="abf1d-1448">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1449">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1450">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="abf1d-1451">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="abf1d-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="abf1d-1452">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="abf1d-1453">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="abf1d-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1454">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1455">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="abf1d-1456">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="abf1d-1457">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="abf1d-1458">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1459">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1460">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="abf1d-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="abf1d-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="abf1d-1462">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="abf1d-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="abf1d-1464">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="abf1d-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="abf1d-1465">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1466">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1467">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="abf1d-1468">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abf1d-1469">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="abf1d-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="abf1d-1470">Az.Aks</span></span>
* <span data-ttu-id="abf1d-1471">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="abf1d-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1472">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1473">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="abf1d-1474">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="abf1d-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="abf1d-1475">Az.Cdn</span></span>
* <span data-ttu-id="abf1d-1476">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1477">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1478">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="abf1d-1479">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="abf1d-1480">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="abf1d-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="abf1d-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="abf1d-1482">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="abf1d-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="abf1d-1483">Az.DataFactory</span></span>
* <span data-ttu-id="abf1d-1484">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1486">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="abf1d-1487">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="abf1d-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="abf1d-1488">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-1489">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-1490">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="abf1d-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-1491">Az.KeyVault</span></span>
* <span data-ttu-id="abf1d-1492">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1493">Az.Network</span></span>
* <span data-ttu-id="abf1d-1494">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1495">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1496">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="abf1d-1497">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="abf1d-1498">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="abf1d-1499">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="abf1d-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="abf1d-1500">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="abf1d-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="abf1d-1501">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="abf1d-1502">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="abf1d-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-1504">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="abf1d-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="abf1d-1505">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1505">Fix some error messages.</span></span>
* <span data-ttu-id="abf1d-1506">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="abf1d-1507">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="abf1d-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="abf1d-1508">Az.SignalR</span></span>
* <span data-ttu-id="abf1d-1509">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1510">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1511">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abf1d-1512">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="abf1d-1513">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="abf1d-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="abf1d-1514">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="abf1d-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1515">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1516">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abf1d-1517">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="abf1d-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="abf1d-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="abf1d-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="abf1d-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="abf1d-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="abf1d-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="abf1d-1521">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1522">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1523">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="abf1d-1524">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="abf1d-1525">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="abf1d-1526">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="abf1d-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="abf1d-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1527">Az.Accounts</span></span>
* <span data-ttu-id="abf1d-1528">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1529">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1530">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="abf1d-1531">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="abf1d-1532">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1534">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="abf1d-1535">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="abf1d-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="abf1d-1536">Az.EventGrid</span></span>
* <span data-ttu-id="abf1d-1537">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="abf1d-1538">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="abf1d-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="abf1d-1539">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="abf1d-1540">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="abf1d-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="abf1d-1541">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="abf1d-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="abf1d-1542">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="abf1d-1543">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="abf1d-1544">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="abf1d-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="abf1d-1545">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="abf1d-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="abf1d-1546">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="abf1d-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="abf1d-1547">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="abf1d-1548">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="abf1d-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="abf1d-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="abf1d-1549">Az.IotHub</span></span>
* <span data-ttu-id="abf1d-1550">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="abf1d-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="abf1d-1551">Az.LogicApp</span></span>
* <span data-ttu-id="abf1d-1552">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="abf1d-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1553">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1554">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="abf1d-1555">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="abf1d-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="abf1d-1556">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="abf1d-1557">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="abf1d-1558">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="abf1d-1559">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="abf1d-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="abf1d-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="abf1d-1560">Az.SignalR</span></span>
* <span data-ttu-id="abf1d-1561">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1562">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1563">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="abf1d-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1564">Az.Storage</span></span>
* <span data-ttu-id="abf1d-1565">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="abf1d-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="abf1d-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="abf1d-1567">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="abf1d-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="abf1d-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="abf1d-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1569">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1570">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="abf1d-1571">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="abf1d-1572">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="abf1d-1573">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-1573">General</span></span>

- <span data-ttu-id="abf1d-1574">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="abf1d-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="abf1d-1575">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="abf1d-1575">Online help for each module</span></span>
- <span data-ttu-id="abf1d-1576">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="abf1d-1577">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="abf1d-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="abf1d-1578">Az.Accounts</span></span>
- <span data-ttu-id="abf1d-1579">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="abf1d-1580">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abf1d-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="abf1d-1582">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="abf1d-1582">Fixes for #7002</span></span>
- <span data-ttu-id="abf1d-1583">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="abf1d-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="abf1d-1584">Az.Batch</span></span>
- <span data-ttu-id="abf1d-1585">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="abf1d-1586">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="abf1d-1587">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="abf1d-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="abf1d-1588">Az.Billing</span></span>
- <span data-ttu-id="abf1d-1589">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="abf1d-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="abf1d-1591">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="abf1d-1592">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abf1d-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="abf1d-1594">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="abf1d-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="abf1d-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="abf1d-1596">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="abf1d-1598">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="abf1d-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1599">Az.Monitor</span></span>
- <span data-ttu-id="abf1d-1600">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="abf1d-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="abf1d-1601">Az.KeyVault</span></span>
- <span data-ttu-id="abf1d-1602">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="abf1d-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="abf1d-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="abf1d-1604">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="abf1d-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="abf1d-1605">Az.Media</span></span>
- <span data-ttu-id="abf1d-1606">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abf1d-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1607">Az.Network</span></span>
<span data-ttu-id="abf1d-1608">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="abf1d-1609">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="abf1d-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="abf1d-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="abf1d-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="abf1d-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="abf1d-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="abf1d-1618">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="abf1d-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abf1d-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="abf1d-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abf1d-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="abf1d-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="abf1d-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="abf1d-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="abf1d-1624">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="abf1d-1625">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="abf1d-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="abf1d-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abf1d-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abf1d-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abf1d-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="abf1d-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="abf1d-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="abf1d-1629">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="abf1d-1630">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="abf1d-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="abf1d-1632">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="abf1d-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1633">Az.Profile</span></span>
- <span data-ttu-id="abf1d-1634">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="abf1d-1636">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="abf1d-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1637">Az.Resources</span></span>
- <span data-ttu-id="abf1d-1638">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abf1d-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="abf1d-1640">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="abf1d-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="abf1d-1641">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="abf1d-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abf1d-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="abf1d-1643">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="abf1d-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="abf1d-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1644">Az.Sql</span></span>
- <span data-ttu-id="abf1d-1645">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="abf1d-1646">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="abf1d-1647">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="abf1d-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1648">Az.Storage</span></span>
- <span data-ttu-id="abf1d-1649">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abf1d-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1650">Az.Websites</span></span>
- <span data-ttu-id="abf1d-1651">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="abf1d-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="abf1d-1652">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="abf1d-1653">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-1653">General</span></span>

* <span data-ttu-id="abf1d-1654">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="abf1d-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="abf1d-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1655">Az.Compute</span></span>

* <span data-ttu-id="abf1d-1656">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="abf1d-1658">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="abf1d-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="abf1d-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="abf1d-1660">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="abf1d-1661">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="abf1d-1662">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="abf1d-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="abf1d-1664">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="abf1d-1665">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="abf1d-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1666">Az.Resources</span></span>

* <span data-ttu-id="abf1d-1667">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="abf1d-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="abf1d-1668">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="abf1d-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1669">Az.Sql</span></span>

* <span data-ttu-id="abf1d-1670">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="abf1d-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="abf1d-1671">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="abf1d-1672">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="abf1d-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1673">Az.Storage</span></span>

* <span data-ttu-id="abf1d-1674">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="abf1d-1675">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="abf1d-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abf1d-1677">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="abf1d-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abf1d-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="abf1d-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="abf1d-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="abf1d-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1680">Az.Websites</span></span>

* <span data-ttu-id="abf1d-1681">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="abf1d-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="abf1d-1682">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="abf1d-1683">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="abf1d-1684">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="abf1d-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="abf1d-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="abf1d-1686">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="abf1d-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="abf1d-1687">Az.Automation</span></span>
* <span data-ttu-id="abf1d-1688">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="abf1d-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="abf1d-1689">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="abf1d-1690">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="abf1d-1691">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="abf1d-1692">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="abf1d-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1693">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1694">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="abf1d-1695">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="abf1d-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="abf1d-1697">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="abf1d-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="abf1d-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="abf1d-1699">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="abf1d-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1700">Az.Network</span></span>
* <span data-ttu-id="abf1d-1701">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="abf1d-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="abf1d-1702">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="abf1d-1703">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="abf1d-1704">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="abf1d-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="abf1d-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="abf1d-1706">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="abf1d-1707">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="abf1d-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="abf1d-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="abf1d-1709">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="abf1d-1710">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="abf1d-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="abf1d-1711">Az.Relay</span></span>
* <span data-ttu-id="abf1d-1712">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="abf1d-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="abf1d-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1713">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1714">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="abf1d-1715">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="abf1d-1716">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="abf1d-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="abf1d-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-1718">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="abf1d-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1719">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1720">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="abf1d-1721">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abf1d-1722">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abf1d-1723">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abf1d-1724">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="abf1d-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="abf1d-1725">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abf1d-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abf1d-1726">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abf1d-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abf1d-1727">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abf1d-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="abf1d-1728">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="abf1d-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="abf1d-1729">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="abf1d-1730">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="abf1d-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="abf1d-1731">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="abf1d-1732">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="abf1d-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abf1d-1733">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="abf1d-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="abf1d-1734">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="abf1d-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="abf1d-1735">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="abf1d-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="abf1d-1736">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="abf1d-1737">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="abf1d-1738">Allgemein</span><span class="sxs-lookup"><span data-stu-id="abf1d-1738">General</span></span>
* <span data-ttu-id="abf1d-1739">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="abf1d-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1740">Az.Profile</span></span>
* <span data-ttu-id="abf1d-1741">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="abf1d-1742">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="abf1d-1743">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="abf1d-1744">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="abf1d-1745">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="abf1d-1746">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="abf1d-1747">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="abf1d-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-1749">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1750">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1751">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="abf1d-1752">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="abf1d-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="abf1d-1753">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1755">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="abf1d-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="abf1d-1756">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="abf1d-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1757">Az.Insights</span></span>
* <span data-ttu-id="abf1d-1758">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="abf1d-1759">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="abf1d-1760">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="abf1d-1761">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1762">Az.Network</span></span>
* <span data-ttu-id="abf1d-1763">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="abf1d-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="abf1d-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="abf1d-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="abf1d-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abf1d-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="abf1d-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="abf1d-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="abf1d-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="abf1d-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="abf1d-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="abf1d-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="abf1d-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="abf1d-1771">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1772">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1773">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="abf1d-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="abf1d-1774">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="abf1d-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="abf1d-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="abf1d-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="abf1d-1776">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="abf1d-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="abf1d-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="abf1d-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="abf1d-1778">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="abf1d-1779">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="abf1d-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="abf1d-1780">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="abf1d-1781">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="abf1d-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="abf1d-1782">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="abf1d-1783">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="abf1d-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1784">Az.Profile</span></span>
* <span data-ttu-id="abf1d-1785">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="abf1d-1786">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1787">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1788">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="abf1d-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="abf1d-1789">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="abf1d-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abf1d-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="abf1d-1791">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="abf1d-1792">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="abf1d-1793">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abf1d-1794">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="abf1d-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1796">Az.Network</span></span>
* <span data-ttu-id="abf1d-1797">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="abf1d-1798">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1799">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1800">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="abf1d-1801">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="abf1d-1802">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="abf1d-1803">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1803">Azure.Storage</span></span>
* <span data-ttu-id="abf1d-1804">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="abf1d-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="abf1d-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="abf1d-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="abf1d-1807">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="abf1d-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="abf1d-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="abf1d-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="abf1d-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="abf1d-1810">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="abf1d-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="abf1d-1811">Az.Compute</span></span>
* <span data-ttu-id="abf1d-1812">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="abf1d-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="abf1d-1813">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="abf1d-1814">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="abf1d-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="abf1d-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="abf1d-1816">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="abf1d-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="abf1d-1817">Az.Network</span></span>
* <span data-ttu-id="abf1d-1818">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="abf1d-1819">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1819">new cmdlets added</span></span>
    - <span data-ttu-id="abf1d-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="abf1d-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="abf1d-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="abf1d-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="abf1d-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="abf1d-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="abf1d-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="abf1d-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="abf1d-1826">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="abf1d-1827">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="abf1d-1828">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="abf1d-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="abf1d-1829">Az.RedisCache</span></span>
* <span data-ttu-id="abf1d-1830">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="abf1d-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="abf1d-1831">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="abf1d-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="abf1d-1832">Az.Resources</span></span>
* <span data-ttu-id="abf1d-1833">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="abf1d-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="abf1d-1834">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="abf1d-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="abf1d-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="abf1d-1835">Az.Sql</span></span>
* <span data-ttu-id="abf1d-1836">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="abf1d-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="abf1d-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="abf1d-1837">Az.Websites</span></span>
* <span data-ttu-id="abf1d-1838">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="abf1d-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="abf1d-1839">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="abf1d-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="abf1d-1840">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="abf1d-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="abf1d-1841">Erste Version</span><span class="sxs-lookup"><span data-stu-id="abf1d-1841">Initial Release</span></span>
