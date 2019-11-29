---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537120"
---
## <a name="310---november-2019"></a><span data-ttu-id="6f357-103">3.1.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6f357-104">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="6f357-104">Highlights since the last major release</span></span>
* <span data-ttu-id="6f357-105">Az.DataBoxEdge 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="6f357-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6f357-106">Az.SqlVirtualMachine 1.0.0 veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="6f357-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-107">Az.Compute</span></span>
* <span data-ttu-id="6f357-108">Funktion zum erneuten Anwenden von VMs</span><span class="sxs-lookup"><span data-stu-id="6f357-108">VM Reapply feature</span></span>
    - <span data-ttu-id="6f357-109">Parameter für erneutes Anwenden zu Cmdlet „Set-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6f357-110">AutomaticRepairs-Funktion für VM-Skalierungsgruppe:</span><span class="sxs-lookup"><span data-stu-id="6f357-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6f357-111">Parameter „EnableAutomaticRepair“, „AutomaticRepairGracePeriod“ und „AutomaticRepairMaxInstanceRepairsPercent“ zu folgenden Cmdlets hinzugefügt:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f357-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6f357-112">Mandantenübergreifende Unterstützung von Katalogimages für „New-AzVM“</span><span class="sxs-lookup"><span data-stu-id="6f357-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6f357-113">„Spot“ zu Argumentvervollständigung des Priority-Parameters in Cmdlets „New-AzVM“, „New-AzVMConfig“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6f357-114">Parameter „DiskIOPSReadWrite“ und „DiskMBpsReadWrite“ zu Cmdlet „Add-AzVmssDataDisk“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6f357-115">Parameter „SourceImageId“ von Cmdlet „New-AzGalleryImageVersion“ in optional geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6f357-116">Parameter „OSDiskImage“ und „DataDiskImage“ zu Cmdlet „New-AzGalleryImageVersion“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6f357-117">Parameter „HyperVGeneration“ zu Cmdlet „New-AzGalleryImageDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6f357-118">Parameter „SkipExtensionsOnOverprovisionedVMs“ zu Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6f357-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6f357-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6f357-120">Cmdlet `Get-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6f357-121">Bestellung abrufen</span><span class="sxs-lookup"><span data-stu-id="6f357-121">Get the Order</span></span>
* <span data-ttu-id="6f357-122">Cmdlet `New-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6f357-123">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="6f357-123">Create new Order</span></span>
* <span data-ttu-id="6f357-124">Cmdlet `Remove-AzDataBoxEdgeOrder` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6f357-125">Bestellung entfernen</span><span class="sxs-lookup"><span data-stu-id="6f357-125">Remove the Order</span></span>
* <span data-ttu-id="6f357-126">Änderung im Cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="6f357-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6f357-127">Erstellt jetzt eine lokale Freigabe</span><span class="sxs-lookup"><span data-stu-id="6f357-127">Now creates Local Share</span></span>
* <span data-ttu-id="6f357-128">Cmdlet `Set-AzDataBoxEdgeRole` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6f357-129">„IotRole“ kann jetzt einer Freigabe zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6f357-130">Cmdlet `Invoke-AzDataBoxEdgeDevice` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6f357-131">Scanupdate aufrufen, Update herunterladen, Updates auf dem Gerät installieren</span><span class="sxs-lookup"><span data-stu-id="6f357-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6f357-132">Cmdlet `Get-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6f357-133">Ruft die Informationen zu Auslösern ab</span><span class="sxs-lookup"><span data-stu-id="6f357-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="6f357-134">Cmdlet `New-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6f357-135">Neue Auslöser erstellen</span><span class="sxs-lookup"><span data-stu-id="6f357-135">Create new Triggers</span></span>
* <span data-ttu-id="6f357-136">Cmdlet `Remove-AzDataBoxEdgeTrigger` hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6f357-137">Auslöser entfernen</span><span class="sxs-lookup"><span data-stu-id="6f357-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-138">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-139">Version des ADF .NET SDK auf 4.4.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6f357-140">Parameter „ExpressCustomSetup“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um Setupkonfigurationen und Drittanbieterkomponenten ohne benutzerdefiniertes Setupskript zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6f357-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-142">Dokumentation von „Get-AzDataLakeStoreDeletedItem“ und „Restore-AzDataLakeStoreDeletedItem“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-143">Az.EventHub</span></span>
* <span data-ttu-id="6f357-144">Behebung des Problems 10301: Datumsformat von SAS-Token korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6f357-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6f357-145">Az.FrontDoor</span></span>
* <span data-ttu-id="6f357-146">Parameter „MinimumTlsVersion“ zu „Enable-AzFrontDoorCustomDomainHttps“ und „New-AzFrontDoorFrontendEndpointObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6f357-147">Parameter „HealthProbeMethod“ und „EnabledState“ zu „New-AzFrontDoorHealthProbeSettingObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6f357-148">Neues Cmdlet zum Erstellen von BackendPoolsSettings-Objekten für die Übergabe in Erstellung/Update von Front Door hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6f357-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6f357-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-150">Az.Network</span></span>
* <span data-ttu-id="6f357-151">FilterData-Optionsbeispiele „Start-AzVirtualNetworkGatewayConnectionPacketCapture.md“ und „Start-AzVirtualnetworkGatewayPacketCapture.md“ geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6f357-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6f357-152">Az.PrivateDns</span></span>
* <span data-ttu-id="6f357-153">PrivateDns.net-SDK auf Version 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-155">Azure Site Recovery-Unterstützung zum Auswählen des Datenträgertyps beim Aktivieren des Schutzes.</span><span class="sxs-lookup"><span data-stu-id="6f357-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6f357-156">Fehlerbehebung bei Bearbeitungsaktion für Azure Site Recovery-Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="6f357-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6f357-157">SQL-Wiederherstellungsunterstützung für Azure Backup zum Akzeptieren von Filestream-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="6f357-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6f357-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6f357-158">Az.RedisCache</span></span>
* <span data-ttu-id="6f357-159">Parameter „MinimumTlsVersion“ in Cmdlets „New-AzRedisCache“ und „Set-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6f357-160">Außerdem „MinimumTlsVersion“ in Ausgabe von Cmdlet „Get-AzRedisCache“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6f357-161">Validierung von Parameter „-Size“ für Cmdlets „Set-AzRedisCache“ und „New-AzRedisCache“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-162">Az.Resources</span></span>
- <span data-ttu-id="6f357-163">Richtlinien-Cmdlets aktualisiert, um die neue API-Version 2019-06-01 mit der neuen EnforcementMode-Eigenschaft bei der Richtlinienzuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f357-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6f357-164">Hilfebeispiel zum Erstellen von Richtliniendefinitionen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="6f357-165">Fehlerkorrektur: „Remove-AZADServicePrincipal -ServicePrincipalName“ gibt Nullverweis aus, wenn Dienstprinzipalname nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6f357-166">Fehlerkorrektur: „New-AZADServicePrincipal“ gibt Nullverweis aus, wenn Mandant kein Abonnement hat.</span><span class="sxs-lookup"><span data-stu-id="6f357-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6f357-167">„New-AzAdServicePrincipal“ geändert, um Anmeldeinformation nur zu zugeordneter Anwendung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f357-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-168">Az.Sql</span></span>
* <span data-ttu-id="6f357-169">Unterstützung von „ReadReplicaCount“ für Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6f357-170">Korrektur von „Set-AzSqlDatabase“, wenn Zonenredundanz nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="6f357-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6f357-171">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6f357-172">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-172">General</span></span>
* <span data-ttu-id="6f357-173">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="6f357-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6f357-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-174">Az.Accounts</span></span>
* <span data-ttu-id="6f357-175">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6f357-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6f357-176">Az.Advisor</span></span>
* <span data-ttu-id="6f357-177">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6f357-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f357-178">Az.Batch</span></span>
* <span data-ttu-id="6f357-179">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6f357-180">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6f357-181">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="6f357-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6f357-182">Für den Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6f357-183">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="6f357-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6f357-184">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6f357-185">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6f357-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6f357-186">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="6f357-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6f357-187">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="6f357-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6f357-188">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6f357-189">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6f357-190">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="6f357-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6f357-191">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6f357-192">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="6f357-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6f357-193">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6f357-194">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6f357-195">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6f357-196">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6f357-197">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6f357-198">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f357-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="6f357-199">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6f357-200">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6f357-201">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6f357-202">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6f357-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="6f357-203">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="6f357-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6f357-204">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f357-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="6f357-205">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6f357-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6f357-206">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6f357-207">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="6f357-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6f357-208">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="6f357-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6f357-209">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="6f357-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6f357-210">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="6f357-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6f357-211">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6f357-212">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="6f357-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6f357-213">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="6f357-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6f357-214">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="6f357-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6f357-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-215">Az.Cdn</span></span>
* <span data-ttu-id="6f357-216">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6f357-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6f357-217">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="6f357-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-218">Az.Compute</span></span>
* <span data-ttu-id="6f357-219">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="6f357-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6f357-220">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6f357-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6f357-221">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6f357-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="6f357-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6f357-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6f357-223">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6f357-224">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6f357-225">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="6f357-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6f357-226">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6f357-227">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="6f357-227">Breaking changes</span></span>
    - <span data-ttu-id="6f357-228">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6f357-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6f357-229">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6f357-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-230">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-231">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-233">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="6f357-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6f357-234">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="6f357-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6f357-235">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="6f357-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6f357-236">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="6f357-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6f357-237">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="6f357-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6f357-238">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="6f357-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6f357-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6f357-239">Az.FrontDoor</span></span>
* <span data-ttu-id="6f357-240">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6f357-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6f357-241">Az.HDInsight</span></span>
* <span data-ttu-id="6f357-242">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="6f357-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6f357-243">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6f357-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6f357-244">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6f357-245">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="6f357-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6f357-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6f357-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6f357-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6f357-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6f357-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6f357-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6f357-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f357-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6f357-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f357-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6f357-251">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="6f357-252">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="6f357-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6f357-253">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="6f357-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6f357-254">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="6f357-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6f357-255">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6f357-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6f357-256">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6f357-257">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6f357-258">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="6f357-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6f357-259">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6f357-260">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6f357-261">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6f357-262">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="6f357-263">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="6f357-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-264">Az.IotHub</span></span>
* <span data-ttu-id="6f357-265">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="6f357-265">Breaking changes:</span></span>
    - <span data-ttu-id="6f357-266">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="6f357-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6f357-267">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6f357-268">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="6f357-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6f357-269">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6f357-270">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6f357-271">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6f357-272">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="6f357-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6f357-273">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="6f357-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6f357-274">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="6f357-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6f357-275">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6f357-276">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="6f357-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6f357-277">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-279">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-280">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6f357-281">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6f357-282">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-283">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-284">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-285">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-286">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-287">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-288">Az.Resources</span></span>
* <span data-ttu-id="6f357-289">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-290">Az.Network</span></span>
* <span data-ttu-id="6f357-291">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6f357-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6f357-292">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f357-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="6f357-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6f357-298">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="6f357-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6f357-299">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f357-299">New cmdlet:</span></span>
        - <span data-ttu-id="6f357-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6f357-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6f357-301">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6f357-302">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6f357-303">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6f357-304">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6f357-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6f357-305">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6f357-306">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6f357-307">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6f357-308">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-308">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6f357-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6f357-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6f357-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6f357-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6f357-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6f357-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6f357-314">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6f357-315">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6f357-316">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6f357-317">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6f357-318">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6f357-319">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6f357-320">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6f357-321">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-321">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6f357-323">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6f357-324">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6f357-325">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6f357-326">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6f357-327">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6f357-328">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6f357-329">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6f357-330">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-330">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6f357-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6f357-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6f357-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6f357-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6f357-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6f357-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6f357-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6f357-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6f357-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6f357-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6f357-337">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6f357-338">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6f357-339">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6f357-340">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6f357-341">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6f357-342">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6f357-343">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6f357-344">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6f357-345">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="6f357-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6f357-346">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6f357-347">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6f357-348">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-348">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="6f357-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6f357-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6f357-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-354">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="6f357-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-355">Az.Sql</span></span>
* <span data-ttu-id="6f357-356">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6f357-357">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="6f357-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6f357-358">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="6f357-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6f357-359">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="6f357-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6f357-360">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="6f357-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6f357-361">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6f357-362">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6f357-363">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="6f357-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="6f357-364">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-365">Az.Storage</span></span>
* <span data-ttu-id="6f357-366">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6f357-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6f357-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6f357-369">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6f357-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6f357-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6f357-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6f357-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6f357-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="6f357-372">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6f357-373">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-373">General</span></span>
* <span data-ttu-id="6f357-374">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6f357-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6f357-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-375">Az.Accounts</span></span>
* <span data-ttu-id="6f357-376">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6f357-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-377">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-378">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6f357-379">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="6f357-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-380">Az.Automation</span></span>
* <span data-ttu-id="6f357-381">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="6f357-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f357-382">Az.Batch</span></span>
* <span data-ttu-id="6f357-383">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6f357-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-384">Az.Compute</span></span>
* <span data-ttu-id="6f357-385">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6f357-386">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6f357-387">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="6f357-388">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="6f357-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-389">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-390">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="6f357-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6f357-391">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="6f357-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6f357-392">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-394">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="6f357-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6f357-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6f357-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="6f357-396">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6f357-397">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6f357-398">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="6f357-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6f357-399">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-400">Az.IotHub</span></span>
* <span data-ttu-id="6f357-401">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6f357-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6f357-402">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="6f357-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="6f357-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-403">Az.Monitor</span></span>
* <span data-ttu-id="6f357-404">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6f357-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6f357-405">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6f357-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6f357-406">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="6f357-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6f357-407">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="6f357-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-408">Az.Network</span></span>
* <span data-ttu-id="6f357-409">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="6f357-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6f357-410">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6f357-411">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-411">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6f357-413">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6f357-414">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6f357-415">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="6f357-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6f357-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6f357-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6f357-419">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6f357-420">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6f357-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6f357-421">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6f357-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6f357-422">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="6f357-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6f357-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6f357-423">Az.RedisCache</span></span>
* <span data-ttu-id="6f357-424">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="6f357-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-425">Az.Sql</span></span>
* <span data-ttu-id="6f357-426">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-427">Az.Storage</span></span>
* <span data-ttu-id="6f357-428">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6f357-429">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="6f357-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6f357-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6f357-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6f357-431">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="6f357-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6f357-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6f357-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6f357-433">Az.StorageSync</span></span>
* <span data-ttu-id="6f357-434">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-435">Az.Websites</span></span>
* <span data-ttu-id="6f357-436">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="6f357-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6f357-437">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6f357-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-438">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-439">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6f357-440">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6f357-441">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="6f357-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-442">Az.Automation</span></span>
* <span data-ttu-id="6f357-443">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6f357-444">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6f357-445">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-446">Az.Compute</span></span>
* <span data-ttu-id="6f357-447">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6f357-448">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6f357-449">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6f357-450">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6f357-451">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6f357-452">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="6f357-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6f357-453">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6f357-454">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6f357-455">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-456">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-457">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6f357-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6f357-458">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6f357-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6f357-459">Az.HDInsight</span></span>
* <span data-ttu-id="6f357-460">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-461">Az.IotHub</span></span>
* <span data-ttu-id="6f357-462">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6f357-463">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6f357-464">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="6f357-464">New cmdlets are:</span></span>
    - <span data-ttu-id="6f357-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6f357-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6f357-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6f357-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6f357-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6f357-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6f357-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6f357-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-469">Az.Monitor</span></span>
* <span data-ttu-id="6f357-470">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="6f357-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6f357-471">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="6f357-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6f357-472">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6f357-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6f357-473">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="6f357-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="6f357-474">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="6f357-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6f357-475">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="6f357-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6f357-476">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="6f357-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6f357-477">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6f357-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6f357-478">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6f357-479">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6f357-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6f357-480">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6f357-481">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6f357-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6f357-482">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="6f357-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6f357-483">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="6f357-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6f357-484">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="6f357-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6f357-485">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="6f357-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6f357-486">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="6f357-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6f357-487">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="6f357-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6f357-488">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6f357-489">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="6f357-489">Overall improved help files</span></span>
* <span data-ttu-id="6f357-490">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-491">Az.Network</span></span>
* <span data-ttu-id="6f357-492">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="6f357-493">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6f357-494">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="6f357-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6f357-495">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="6f357-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6f357-496">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="6f357-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6f357-497">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6f357-498">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6f357-499">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6f357-500">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6f357-501">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6f357-502">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6f357-503">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="6f357-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6f357-504">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-504">New cmdlets</span></span>
        - <span data-ttu-id="6f357-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6f357-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6f357-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6f357-507">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f357-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="6f357-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6f357-508">New-VpnSite</span></span>
        - <span data-ttu-id="6f357-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6f357-509">Update-VpnSite</span></span>
        - <span data-ttu-id="6f357-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-510">New-VpnConnection</span></span>
        - <span data-ttu-id="6f357-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-511">Update-VpnConnection</span></span>
* <span data-ttu-id="6f357-512">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f357-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-514">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6f357-515">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-516">Az.Resources</span></span>
* <span data-ttu-id="6f357-517">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="6f357-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-519">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6f357-520">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6f357-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6f357-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6f357-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6f357-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6f357-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6f357-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6f357-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6f357-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6f357-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6f357-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6f357-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6f357-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6f357-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6f357-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6f357-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6f357-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6f357-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6f357-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6f357-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6f357-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6f357-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6f357-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6f357-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6f357-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6f357-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6f357-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6f357-534">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="6f357-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6f357-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6f357-535">Az.SignalR</span></span>
* <span data-ttu-id="6f357-536">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-537">Az.Sql</span></span>
* <span data-ttu-id="6f357-538">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6f357-539">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="6f357-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6f357-540">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="6f357-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6f357-541">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="6f357-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6f357-542">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="6f357-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-543">Az.Storage</span></span>
* <span data-ttu-id="6f357-544">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6f357-545">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f357-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6f357-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6f357-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6f357-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6f357-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6f357-548">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6f357-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f357-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6f357-550">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="6f357-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6f357-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6f357-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6f357-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6f357-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6f357-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6f357-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6f357-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6f357-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-555">Az.Websites</span></span>
* <span data-ttu-id="6f357-556">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="6f357-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6f357-557">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6f357-558">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6f357-559">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6f357-560">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-560">General</span></span>
* <span data-ttu-id="6f357-561">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6f357-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-562">Az.Accounts</span></span>
* <span data-ttu-id="6f357-563">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="6f357-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6f357-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6f357-564">Az.Aks</span></span>
* <span data-ttu-id="6f357-565">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6f357-566">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="6f357-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6f357-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-567">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-568">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="6f357-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6f357-569">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="6f357-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6f357-570">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6f357-571">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="6f357-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6f357-572">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="6f357-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6f357-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f357-573">Az.Batch</span></span>
* <span data-ttu-id="6f357-574">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="6f357-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6f357-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-575">Az.Cdn</span></span>
* <span data-ttu-id="6f357-576">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-577">Az.Compute</span></span>
* <span data-ttu-id="6f357-578">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6f357-579">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6f357-580">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6f357-581">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6f357-582">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6f357-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6f357-583">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6f357-584">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6f357-585">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-586">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-587">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="6f357-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6f357-588">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6f357-589">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="6f357-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6f357-590">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-592">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-593">Az.EventHub</span></span>
* <span data-ttu-id="6f357-594">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="6f357-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6f357-595">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="6f357-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6f357-596">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6f357-597">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6f357-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6f357-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6f357-599">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-600">Az.Monitor</span></span>
* <span data-ttu-id="6f357-601">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-602">Az.Network</span></span>
* <span data-ttu-id="6f357-603">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6f357-604">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="6f357-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6f357-605">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="6f357-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6f357-606">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6f357-607">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="6f357-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="6f357-608">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6f357-609">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="6f357-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-611">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="6f357-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6f357-612">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-612">Added example</span></span>
    - <span data-ttu-id="6f357-613">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6f357-614">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6f357-615">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-617">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-618">Az.Resources</span></span>
* <span data-ttu-id="6f357-619">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6f357-620">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6f357-621">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6f357-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6f357-622">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-623">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-624">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="6f357-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6f357-625">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6f357-626">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-628">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="6f357-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6f357-629">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="6f357-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6f357-630">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6f357-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6f357-631">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="6f357-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6f357-632">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6f357-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6f357-633">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="6f357-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-634">Az.Sql</span></span>
* <span data-ttu-id="6f357-635">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-636">Az.Storage</span></span>
* <span data-ttu-id="6f357-637">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="6f357-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6f357-638">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="6f357-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6f357-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f357-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6f357-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6f357-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6f357-641">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="6f357-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6f357-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6f357-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-643">Az.Websites</span></span>
* <span data-ttu-id="6f357-644">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="6f357-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6f357-645">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-646">Az.Accounts</span></span>
* <span data-ttu-id="6f357-647">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="6f357-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6f357-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6f357-649">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="6f357-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-650">Az.Automation</span></span>
* <span data-ttu-id="6f357-651">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-653">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-654">Az.Compute</span></span>
* <span data-ttu-id="6f357-655">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6f357-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f357-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6f357-657">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6f357-658">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="6f357-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-659">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-660">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6f357-661">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-662">Az.EventHub</span></span>
* <span data-ttu-id="6f357-663">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6f357-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6f357-664">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="6f357-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6f357-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-665">Az.KeyVault</span></span>
* <span data-ttu-id="6f357-666">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6f357-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6f357-667">Az.LogicApp</span></span>
* <span data-ttu-id="6f357-668">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="6f357-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6f357-669">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6f357-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6f357-670">Az.ManagedServices</span></span>
* <span data-ttu-id="6f357-671">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-672">Az.Network</span></span>
* <span data-ttu-id="6f357-673">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6f357-674">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-674">New cmdlets</span></span>
        - <span data-ttu-id="6f357-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f357-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6f357-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6f357-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6f357-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6f357-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6f357-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6f357-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6f357-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6f357-683">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6f357-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6f357-684">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6f357-685">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="6f357-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6f357-686">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="6f357-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6f357-687">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f357-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6f357-688">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="6f357-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6f357-689">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-689">Updated cmdlets</span></span>
        - <span data-ttu-id="6f357-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6f357-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6f357-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6f357-693">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6f357-694">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6f357-695">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f357-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="6f357-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6f357-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6f357-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6f357-699">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6f357-700">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6f357-701">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="6f357-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-703">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="6f357-704">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-706">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6f357-707">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6f357-708">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6f357-709">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6f357-710">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6f357-711">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6f357-712">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6f357-713">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6f357-714">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6f357-715">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-716">Az.Resources</span></span>
- <span data-ttu-id="6f357-717">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="6f357-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6f357-718">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-719">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-720">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6f357-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6f357-721">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="6f357-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-722">Az.Sql</span></span>
* <span data-ttu-id="6f357-723">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6f357-724">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6f357-725">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-726">Az.Storage</span></span>
* <span data-ttu-id="6f357-727">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="6f357-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6f357-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6f357-728">Az.StorageSync</span></span>
* <span data-ttu-id="6f357-729">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6f357-730">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-731">Az.Websites</span></span>
* <span data-ttu-id="6f357-732">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="6f357-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6f357-733">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6f357-734">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6f357-735">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-736">Az.Accounts</span></span>
* <span data-ttu-id="6f357-737">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6f357-738">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6f357-739">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="6f357-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6f357-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6f357-740">Az.Advisor</span></span>
* <span data-ttu-id="6f357-741">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6f357-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6f357-742">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f357-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6f357-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-743">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-744">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="6f357-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6f357-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6f357-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6f357-746">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6f357-747">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="6f357-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6f357-748">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="6f357-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6f357-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6f357-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6f357-750">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-751">Az.Automation</span></span>
* <span data-ttu-id="6f357-752">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-753">Az.Compute</span></span>
* <span data-ttu-id="6f357-754">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-755">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-756">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="6f357-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6f357-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6f357-757">Az.EventGrid</span></span>
* <span data-ttu-id="6f357-758">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-759">Az.IotHub</span></span>
* <span data-ttu-id="6f357-760">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-761">Az.Network</span></span>
* <span data-ttu-id="6f357-762">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6f357-763">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="6f357-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6f357-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="6f357-765">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="6f357-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6f357-766">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="6f357-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-768">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-770">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="6f357-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-771">Az.Resources</span></span>
    - <span data-ttu-id="6f357-772">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6f357-773">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6f357-774">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6f357-775">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-776">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-777">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="6f357-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-778">Az.Sql</span></span>
* <span data-ttu-id="6f357-779">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6f357-780">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6f357-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6f357-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6f357-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6f357-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6f357-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6f357-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6f357-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6f357-787">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-788">Az.Storage</span></span>
* <span data-ttu-id="6f357-789">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="6f357-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6f357-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6f357-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6f357-791">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="6f357-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6f357-792">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="6f357-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6f357-793">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6f357-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6f357-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6f357-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6f357-796">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="6f357-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6f357-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6f357-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6f357-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6f357-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6f357-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6f357-799">Az.StorageSync</span></span>
* <span data-ttu-id="6f357-800">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f357-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6f357-801">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-802">Az.Accounts</span></span>
* <span data-ttu-id="6f357-803">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="6f357-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6f357-804">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="6f357-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6f357-805">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6f357-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6f357-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6f357-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6f357-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-808">Az.Compute</span></span>
* <span data-ttu-id="6f357-809">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="6f357-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6f357-810">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6f357-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6f357-811">Az.Dns</span></span>
* <span data-ttu-id="6f357-812">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6f357-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6f357-813">Az.EventGrid</span></span>
* <span data-ttu-id="6f357-814">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6f357-815">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-815">New cmdlets:</span></span>
    - <span data-ttu-id="6f357-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6f357-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6f357-817">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="6f357-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6f357-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6f357-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6f357-819">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6f357-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6f357-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6f357-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6f357-821">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="6f357-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6f357-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6f357-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6f357-823">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="6f357-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6f357-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6f357-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6f357-825">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6f357-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6f357-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6f357-827">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="6f357-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6f357-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6f357-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6f357-829">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6f357-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="6f357-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="6f357-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6f357-831">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="6f357-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6f357-832">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="6f357-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6f357-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6f357-834">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6f357-835">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6f357-836">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="6f357-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6f357-837">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6f357-838">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="6f357-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6f357-839">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="6f357-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6f357-840">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6f357-841">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="6f357-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="6f357-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="6f357-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6f357-843">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6f357-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6f357-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6f357-845">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6f357-846">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="6f357-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6f357-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6f357-847">Az.FrontDoor</span></span>
* <span data-ttu-id="6f357-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6f357-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6f357-849">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6f357-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6f357-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6f357-851">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-852">Az.Network</span></span>
* <span data-ttu-id="6f357-853">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6f357-854">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-854">New cmdlets</span></span>
        - <span data-ttu-id="6f357-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6f357-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6f357-856">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6f357-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6f357-857">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-857">New cmdlets</span></span> 
        - <span data-ttu-id="6f357-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6f357-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6f357-859">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6f357-860">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-860">New cmdlets</span></span> 
        - <span data-ttu-id="6f357-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6f357-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="6f357-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6f357-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6f357-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6f357-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6f357-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6f357-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6f357-866">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6f357-867">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-867">New cmdlets</span></span>
        - <span data-ttu-id="6f357-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f357-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6f357-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f357-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6f357-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f357-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6f357-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6f357-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6f357-872">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="6f357-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6f357-873">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="6f357-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6f357-874">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="6f357-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6f357-875">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6f357-876">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6f357-877">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="6f357-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6f357-878">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6f357-879">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="6f357-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6f357-880">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6f357-881">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6f357-882">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="6f357-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6f357-883">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6f357-884">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6f357-885">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6f357-886">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="6f357-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6f357-887">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="6f357-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6f357-888">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="6f357-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6f357-889">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="6f357-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6f357-890">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="6f357-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="6f357-891">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="6f357-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="6f357-892">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6f357-893">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6f357-894">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-896">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="6f357-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-897">Az.Resources</span></span>
* <span data-ttu-id="6f357-898">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6f357-899">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6f357-900">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6f357-901">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="6f357-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-903">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="6f357-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-904">Az.Sql</span></span>
* <span data-ttu-id="6f357-905">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6f357-906">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6f357-907">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="6f357-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6f357-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f357-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6f357-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f357-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6f357-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f357-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6f357-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6f357-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6f357-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6f357-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-913">Az.Storage</span></span>
* <span data-ttu-id="6f357-914">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="6f357-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6f357-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="6f357-916">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="6f357-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6f357-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-918">Az.Websites</span></span>
* <span data-ttu-id="6f357-919">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="6f357-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6f357-920">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6f357-921">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6f357-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-922">Az.Cdn</span></span>
* <span data-ttu-id="6f357-923">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6f357-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-924">Az.Compute</span></span>
* <span data-ttu-id="6f357-925">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6f357-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6f357-926">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6f357-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-927">Az.EventHub</span></span>
* <span data-ttu-id="6f357-928">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="6f357-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6f357-929">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="6f357-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-930">Az.Network</span></span>
* <span data-ttu-id="6f357-931">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6f357-932">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6f357-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="6f357-934">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6f357-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-936">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-937">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-938">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="6f357-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-940">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6f357-941">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-942">Az.Sql</span></span>
* <span data-ttu-id="6f357-943">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="6f357-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6f357-944">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="6f357-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6f357-945">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="6f357-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6f357-946">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="6f357-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-947">Az.Websites</span></span>
* <span data-ttu-id="6f357-948">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6f357-949">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6f357-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-950">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-951">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="6f357-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6f357-952">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="6f357-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6f357-953">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="6f357-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6f357-954">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="6f357-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6f357-955">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="6f357-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6f357-956">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="6f357-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6f357-957">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="6f357-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6f357-958">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="6f357-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6f357-959">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="6f357-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6f357-960">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="6f357-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6f357-961">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="6f357-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6f357-962">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="6f357-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6f357-963">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="6f357-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6f357-964">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="6f357-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6f357-965">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="6f357-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6f357-966">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="6f357-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6f357-967">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="6f357-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6f357-968">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="6f357-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6f357-969">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="6f357-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="6f357-970">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="6f357-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6f357-971">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="6f357-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6f357-972">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="6f357-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6f357-973">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="6f357-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6f357-974">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="6f357-975">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6f357-976">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6f357-977">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="6f357-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6f357-978">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6f357-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6f357-979">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6f357-980">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="6f357-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6f357-981">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="6f357-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="6f357-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6f357-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6f357-983">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6f357-984">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6f357-985">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="6f357-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6f357-986">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="6f357-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6f357-987">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="6f357-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6f357-988">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="6f357-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6f357-989">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="6f357-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6f357-990">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="6f357-991">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="6f357-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6f357-992">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="6f357-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6f357-993">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="6f357-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6f357-994">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="6f357-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6f357-995">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6f357-996">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="6f357-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6f357-997">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="6f357-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="6f357-998">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="6f357-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="6f357-999">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6f357-1000">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="6f357-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6f357-1001">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="6f357-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6f357-1002">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="6f357-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6f357-1003">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="6f357-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6f357-1004">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6f357-1005">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="6f357-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6f357-1006">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="6f357-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6f357-1007">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6f357-1008">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="6f357-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6f357-1009">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="6f357-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6f357-1010">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6f357-1011">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6f357-1012">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="6f357-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6f357-1013">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="6f357-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6f357-1014">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6f357-1015">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="6f357-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6f357-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6f357-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6f357-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6f357-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6f357-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6f357-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6f357-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6f357-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6f357-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6f357-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6f357-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6f357-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6f357-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6f357-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6f357-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6f357-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6f357-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6f357-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6f357-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6f357-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="6f357-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6f357-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6f357-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6f357-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1028">Az.Automation</span></span>
* <span data-ttu-id="6f357-1029">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6f357-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6f357-1030">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="6f357-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6f357-1031">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="6f357-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6f357-1032">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="6f357-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6f357-1033">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="6f357-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6f357-1034">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="6f357-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6f357-1035">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="6f357-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1036">Az.Compute</span></span>
* <span data-ttu-id="6f357-1037">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6f357-1038">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1040">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="6f357-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-1041">Az.Monitor</span></span>
* <span data-ttu-id="6f357-1042">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="6f357-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1043">Az.Network</span></span>
* <span data-ttu-id="6f357-1044">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6f357-1045">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6f357-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="6f357-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6f357-1047">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f357-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1048">Az.Resources</span></span>
* <span data-ttu-id="6f357-1049">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1050">Az.Sql</span></span>
* <span data-ttu-id="6f357-1051">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="6f357-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6f357-1052">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1053">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1054">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="6f357-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-1056">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="6f357-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6f357-1057">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="6f357-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1058">Az.Compute</span></span>
* <span data-ttu-id="6f357-1059">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="6f357-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6f357-1060">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6f357-1061">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6f357-1062">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6f357-1063">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f357-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6f357-1064">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="6f357-1065">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="6f357-1065">Breaking changes</span></span>
    - <span data-ttu-id="6f357-1066">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6f357-1067">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6f357-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6f357-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="6f357-1069">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6f357-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6f357-1070">Az.Dns</span></span>
* <span data-ttu-id="6f357-1071">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="6f357-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6f357-1072">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f357-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6f357-1073">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6f357-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6f357-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="6f357-1075">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6f357-1076">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="6f357-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6f357-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6f357-1077">Az.HDInsight</span></span>
* <span data-ttu-id="6f357-1078">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="6f357-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6f357-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f357-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6f357-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6f357-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6f357-1081">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="6f357-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6f357-1082">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="6f357-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6f357-1083">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6f357-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6f357-1084">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="6f357-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-1085">Az.Monitor</span></span>
* <span data-ttu-id="6f357-1086">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="6f357-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="6f357-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6f357-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6f357-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6f357-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6f357-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6f357-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6f357-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6f357-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6f357-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6f357-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6f357-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6f357-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6f357-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6f357-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6f357-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6f357-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6f357-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6f357-1098">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="6f357-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6f357-1099">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="6f357-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1100">Az.Network</span></span>
* <span data-ttu-id="6f357-1101">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6f357-1102">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-1102">New cmdlets</span></span>
        - <span data-ttu-id="6f357-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6f357-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="6f357-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6f357-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6f357-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6f357-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6f357-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6f357-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6f357-1107">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="6f357-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6f357-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6f357-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6f357-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6f357-1110">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6f357-1111">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="6f357-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6f357-1112">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="6f357-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6f357-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="6f357-1114">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="6f357-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6f357-1115">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6f357-1116">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="6f357-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-1118">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="6f357-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6f357-1119">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="6f357-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6f357-1120">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="6f357-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6f357-1121">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="6f357-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6f357-1122">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="6f357-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6f357-1123">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="6f357-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6f357-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6f357-1124">Az.Relay</span></span>
* <span data-ttu-id="6f357-1125">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="6f357-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-1127">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1128">Az.Storage</span></span>
* <span data-ttu-id="6f357-1129">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="6f357-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="6f357-1130">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="6f357-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6f357-1131">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6f357-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="6f357-1133">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="6f357-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6f357-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6f357-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6f357-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1137">Az.Websites</span></span>
* <span data-ttu-id="6f357-1138">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6f357-1139">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6f357-1140">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6f357-1141">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="6f357-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="6f357-1142">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="6f357-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="6f357-1143">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="6f357-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6f357-1144">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="6f357-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6f357-1145">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6f357-1146">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6f357-1147">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6f357-1148">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6f357-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1149">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1150">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="6f357-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6f357-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f357-1151">Az.Batch</span></span>
* <span data-ttu-id="6f357-1152">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6f357-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-1153">Az.Cdn</span></span>
* <span data-ttu-id="6f357-1154">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-1156">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1157">Az.Compute</span></span>
* <span data-ttu-id="6f357-1158">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="6f357-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6f357-1159">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1160">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-1161">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-1162">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="6f357-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1164">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6f357-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6f357-1165">Az.EventGrid</span></span>
* <span data-ttu-id="6f357-1166">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f357-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-1167">Az.EventHub</span></span>
* <span data-ttu-id="6f357-1168">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="6f357-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6f357-1169">Az.HDInsight</span></span>
* <span data-ttu-id="6f357-1170">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-1171">Az.IotHub</span></span>
* <span data-ttu-id="6f357-1172">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6f357-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-1173">Az.KeyVault</span></span>
* <span data-ttu-id="6f357-1174">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1175">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6f357-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6f357-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="6f357-1177">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6f357-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6f357-1178">Az.Media</span></span>
* <span data-ttu-id="6f357-1179">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-1180">Az.Monitor</span></span>
  * <span data-ttu-id="6f357-1181">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="6f357-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6f357-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6f357-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6f357-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6f357-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6f357-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6f357-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6f357-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6f357-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6f357-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6f357-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6f357-1187">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1188">Az.Network</span></span>
* <span data-ttu-id="6f357-1189">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1190">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6f357-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6f357-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="6f357-1192">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-1194">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6f357-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6f357-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6f357-1196">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-1198">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1199">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6f357-1200">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6f357-1201">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6f357-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6f357-1202">Az.RedisCache</span></span>
* <span data-ttu-id="6f357-1203">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1204">Az.Resources</span></span>
* <span data-ttu-id="6f357-1205">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1206">Az.Sql</span></span>
* <span data-ttu-id="6f357-1207">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="6f357-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6f357-1208">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1209">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="6f357-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6f357-1210">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6f357-1211">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="6f357-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6f357-1212">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="6f357-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6f357-1213">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1214">Az.Websites</span></span>
* <span data-ttu-id="6f357-1215">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="6f357-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6f357-1216">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6f357-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6f357-1217">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6f357-1218">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6f357-1219">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6f357-1220">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="6f357-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="6f357-1221">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="6f357-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="6f357-1222">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="6f357-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6f357-1223">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="6f357-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6f357-1224">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6f357-1225">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6f357-1226">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6f357-1227">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6f357-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1228">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1229">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="6f357-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6f357-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="6f357-1231">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6f357-1232">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1233">Az.Automation</span></span>
* <span data-ttu-id="6f357-1234">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="6f357-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6f357-1235">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="6f357-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6f357-1236">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="6f357-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1237">Az.Compute</span></span>
* <span data-ttu-id="6f357-1238">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6f357-1239">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="6f357-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="6f357-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="6f357-1241">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="6f357-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-1242">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-1243">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6f357-1244">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1245">Az.Resources</span></span>
* <span data-ttu-id="6f357-1246">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="6f357-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6f357-1247">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="6f357-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6f357-1248">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="6f357-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6f357-1249">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6f357-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6f357-1250">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="6f357-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6f357-1251">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6f357-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1252">Az.Sql</span></span>
* <span data-ttu-id="6f357-1253">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="6f357-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1254">Az.Storage</span></span>
* <span data-ttu-id="6f357-1255">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="6f357-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6f357-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f357-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="6f357-1257">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="6f357-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6f357-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6f357-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6f357-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6f357-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6f357-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6f357-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6f357-1262">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="6f357-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6f357-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f357-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6f357-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f357-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6f357-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6f357-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6f357-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6f357-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6f357-1267">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6f357-1268">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="6f357-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="6f357-1269">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="6f357-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="6f357-1270">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="6f357-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6f357-1271">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="6f357-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6f357-1272">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6f357-1273">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6f357-1274">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6f357-1275">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1276">Az.Automation</span></span>
* <span data-ttu-id="6f357-1277">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="6f357-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6f357-1278">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="6f357-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="6f357-1279">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="6f357-1279">Pre-Post script</span></span>
    * <span data-ttu-id="6f357-1280">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="6f357-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1281">Az.Compute</span></span>
* <span data-ttu-id="6f357-1282">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6f357-1283">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6f357-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-1284">Az.KeyVault</span></span>
* <span data-ttu-id="6f357-1285">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1286">Az.Network</span></span>
* <span data-ttu-id="6f357-1287">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6f357-1288">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-1290">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="6f357-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6f357-1291">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1292">Az.Resources</span></span>
* <span data-ttu-id="6f357-1293">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6f357-1294">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6f357-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1295">Az.Sql</span></span>
* <span data-ttu-id="6f357-1296">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6f357-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1297">Az.Storage</span></span>
* <span data-ttu-id="6f357-1298">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6f357-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6f357-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6f357-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6f357-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6f357-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6f357-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6f357-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6f357-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6f357-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1305">Az.Websites</span></span>
* <span data-ttu-id="6f357-1306">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="6f357-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="6f357-1307">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1308">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1309">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6f357-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6f357-1310">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1311">Az.Automation</span></span>
* <span data-ttu-id="6f357-1312">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="6f357-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6f357-1313">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6f357-1314">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f357-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6f357-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-1315">Az.Cdn</span></span>
* <span data-ttu-id="6f357-1316">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="6f357-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1317">Az.Compute</span></span>
* <span data-ttu-id="6f357-1318">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-1319">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-1320">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6f357-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6f357-1321">Az.LogicApp</span></span>
* <span data-ttu-id="6f357-1322">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6f357-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1323">Az.Network</span></span>
* <span data-ttu-id="6f357-1324">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-1326">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="6f357-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6f357-1327">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="6f357-1327">SDK Update</span></span>
* <span data-ttu-id="6f357-1328">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6f357-1329">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1330">Az.Resources</span></span>
* <span data-ttu-id="6f357-1331">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6f357-1332">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6f357-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6f357-1333">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6f357-1334">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6f357-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6f357-1335">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6f357-1336">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6f357-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1337">Az.Sql</span></span>
* <span data-ttu-id="6f357-1338">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6f357-1339">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1340">Az.Storage</span></span>
* <span data-ttu-id="6f357-1341">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f357-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6f357-1342">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6f357-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="6f357-1344">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1345">Az.Automation</span></span>
* <span data-ttu-id="6f357-1346">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6f357-1347">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6f357-1348">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="6f357-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-1350">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1351">Az.Compute</span></span>
* <span data-ttu-id="6f357-1352">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6f357-1353">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="6f357-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6f357-1354">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6f357-1355">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="6f357-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1357">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6f357-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6f357-1358">Az.EventHub</span></span>
* <span data-ttu-id="6f357-1359">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="6f357-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-1360">Az.KeyVault</span></span>
* <span data-ttu-id="6f357-1361">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6f357-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6f357-1362">Az.LogicApp</span></span>
* <span data-ttu-id="6f357-1363">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6f357-1364">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6f357-1365">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="6f357-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6f357-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6f357-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6f357-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6f357-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6f357-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6f357-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6f357-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6f357-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6f357-1370">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6f357-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6f357-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6f357-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6f357-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6f357-1375">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6f357-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-1376">Az.Monitor</span></span>
* <span data-ttu-id="6f357-1377">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1378">Az.Network</span></span>
* <span data-ttu-id="6f357-1379">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="6f357-1381">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6f357-1382">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="6f357-1383">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="6f357-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="6f357-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1384">Az.Resources</span></span>
* <span data-ttu-id="6f357-1385">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6f357-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6f357-1386">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6f357-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6f357-1387">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="6f357-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6f357-1388">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="6f357-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1389">Az.Sql</span></span>
* <span data-ttu-id="6f357-1390">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6f357-1391">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="6f357-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1392">Az.Websites</span></span>
* <span data-ttu-id="6f357-1393">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6f357-1394">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1395">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1396">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="6f357-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6f357-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="6f357-1398">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="6f357-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1399">Az.Compute</span></span>
* <span data-ttu-id="6f357-1400">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6f357-1401">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6f357-1402">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="6f357-1404">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="6f357-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1405">Az.Resources</span></span>
* <span data-ttu-id="6f357-1406">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="6f357-1407">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6f357-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6f357-1408">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="6f357-1409">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6f357-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1410">Az.Sql</span></span>
* <span data-ttu-id="6f357-1411">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6f357-1412">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="6f357-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6f357-1413">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6f357-1414">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1415">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1416">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="6f357-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6f357-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="6f357-1418">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="6f357-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="6f357-1420">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="6f357-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6f357-1421">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1422">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1423">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6f357-1424">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6f357-1425">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6f357-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6f357-1426">Az.Aks</span></span>
* <span data-ttu-id="6f357-1427">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6f357-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1428">Az.Automation</span></span>
* <span data-ttu-id="6f357-1429">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6f357-1430">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6f357-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6f357-1431">Az.Cdn</span></span>
* <span data-ttu-id="6f357-1432">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1433">Az.Compute</span></span>
* <span data-ttu-id="6f357-1434">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6f357-1435">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6f357-1436">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6f357-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6f357-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6f357-1438">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6f357-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6f357-1439">Az.DataFactory</span></span>
* <span data-ttu-id="6f357-1440">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1442">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6f357-1443">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6f357-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6f357-1444">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-1445">Az.IotHub</span></span>
* <span data-ttu-id="6f357-1446">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6f357-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-1447">Az.KeyVault</span></span>
* <span data-ttu-id="6f357-1448">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1449">Az.Network</span></span>
* <span data-ttu-id="6f357-1450">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1451">Az.Resources</span></span>
* <span data-ttu-id="6f357-1452">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6f357-1453">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="6f357-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6f357-1454">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="6f357-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6f357-1455">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="6f357-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6f357-1456">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="6f357-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6f357-1457">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6f357-1458">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6f357-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-1460">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6f357-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6f357-1461">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1461">Fix some error messages.</span></span>
* <span data-ttu-id="6f357-1462">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="6f357-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6f357-1463">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6f357-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6f357-1464">Az.SignalR</span></span>
* <span data-ttu-id="6f357-1465">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1466">Az.Sql</span></span>
* <span data-ttu-id="6f357-1467">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6f357-1468">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6f357-1469">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="6f357-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6f357-1470">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="6f357-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1471">Az.Storage</span></span>
* <span data-ttu-id="6f357-1472">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6f357-1473">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6f357-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6f357-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6f357-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6f357-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6f357-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6f357-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="6f357-1477">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1478">Az.Websites</span></span>
* <span data-ttu-id="6f357-1479">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6f357-1480">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6f357-1481">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6f357-1482">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="6f357-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6f357-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1483">Az.Accounts</span></span>
* <span data-ttu-id="6f357-1484">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1485">Az.Compute</span></span>
* <span data-ttu-id="6f357-1486">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="6f357-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6f357-1487">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6f357-1488">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1490">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="6f357-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6f357-1491">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6f357-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6f357-1492">Az.EventGrid</span></span>
* <span data-ttu-id="6f357-1493">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6f357-1494">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6f357-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6f357-1495">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6f357-1496">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6f357-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6f357-1497">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6f357-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6f357-1498">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6f357-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6f357-1499">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="6f357-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6f357-1500">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6f357-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6f357-1501">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="6f357-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6f357-1502">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="6f357-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="6f357-1503">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6f357-1504">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="6f357-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6f357-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6f357-1505">Az.IotHub</span></span>
* <span data-ttu-id="6f357-1506">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6f357-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6f357-1507">Az.LogicApp</span></span>
* <span data-ttu-id="6f357-1508">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="6f357-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1509">Az.Resources</span></span>
* <span data-ttu-id="6f357-1510">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6f357-1511">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6f357-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6f357-1512">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6f357-1513">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6f357-1514">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="6f357-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6f357-1515">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6f357-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6f357-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6f357-1516">Az.SignalR</span></span>
* <span data-ttu-id="6f357-1517">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1518">Az.Sql</span></span>
* <span data-ttu-id="6f357-1519">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6f357-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1520">Az.Storage</span></span>
* <span data-ttu-id="6f357-1521">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6f357-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f357-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="6f357-1523">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="6f357-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6f357-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6f357-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1525">Az.Websites</span></span>
* <span data-ttu-id="6f357-1526">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6f357-1527">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6f357-1528">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6f357-1529">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-1529">General</span></span>

- <span data-ttu-id="6f357-1530">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="6f357-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="6f357-1531">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="6f357-1531">Online help for each module</span></span>
- <span data-ttu-id="6f357-1532">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="6f357-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6f357-1533">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6f357-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6f357-1534">Az.Accounts</span></span>
- <span data-ttu-id="6f357-1535">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6f357-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="6f357-1536">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="6f357-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6f357-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="6f357-1538">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="6f357-1538">Fixes for #7002</span></span>
- <span data-ttu-id="6f357-1539">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6f357-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6f357-1540">Az.Batch</span></span>
- <span data-ttu-id="6f357-1541">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6f357-1542">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="6f357-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6f357-1543">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6f357-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6f357-1544">Az.Billing</span></span>
- <span data-ttu-id="6f357-1545">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6f357-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="6f357-1547">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6f357-1548">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6f357-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="6f357-1550">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6f357-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6f357-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6f357-1552">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="6f357-1554">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6f357-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6f357-1555">Az.Monitor</span></span>
- <span data-ttu-id="6f357-1556">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6f357-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f357-1557">Az.KeyVault</span></span>
- <span data-ttu-id="6f357-1558">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6f357-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6f357-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="6f357-1560">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="6f357-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6f357-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6f357-1561">Az.Media</span></span>
- <span data-ttu-id="6f357-1562">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="6f357-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6f357-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1563">Az.Network</span></span>
<span data-ttu-id="6f357-1564">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6f357-1565">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="6f357-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6f357-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6f357-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6f357-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f357-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6f357-1574">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6f357-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f357-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6f357-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6f357-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6f357-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6f357-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6f357-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6f357-1580">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6f357-1581">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6f357-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6f357-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6f357-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6f357-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6f357-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6f357-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6f357-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6f357-1585">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6f357-1586">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6f357-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="6f357-1588">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6f357-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6f357-1589">Az.Profile</span></span>
- <span data-ttu-id="6f357-1590">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="6f357-1592">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6f357-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1593">Az.Resources</span></span>
- <span data-ttu-id="6f357-1594">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6f357-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="6f357-1596">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="6f357-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6f357-1597">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6f357-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6f357-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="6f357-1599">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6f357-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6f357-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1600">Az.Sql</span></span>
- <span data-ttu-id="6f357-1601">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6f357-1602">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6f357-1603">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6f357-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1604">Az.Storage</span></span>
- <span data-ttu-id="6f357-1605">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6f357-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1606">Az.Websites</span></span>
- <span data-ttu-id="6f357-1607">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="6f357-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6f357-1608">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6f357-1609">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-1609">General</span></span>

* <span data-ttu-id="6f357-1610">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="6f357-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6f357-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1611">Az.Compute</span></span>

* <span data-ttu-id="6f357-1612">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="6f357-1614">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6f357-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6f357-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="6f357-1616">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="6f357-1617">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6f357-1618">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6f357-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="6f357-1620">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6f357-1621">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="6f357-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6f357-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1622">Az.Resources</span></span>

* <span data-ttu-id="6f357-1623">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6f357-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6f357-1624">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f357-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6f357-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1625">Az.Sql</span></span>

* <span data-ttu-id="6f357-1626">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="6f357-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6f357-1627">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6f357-1628">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6f357-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1629">Az.Storage</span></span>

* <span data-ttu-id="6f357-1630">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6f357-1631">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6f357-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6f357-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6f357-1633">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="6f357-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6f357-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6f357-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6f357-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6f357-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1636">Az.Websites</span></span>

* <span data-ttu-id="6f357-1637">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6f357-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="6f357-1638">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f357-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6f357-1639">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="6f357-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6f357-1640">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6f357-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6f357-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="6f357-1642">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6f357-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6f357-1643">Az.Automation</span></span>
* <span data-ttu-id="6f357-1644">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6f357-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6f357-1645">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6f357-1646">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6f357-1647">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6f357-1648">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6f357-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1649">Az.Compute</span></span>
* <span data-ttu-id="6f357-1650">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6f357-1651">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6f357-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="6f357-1653">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6f357-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6f357-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6f357-1655">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6f357-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1656">Az.Network</span></span>
* <span data-ttu-id="6f357-1657">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6f357-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6f357-1658">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6f357-1659">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="6f357-1660">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6f357-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6f357-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6f357-1662">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6f357-1663">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="6f357-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6f357-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6f357-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6f357-1665">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="6f357-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6f357-1666">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6f357-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6f357-1667">Az.Relay</span></span>
* <span data-ttu-id="6f357-1668">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="6f357-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6f357-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1669">Az.Resources</span></span>
* <span data-ttu-id="6f357-1670">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6f357-1671">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="6f357-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6f357-1672">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="6f357-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6f357-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-1674">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6f357-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1675">Az.Sql</span></span>
* <span data-ttu-id="6f357-1676">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6f357-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6f357-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6f357-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6f357-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6f357-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6f357-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6f357-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6f357-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6f357-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6f357-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6f357-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6f357-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6f357-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6f357-1685">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="6f357-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6f357-1686">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="6f357-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6f357-1687">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f357-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6f357-1688">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="6f357-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6f357-1689">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="6f357-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6f357-1690">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="6f357-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6f357-1691">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="6f357-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6f357-1692">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6f357-1693">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6f357-1694">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6f357-1694">General</span></span>
* <span data-ttu-id="6f357-1695">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="6f357-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6f357-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6f357-1696">Az.Profile</span></span>
* <span data-ttu-id="6f357-1697">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6f357-1698">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6f357-1699">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6f357-1700">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6f357-1701">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6f357-1702">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6f357-1703">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="6f357-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-1705">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1706">Az.Compute</span></span>
* <span data-ttu-id="6f357-1707">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6f357-1708">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="6f357-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6f357-1709">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="6f357-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1711">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="6f357-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6f357-1712">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6f357-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6f357-1713">Az.Insights</span></span>
* <span data-ttu-id="6f357-1714">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="6f357-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6f357-1715">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="6f357-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6f357-1716">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="6f357-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6f357-1717">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1718">Az.Network</span></span>
* <span data-ttu-id="6f357-1719">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6f357-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6f357-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6f357-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6f357-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6f357-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6f357-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6f357-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6f357-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6f357-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6f357-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6f357-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6f357-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6f357-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6f357-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="6f357-1727">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1728">Az.Resources</span></span>
* <span data-ttu-id="6f357-1729">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6f357-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6f357-1730">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="6f357-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6f357-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6f357-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="6f357-1732">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="6f357-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6f357-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6f357-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="6f357-1734">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6f357-1735">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="6f357-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6f357-1736">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="6f357-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6f357-1737">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="6f357-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6f357-1738">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6f357-1739">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6f357-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6f357-1740">Az.Profile</span></span>
* <span data-ttu-id="6f357-1741">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6f357-1742">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1743">Az.Compute</span></span>
* <span data-ttu-id="6f357-1744">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="6f357-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6f357-1745">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6f357-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6f357-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="6f357-1747">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6f357-1748">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6f357-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6f357-1749">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f357-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6f357-1750">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="6f357-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6f357-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="6f357-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1752">Az.Network</span></span>
* <span data-ttu-id="6f357-1753">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="6f357-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6f357-1754">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1755">Az.Resources</span></span>
* <span data-ttu-id="6f357-1756">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f357-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6f357-1757">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6f357-1758">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6f357-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6f357-1759">Azure.Storage</span></span>
* <span data-ttu-id="6f357-1760">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="6f357-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6f357-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6f357-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6f357-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6f357-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6f357-1763">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="6f357-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6f357-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6f357-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="6f357-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6f357-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="6f357-1766">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6f357-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6f357-1767">Az.Compute</span></span>
* <span data-ttu-id="6f357-1768">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="6f357-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6f357-1769">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6f357-1770">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="6f357-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6f357-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6f357-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6f357-1772">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6f357-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6f357-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6f357-1773">Az.Network</span></span>
* <span data-ttu-id="6f357-1774">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f357-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6f357-1775">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1775">new cmdlets added</span></span>
    - <span data-ttu-id="6f357-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6f357-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6f357-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6f357-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6f357-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6f357-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6f357-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6f357-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6f357-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6f357-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6f357-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6f357-1782">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6f357-1783">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6f357-1784">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6f357-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6f357-1785">Az.RedisCache</span></span>
* <span data-ttu-id="6f357-1786">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="6f357-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6f357-1787">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6f357-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6f357-1788">Az.Resources</span></span>
* <span data-ttu-id="6f357-1789">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="6f357-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6f357-1790">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="6f357-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6f357-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6f357-1791">Az.Sql</span></span>
* <span data-ttu-id="6f357-1792">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="6f357-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6f357-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6f357-1793">Az.Websites</span></span>
* <span data-ttu-id="6f357-1794">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="6f357-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6f357-1795">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="6f357-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6f357-1796">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="6f357-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6f357-1797">Erste Version</span><span class="sxs-lookup"><span data-stu-id="6f357-1797">Initial Release</span></span>
