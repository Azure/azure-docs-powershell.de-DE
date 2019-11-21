---
title: Versionshinweise zu Azure PowerShell
description: Hier erfahren Sie mehr über die aktuellen Updates für die Azure PowerShell-Module.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062138"
---
## <a name="300---november-2019"></a><span data-ttu-id="bbd58-103">3.0.0 – November 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="bbd58-104">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-104">General</span></span>
* <span data-ttu-id="bbd58-105">Az.PrivateDns 1.0.0 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="bbd58-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bbd58-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-106">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-107">Hinweis zur Veraltung des Alias „Resolve-Error“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bbd58-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bbd58-108">Az.Advisor</span></span>
* <span data-ttu-id="bbd58-109">Neue Kategorie „Operational Excellence“ für Cmdlet „Get-AzAdvisorRecommendation“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bbd58-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bbd58-110">Az.Batch</span></span>
* <span data-ttu-id="bbd58-111">`CoreQuota` für `BatchAccountContext` in `DedicatedCoreQuota` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="bbd58-112">Außerdem wurde das neue Element `LowPriorityCoreQuota` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="bbd58-113">Dies wirkt sich auf **Get-AzBatchAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="bbd58-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="bbd58-114">Für den Parameter `-ResourceFile` von **New-AzBatchTask** wird jetzt eine Sammlung mit `PSResourceFile`-Objekten verwendet, und für die Erstellung kann das Cmdlet **New-AzBatchResourceFile** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="bbd58-115">Neues Cmdlet **New-AzBatchResourceFile** als Hilfe für die Erstellung von `PSResourceFile`-Objekten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="bbd58-116">Diese können für **New-AzBatchTask** über den Parameter `-ResourceFile` bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="bbd58-117">Hierbei werden zusätzlich zum Ansatz mit `HttpUrl` zwei neue Arten von Ressourcendateien unterstützt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="bbd58-118">Mit Ressourcendateien, die auf `AutoStorageContainerName` basieren, wird ein gesamter Container für die automatische Speicherung auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="bbd58-119">Für Ressourcendateien, die auf `StorageContainerUrl` basieren, wird der in der URL angegebene Container auf den Batch-Knoten heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="bbd58-120">`ApplicationPackages`-Eigenschaft von `PSApplication` entfernt, die von **Get-AzBatchApplication** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bbd58-121">Die spezifischen Pakete in einer Anwendung können jetzt mit **Get-AzBatchApplicationPackage** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="bbd58-122">Beispiel: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="bbd58-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="bbd58-123">`ApplicationId` für **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** und **Set-AzBatchApplication** in `ApplicationName` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="bbd58-124">`ApplicationId` ist jetzt ein Alias von `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="bbd58-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="bbd58-125">Neue `PSWindowsUserConfiguration`-Eigenschaft zu `PSUserAccount` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="bbd58-126">`Version` für `PSApplicationPackage` in `Name` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="bbd58-127">`BlobSource` für `PSResourceFile` in `HttpUrl` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="bbd58-128">`OSDisk`-Eigenschaft aus `PSVirtualMachineConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="bbd58-129">**Set-AzBatchPoolOSVersion** entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="bbd58-130">Dieser Vorgang wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="bbd58-131">`TargetOSVersion` aus `PSCloudServiceConfiguration` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bbd58-132">`CurrentOSVersion` für `PSCloudServiceConfiguration` in `OSVersion` umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="bbd58-133">`DataEgressGiB` und `DataIngressGiB` aus `PSPoolUsageMetrics` entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="bbd58-134">**Get-AzBatchNodeAgentSku** entfernt und durch **Get-AzBatchSupportedImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="bbd58-135">**Get-AzBatchSupportedImage** gibt die gleichen Daten wie **Get-AzBatchNodeAgentSku** zurück, aber in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="bbd58-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="bbd58-136">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbd58-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="bbd58-137">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="bbd58-138">Möglichkeit zum Bereitstellen von Remotedateisystemen auf jedem Knoten eines Pools über den neuen Parameter `MountConfiguration` von **New-AzBatchPool** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="bbd58-139">Es ist jetzt Unterstützung für Sicherheitsregeln vorhanden, die den Netzwerkzugriff auf einen Pool basierend auf dem Quellport des Datenverkehrs blockieren.</span><span class="sxs-lookup"><span data-stu-id="bbd58-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="bbd58-140">Dies erfolgt über die `SourcePortRanges`-Eigenschaft unter `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="bbd58-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="bbd58-141">Bei der Ausführung eines Containers unterstützt Batch jetzt die Ausführung der Aufgabe im Arbeitsverzeichnis des Containers bzw. im Arbeitsverzeichnis der Batch-Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="bbd58-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="bbd58-142">Dies wird mit der `WorkingDirectory`-Eigenschaft unter `PSTaskContainerSettings` gesteuert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="bbd58-143">Möglichkeit zum Angeben einer Sammlung mit öffentlichen IP-Adressen für `PSNetworkConfiguration` über die neue `PublicIPs`-Eigenschaft hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="bbd58-144">So wird sichergestellt, dass Knoten im Pool über eine IP-Adresse aus der Liste mit den von Benutzern bereitgestellten IP-Adressen verfügen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="bbd58-145">Wenn kein Wert angegeben wird, lautet der Standardwert von `WaitForSuccess` unter `PSSTartTask` jetzt `$True` (bisher `$False`).</span><span class="sxs-lookup"><span data-stu-id="bbd58-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="bbd58-146">Wenn kein Wert angegeben wird, lautet der Standardwert von `Scope` unter `PSAutoUserSpecification` jetzt `Pool` (bisher `Task` unter Windows und `Pool` unter Linux).</span><span class="sxs-lookup"><span data-stu-id="bbd58-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bbd58-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-147">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-148">„UrlRewriteAction“ und „CacheKeyQueryStringAction“ für „RulesEngine“ eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="bbd58-149">Mehrere Fehler behoben, z. B. fehlende „Selector“-Eingabe im Cmdlet „New-AzDeliveryRuleCondition“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-150">Az.Compute</span></span>
* <span data-ttu-id="bbd58-151">Feature „Datenträgerverschlüsselungssatz“</span><span class="sxs-lookup"><span data-stu-id="bbd58-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="bbd58-152">Neue Cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="bbd58-153">Parameter „DiskEncryptionSetId“ wurde den folgenden Cmdlets hinzugefügt: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="bbd58-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bbd58-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="bbd58-155">Die Parameter „DiskEncryptionSetId“ und „EncryptionType“ wurden den folgenden Cmdlets hinzugefügt:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bbd58-156">Parameter „PublicIPAddressVersion“ wurde „New-AzVmssIPConfig“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="bbd58-157">„FileUris“ für benutzerdefinierte Skripterweiterung von öffentlicher Einstellung auf geschützte Einstellung umgestellt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="bbd58-158">„ScaleInPolicy“ wurde den Cmdlets „New-AzVmss“, „New-AzVmssConfig“ und „Update-AzVmss hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="bbd58-159">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="bbd58-159">Breaking changes</span></span>
    - <span data-ttu-id="bbd58-160">Parameter „UploadSizeInBytes“ wird anstelle von „DiskSizeGB“ für „New-AzDiskConfig“ verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bbd58-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="bbd58-161">Im „GalleryImageVersion“-Objekt wurde „objectPublishingProfile.Source.ManagedImage.Id“ durch „StorageProfile.Source.Id“ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-162">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-163">Version des ADF .NET SDK auf 4.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-165">Update für ADLS SDK-Version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) mit den folgenden Fehlerbehebungen durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="bbd58-166">Vermeidung der Auslösung einer Ausnahme, während die Deserialisierung des „creationtime“-Elements des Papierkorb- oder Verzeichniseintrags nicht durchgeführt werden kann</span><span class="sxs-lookup"><span data-stu-id="bbd58-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="bbd58-167">Verfügbarmachung der Einstellung pro Anforderungszeitlimit in „adlsclient“</span><span class="sxs-lookup"><span data-stu-id="bbd58-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="bbd58-168">Fehlerbehebung für Übergabe des ursprünglichen „syncflag“-Elements für badoffset-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="bbd58-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="bbd58-169">Fehlerbehebung für „EnumerateDirectory“ zum Abrufen des Fortsetzungstokens nach der Überprüfung der Antwort</span><span class="sxs-lookup"><span data-stu-id="bbd58-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="bbd58-170">Behebung eines Verkettungsfehlers</span><span class="sxs-lookup"><span data-stu-id="bbd58-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bbd58-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bbd58-171">Az.FrontDoor</span></span>
* <span data-ttu-id="bbd58-172">Verschiedene Tippfehler im Modul korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bbd58-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bbd58-173">Az.HDInsight</span></span>
* <span data-ttu-id="bbd58-174">Fehler behoben, bei dem Kunden die Meldung „Keine gültige Base64-Zeichenfolge“ erhalten haben, wenn sie „Get-AzHDInsightCluster“ zum Abrufen des Clusters mit ADLSGen1-Speicher verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="bbd58-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="bbd58-175">Parameter mit dem Namen „ApplicationId“ den drei Cmdlets „Add-AzHDInsightClusterIdentity“, „New-AzHDInsightClusterConfig“ und „New-AzHDInsightCluster“ hinzugefügt, damit der Kunde die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="bbd58-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="bbd58-176">Microsoft.Azure.Management.HDInsight von 2.1.0 in 5.1.0 geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="bbd58-177">Fünf Cmdlets wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="bbd58-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bbd58-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bbd58-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bbd58-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bbd58-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="bbd58-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="bbd58-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bbd58-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="bbd58-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bbd58-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="bbd58-183">Drei Cmdlets wurden hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="bbd58-184">„Get-AzHDInsightMonitoring“ als Ersatz für „Get-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bbd58-185">„Enable-AzHDInsightMonitoring“ als Ersatz für „Enable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="bbd58-186">„Disable-AzHDInsightMonitoring“ als Ersatz für „Disable-AzHDInsightOMS“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="bbd58-187">Fehler für Cmdlet „Get-AzHDInsightProperties“ behoben, um Unterstützung für das Abrufen von Funktionsinformationen von einem bestimmten Ort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="bbd58-188">Parametersätze („Spark1“, „Spark2“) aus „Add-AzHDInsightConfigValue“ entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="bbd58-189">Beispiele den Hilfedokumenten des Cmdlets „Add-AzHDInsightSecurityProfile“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="bbd58-190">Der Ausgabetyp der folgenden Cmdlets wurde geändert:</span><span class="sxs-lookup"><span data-stu-id="bbd58-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="bbd58-191">Ausgabetyp für „Get-AzHDInsightProperties“ von „CapabilitiesResponse“ in „AzureHDInsightCapabilities“ geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="bbd58-192">Ausgabetyp für „Remove-AzHDInsightCluster“ von „ClusterGetResponse“ in „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="bbd58-193">Ausgabetyp für „Set-AzHDInsightGatewaySettings“ von „HttpConnectivitySettings“ in „GatewaySettings“ geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="bbd58-194">Einige Testfälle für Szenarien wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="bbd58-195">Aliase wurden entfernt: „Add-AzHDInsightConfigValues“, „Get-AzHDInsightProperties“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-196">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-197">Wichtige Änderungen:</span><span class="sxs-lookup"><span data-stu-id="bbd58-197">Breaking changes:</span></span>
    - <span data-ttu-id="bbd58-198">Das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bbd58-199">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Add-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bbd58-200">Das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bbd58-201">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Get-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bbd58-202">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="bbd58-203">Die „OperationsMonitoringProperties“-Eigenschaft vom Typ „Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="bbd58-204">Das Cmdlet „New-AzIotHubExportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubExportDevices“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="bbd58-205">Das Cmdlet „New-AzIotHubImportDevice“ verfügt nicht mehr über Unterstützung für den Alias „New-AzIotHubImportDevices“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="bbd58-206">Das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ unterstützt den Parameter „EventHubEndpointName“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bbd58-207">Der Parametersatz „__AllParameterSets“ für das Cmdlet „Remove-AzIotHubEventHubConsumerGroup“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="bbd58-208">Das Cmdlet „Set-AzIotHub“ unterstützt den Parameter „OperationsMonitoringProperties“ nicht mehr, und für den ursprünglichen Parameternamen wurde kein Alias gefunden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="bbd58-209">Der Parametersatz „UpdateOperationsMonitoringProperties“ für das Cmdlet „Set-AzIotHub“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-211">Azure wurde die Azure Site Recovery-Unterstützung zum Konfigurieren von Netzwerkressourcen, z. B. NSG, öffentliche IP-Adresse und interner Load Balancer für Azure, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-212">Azure Site Recovery-Unterstützung zum Schreiben auf verwaltete Datenträger für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="bbd58-213">Azure Site Recovery-Unterstützung für NIC-Reduzierung für VMware zu Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="bbd58-214">Azure wurde Azure Site Recovery-Unterstützung für beschleunigten Netzwerkbetrieb für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-215">Azure wurde Azure Site Recovery-Unterstützung für automatische Agent-Updates für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-216">Azure wurde Azure Site Recovery-Unterstützung für SSD Standard für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-217">Azure wurde Azure Site Recovery-Unterstützung für das zweistufige Azure Disk Encryption-Verfahren für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-218">Azure wurde Azure Site Recovery-Unterstützung für das Schützen von neu hinzugefügten Datenträgern für Azure hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-219">Feature „Vorläufiges Löschen“ (SoftDelete) für VM und zugehörige Tests hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-220">Az.Resources</span></span>
* <span data-ttu-id="bbd58-221">Abhängigkeitsassembly „Microsoft.Extensions.Caching.Memory“ von 1.1.1 auf 2.2 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-222">Az.Network</span></span>
* <span data-ttu-id="bbd58-223">Alle Cmdlets für „PrivateEndpointConnection“ geändert, um Unterstützung für generischen Dienstanbieter bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="bbd58-224">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bbd58-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="bbd58-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bbd58-230">Neues Cmdlet für „PrivateLinkResource“ hinzugefügt, einschließlich Unterstützung des generischen Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="bbd58-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="bbd58-231">Neues Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bbd58-231">New cmdlet:</span></span>
        - <span data-ttu-id="bbd58-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="bbd58-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="bbd58-233">Neue Felder und Parameter für das Feature „Proxyprotokoll V2“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="bbd58-234">„EnableProxyProtocol“-Eigenschaft in „PrivateLinkService“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="bbd58-235">„LinkIdentifier“-Eigenschaft in „PrivateEndpointConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="bbd58-236">„New-AzPrivateLinkService“ aktualisiert, um den neuen optionalen Parameter „EnableProxyProtocol“ hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="bbd58-237">Fehlerhafte Parameterbeschreibung in Referenzdokumentation von „New-AzApplicationGatewaySku“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="bbd58-238">Neue Cmdlets zur Unterstützung der Azure-Firewallrichtlinie hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="bbd58-239">Unterstützung für untergeordnete Ressource „RouteTables“ von VirtualHub hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="bbd58-240">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-240">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="bbd58-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="bbd58-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bbd58-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bbd58-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="bbd58-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="bbd58-246">Unterstützung für die neuen Eigenschaften „Sku“ von VirtualHub und „VirtualWANType“ von VirtualWan hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="bbd58-247">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bbd58-248">New-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bbd58-249">Update-AzVirtualHub: Parameter „Sku“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="bbd58-250">New-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="bbd58-251">Update-AzVirtualWan: Parameter „VirtualWANType“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="bbd58-252">Unterstützung für „EnableInternetSecurity“-Eigenschaft für „HubVnetConnection“, „VpnConnection“ und „ExpressRouteConnection“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="bbd58-253">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-253">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="bbd58-255">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bbd58-256">New-AzureRmVirtualHubVnetConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bbd58-257">New-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bbd58-258">Update-AzureRmVpnConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bbd58-259">New-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="bbd58-260">Set-AzureRmExpressRouteConnection: Parameter „EnableInternetSecurity“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="bbd58-261">Unterstützung für die Konfiguration der „WebApplicationFirewall“-Richtlinie der obersten Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="bbd58-262">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-262">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="bbd58-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="bbd58-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="bbd58-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="bbd58-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="bbd58-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="bbd58-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bbd58-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="bbd58-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="bbd58-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="bbd58-269">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bbd58-270">New-AzApplicationGatewayFirewallPolicy: Parameter „PolicySetting“, „ManagedRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="bbd58-271">Unterstützung für Operator „Geo-Match“ unter „CustomRule“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="bbd58-272">„GeoMatch“ zum Operator von „FirewallCondition“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="bbd58-273">Unterstützung für Firewallrichtlinien „perListener“ und „perSite“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="bbd58-274">Mit optionalen Parametern aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="bbd58-275">New-AzApplicationGatewayHttpListener: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="bbd58-276">New-AzApplicationGatewayPathRuleConfig: Parameter „FirewallPolicy“, „FirewallPolicyId“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="bbd58-277">Fehlerbehebung: Nichtbeachtung der Groß-/Kleinschreibung für erforderliches Subnetz mit dem Namen „AzureBastionSubnet“ in „PSBastion“ ist jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="bbd58-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="bbd58-278">Unterstützung für Ziel-FQDNs in Netzwerkregeln und Übersetzung von FQDN in NAT-Regeln für Azure Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="bbd58-279">Unterstützung für Ressource „RouteTables“ der obersten Ebene von „IpGroup“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="bbd58-280">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-280">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="bbd58-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="bbd58-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="bbd58-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-286">Cmdlet „Add-AzServiceFabricApplicationCertificate“ entfernt, da dieses Szenario durch „Add-AzVmssSecret“ abgedeckt ist.</span><span class="sxs-lookup"><span data-stu-id="bbd58-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-287">Az.Sql</span></span>
* <span data-ttu-id="bbd58-288">Unterstützung für die Wiederherstellung von gelöschten Datenbanken auf verwalteten Instanzen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="bbd58-289">Veraltete Cmdlets für die Überprüfung aus Code ausgesondert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="bbd58-290">Veraltete Aliase entfernt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="bbd58-291">Get-AzSqlDatabaseIndexRecommendations (stattdessen „Get-AzSqlDatabaseIndexRecommendation“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="bbd58-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="bbd58-292">Get-AzSqlDatabaseRestorePoints (stattdessen „Get-AzSqlDatabaseRestorePoint“ verwenden)</span><span class="sxs-lookup"><span data-stu-id="bbd58-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="bbd58-293">Cmdlet „Get-AzSqlDatabaseSecureConnectionPolicy“ wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bbd58-294">Aliase für veraltete Cmdlets für Einstellungen zur Sicherheitsrisikobewertung wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="bbd58-295">Cmdlets für Einstellungen für die erweiterte Bedrohungserkennung wurden als veraltet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="bbd58-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="bbd58-296">Cmdlets zum Deaktivieren und Aktivieren von Vertraulichkeitsempfehlungen in Spalten einer Datenbank hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-297">Az.Storage</span></span>
* <span data-ttu-id="bbd58-298">Unterstützung für große Dateifreigaben beim Erstellen oder Aktualisieren eines Speicherkontos hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="bbd58-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bbd58-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bbd58-301">Beim Schließen/Abrufen des Dateihandles wird die Überprüfung des Eingabepfads auf Dateiverzeichnis oder Datei übersprungen, um einen Fehler für das Objekt im Status „DeletePending“ zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="bbd58-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bbd58-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="bbd58-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bbd58-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="bbd58-304">2.8.0: Oktober 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="bbd58-305">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-305">General</span></span>
* <span data-ttu-id="bbd58-306">Az.HealthcareApis-Release 1.0.0</span><span class="sxs-lookup"><span data-stu-id="bbd58-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bbd58-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-307">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-308">Telemetriedaten und URL-Umschreibung für generierte Module aktualisiert, Windows-Komponententests korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bbd58-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-309">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-310">**Set-AzApiManagementApi**: Unterstützung für die Aktualisierung der API in „ApiVersionSet“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="bbd58-311">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="bbd58-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-312">Az.Automation</span></span>
* <span data-ttu-id="bbd58-313">Cmdlet „New-AzureAutomationSoftwareUpdateConfiguration“ für den Parameter für die Linux-Neustarteinstellung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="bbd58-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bbd58-314">Az.Batch</span></span>
* <span data-ttu-id="bbd58-315">**Get-AzBatchNodeAgentSku** ist veraltet und wird in Version 2.0.0 durch **Get-AzBatchSupportImage** ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-316">Az.Compute</span></span>
* <span data-ttu-id="bbd58-317">Parameter „Priority“, „EvictionPolicy“ und „MaxPrice“ zu den Cmdlets „“New-AzVM“ und „New-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="bbd58-318">Warnmeldung und Hilfedokument für die Cmdlets „Add-AzVMAdditionalUnattendContent“ und „Add-AzVMSshPublicKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="bbd58-319">Ausnahme „-skipVmBackup“ Linux-VMs mit verwalteten Datenträgern für „Set-AzVMDiskEncryptionExtension“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="bbd58-320">Fehler beim Aktualisieren von Verschlüsselungseinstellungen in „Set-AzVMDiskEncryptionExtension“ korrigiert (zweistufiges Szenario)</span><span class="sxs-lookup"><span data-stu-id="bbd58-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-321">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-322">CRUD-Befehle für ADF V2-Datenfluss hinzugefügt: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow und Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="bbd58-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="bbd58-323">Aktionsbefehle für Debugsitzung für ADF V2-Datenfluss hinzugefügt: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand und Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="bbd58-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="bbd58-324">Version des ADF .NET SDK auf 4.2.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-326">Kontoüberprüfung korrigiert, sodass Konten mit „-“ ohne Domäne übermittelt werden können</span><span class="sxs-lookup"><span data-stu-id="bbd58-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="bbd58-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="bbd58-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="bbd58-328">PowerShell-Version auf 1.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="bbd58-329">SDK-Version auf 1.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="bbd58-330">Aktualisierung in Tests, um auf neue SDK-Version zu verweisen</span><span class="sxs-lookup"><span data-stu-id="bbd58-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="bbd58-331">Ausgabestruktur von geschachtelt in vereinfacht geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-332">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-333">Neue Routingquelle hinzugefügt: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="bbd58-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="bbd58-334">Kleinere Fehlerbehebung: „Get-AzIothub“ gibt „subscriptionId“ nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd58-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-335">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-336">Neue Aktionsgruppenempfänger für Aktionsgruppe hinzugefügt:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="bbd58-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="bbd58-337">Verwendung des allgemeinen Warnungsschemas für Empfänger aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="bbd58-338">Dies gilt nicht für SMS, Azure App-Pushbenachrichtigungen, ITSM und Sprachempfänger.</span><span class="sxs-lookup"><span data-stu-id="bbd58-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="bbd58-339">Webhooks unterstützen nun die Azure Active Directory-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="bbd58-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-340">Az.Network</span></span>
* <span data-ttu-id="bbd58-341">Neues Cmdlet „Get-AzAvailableServiceAlias“ hinzugefügt, das zum Abrufen der Aliase aufgerufen werden kann, die für Dienstendpunktrichtlinien verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="bbd58-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="bbd58-342">Unterstützung für das Hinzufügen von Verbindungen von Datenverkehrsselektoren zu Virtual Network-Gatewayverbindungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="bbd58-343">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-343">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="bbd58-345">Cmdlets mit optionalen Parametern aktualisiert: -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bbd58-346">Unterstützung für ESP- und AH-Protokolle in Konfigurationen von Netzwerksicherheitsregeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="bbd58-347">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="bbd58-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bbd58-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bbd58-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bbd58-351">Verbesserte Behandlung von Ausnahmen in Cortex-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="bbd58-352">Neue Generationen und SKUs für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="bbd58-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="bbd58-353">Einführung neuer Generationen für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="bbd58-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="bbd58-354">Einführung neuer SKUs mit höherem Durchsatz für VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="bbd58-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bbd58-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bbd58-355">Az.RedisCache</span></span>
* <span data-ttu-id="bbd58-356">Referenzdokumentation zu „Set-AzRedisCache“ aktualisiert, um fehlende Werte für den Parameter „-Size“ aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="bbd58-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-357">Az.Sql</span></span>
* <span data-ttu-id="bbd58-358">Unterstützung für das Festlegen des Active Directory-Administrators für verwaltete Instanz hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-359">Az.Storage</span></span>
* <span data-ttu-id="bbd58-360">Storage-Clientbibliothek auf 11.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="bbd58-361">Auflisten von Containern mit der API der Verwaltungsebene, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="bbd58-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bbd58-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bbd58-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="bbd58-363">Auflisten von Storage-Konten aus Abonnements, wird mit „NextPageLink“ aufgelistet</span><span class="sxs-lookup"><span data-stu-id="bbd58-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="bbd58-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bbd58-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bbd58-365">Az.StorageSync</span></span>
* <span data-ttu-id="bbd58-366">Problem 9810 in „Reset-AzStorageSyncServerCertificate“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-367">Az.Websites</span></span>
* <span data-ttu-id="bbd58-368">Fehler beim Aktualisieren von ASP einer App mit „Set-AzWebApp“</span><span class="sxs-lookup"><span data-stu-id="bbd58-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="bbd58-369">2.7.0: September 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bbd58-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-370">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-371">Beschreibung des Parameters „-Format“ in der Referenzdokumentation für „Set-AzApiManagementPolicy“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="bbd58-372">Verweise des veralteten Cmdlets „Update-AzApiManagementDeployment“ aus Referenzdokumentation entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="bbd58-373">Verwenden Sie stattdessen „Set-AzApiManagement“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-374">Az.Automation</span></span>
* <span data-ttu-id="bbd58-375">Tippfehler im Beispiel in der Referenzdokumentation für „Register-AzAutomationDscNode“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="bbd58-376">Erläuterung zur Betriebssystemeinschränkung zu „Register-AzAutomationDSCNode“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="bbd58-377">Nullverweisausnahme des Cmdlets „Start-AzAutomationRunbook“ für die Option „-Wait“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-378">Az.Compute</span></span>
* <span data-ttu-id="bbd58-379">Parameter „UploadSizeInBytes“ zu „New-AzDiskConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="bbd58-380">Inkrementeller Parameter zu „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bbd58-381">Feature für VM mit niedriger Priorität hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="bbd58-382">Parameter „MaxPrice“, „EvictionPolicy“ und „Priority“ zu New-AzVMConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="bbd58-383">Parameter „MaxPrice“ zu den Cmdlets „New-AzVmssConfig“, „Update-AzVM“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="bbd58-384">Fehlerbehebung für VM-Verweis für das Cmdlet „Get-AzAvailabilitySet“, wenn alle Verfügbarkeitsgruppen im Abonnement aufgelistet werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="bbd58-385">Nullausnahme für „Get-AzRemoteDesktopFile“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="bbd58-386">VHD-Suchmethode für Position relativ zum Ende korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="bbd58-387">Problem mit UltraSSD für „New-AzVM“ und „Update-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-388">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-389">Drei neue Befehle für ADF V2 hinzugefügt: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription und Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="bbd58-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="bbd58-390">Version des ADF .NET SDK auf 4.1.3 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="bbd58-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bbd58-391">Az.HDInsight</span></span>
* <span data-ttu-id="bbd58-392">Hinweis auf Breaking Changes hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-393">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-394">Unterstützung zum Aufrufen eines Failovers für einen IoT-Hub zur geografisch gekoppelten Notfallwiederherstellungsregion hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="bbd58-395">Unterstützung zum Verwalten der Nachrichtenanreicherung für einen IoT-Hub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="bbd58-396">Die folgenden Cmdlets sind neu:</span><span class="sxs-lookup"><span data-stu-id="bbd58-396">New cmdlets are:</span></span>
    - <span data-ttu-id="bbd58-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bbd58-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bbd58-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bbd58-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bbd58-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bbd58-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="bbd58-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="bbd58-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-401">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-402">Verweis auf das aktuelle Monitor SDK, d. h. 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="bbd58-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="bbd58-403">Geringfügige Änderungen an den Metrik-Cmdlets vorgenommen, d. h. die Einheitenenumeration unterstützt verschiedene neue Werte.</span><span class="sxs-lookup"><span data-stu-id="bbd58-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="bbd58-404">Dabei handelt es sich um schreibgeschützte Cmdlets, sodass keine Änderungen an der Eingabe der Cmdlets erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="bbd58-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="bbd58-405">Die API-Version der **ActionGroups**-Anforderungen lautet jetzt **2019-06-01** (zuvor **2018-03-01**).</span><span class="sxs-lookup"><span data-stu-id="bbd58-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="bbd58-406">Die Szenariotests wurden aktualisiert, um diese Änderung zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="bbd58-407">Die Konstruktoren für die Klassen **EmailReceiver** und **WebhookReceiver** haben ein neues obligatorisches Argument hinzugefügt, d. h. einen booleschen Wert namens **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="bbd58-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="bbd58-408">Derzeit ist der Wert auf **false** festgelegt, damit sich dieser Breaking Change nicht auf die Cmdlets auswirkt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="bbd58-409">**HINWEIS:** Dies ist eine vorübergehende Änderung, die vom Team für Warnungen validiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="bbd58-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="bbd58-410">Die Reihenfolge der Argumente für den Konstruktor der Klasse **Source** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bbd58-411">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bbd58-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="bbd58-412">Die Reihenfolge der Argumente für den Konstruktor der Klasse **AlertingAction** (in Bezug auf die Klasse **ScheduledQueryRuleSource**) hat sich seit dem vorherigen SDK geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="bbd58-413">Im Rahmen dieser Änderung war die Korrektur von zwei Komponententests erforderlich: Sie wurden kompiliert, bei den Tests trat jedoch ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bbd58-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="bbd58-414">Unterstützung von Kriterien für dynamische Schwellwerte für Metrikwarnung v2</span><span class="sxs-lookup"><span data-stu-id="bbd58-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="bbd58-415">New-AzMetricAlertRuleV2Criteria: Erstellt nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="bbd58-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="bbd58-416">Add-AzMetricAlertRuleV2: Akzeptiert nun auch Kriterien für dynamische Schwellwerte.</span><span class="sxs-lookup"><span data-stu-id="bbd58-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="bbd58-417">Verbesserungen an den Cmdlets für geplante Abfrageregeln (Scheduled Query Rule, SQR)</span><span class="sxs-lookup"><span data-stu-id="bbd58-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="bbd58-418">Cmdlets akzeptieren den Parameter „Location“ in zwei Formaten: entweder den Standort (z. B. „eastus“) oder den Anzeigenamen des Standorts (z. B. „USA, Osten“)</span><span class="sxs-lookup"><span data-stu-id="bbd58-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="bbd58-419">Parameter „Enabled“ in Hilfedateien ordnungsgemäß dargestellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="bbd58-420">Beispiele für optionalen Parameter „ActionGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="bbd58-421">Hilfedateien insgesamt verbessert</span><span class="sxs-lookup"><span data-stu-id="bbd58-421">Overall improved help files</span></span>
* <span data-ttu-id="bbd58-422">Fehler beim Bestimmen des Bereichstyps für „Set-AzActionRule“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-423">Az.Network</span></span>
* <span data-ttu-id="bbd58-424">Fehlerhaftes Beispiel in der Referenzdokumentation zu „New-AzApplicationGateway“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="bbd58-425">Hinweis in der Referenzdokumentation zu „Get-AzNetworkWatcherPacketCapture“ zum Abrufen aller Eigenschaften für eine Paketerfassung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="bbd58-426">Beispiel in der Referenzdokumentation zu „Test-AzNetworkWatcherIPFlow“ korrigiert, um die Netzwerkadapter ordnungsgemäß aufzulisten</span><span class="sxs-lookup"><span data-stu-id="bbd58-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="bbd58-427">Cloudausnahmeanalyse verbessert, um ggf. zusätzliche Details anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="bbd58-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="bbd58-428">Cloudausnahmeanalyse verbessert, um zusätzlichen Typ der SDK-Ausnahme zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="bbd58-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="bbd58-429">Falsche Zuordnung der Sicherheitsregelmodelle korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="bbd58-430">Eigenschaften zur Netzwerkschnittstelle für das Feature für die private IP-Adresse hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="bbd58-431">Eigenschaft „PrivateEndpoint“ als Typ „PSResourceId“ zu „PSNetworkInterface“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="bbd58-432">Eigenschaft „PrivateLinkConnectionProperties“ als Typ „PSIpConfigurationConnectivityInformation“ zu „PSNetworkInterfaceIPConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="bbd58-433">Neue Modellklasse „PSIpConfigurationConnectivityInformation“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="bbd58-434">Neues ApplicationRuleProtocolType-Element „mssql“ für Azure Firewall-Ressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="bbd58-435">Unterstützung von Mehrfachverbindungen in Virtual WAN</span><span class="sxs-lookup"><span data-stu-id="bbd58-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="bbd58-436">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-436">New cmdlets</span></span>
        - <span data-ttu-id="bbd58-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="bbd58-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="bbd58-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="bbd58-439">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bbd58-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="bbd58-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bbd58-440">New-VpnSite</span></span>
        - <span data-ttu-id="bbd58-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="bbd58-441">Update-VpnSite</span></span>
        - <span data-ttu-id="bbd58-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-442">New-VpnConnection</span></span>
        - <span data-ttu-id="bbd58-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-443">Update-VpnConnection</span></span>
* <span data-ttu-id="bbd58-444">Dokumente für einige PowerShell-Beispiele korrigiert, sodass Az-Cmdlets anstelle von AzureRM-Cmdlets verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-446">AzureVMpolicy-Objekt mit ProtectedItemsCount-Attribut aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="bbd58-447">Tests für VM-Richtlinie und Wiederherstellung des ursprünglichen Speicherkontos hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-448">Az.Resources</span></span>
* <span data-ttu-id="bbd58-449">Fehler behoben, aufgrund dessen „New-AzRoleAssignment“ nicht ohne den Parameter „Scope“ aufgerufen werden konnte</span><span class="sxs-lookup"><span data-stu-id="bbd58-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-451">Tippfehler im Beispiel für die Referenzdokumentation „Update-AzServiceFabricReliability“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="bbd58-452">Neue Cmdlets zum Verwalten von Anwendung und Diensten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="bbd58-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bbd58-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bbd58-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bbd58-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bbd58-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bbd58-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bbd58-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bbd58-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="bbd58-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bbd58-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bbd58-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bbd58-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bbd58-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bbd58-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bbd58-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bbd58-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bbd58-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="bbd58-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="bbd58-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="bbd58-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="bbd58-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="bbd58-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="bbd58-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="bbd58-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="bbd58-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="bbd58-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="bbd58-466">Service Fabric SDK auf Version 1.2.0 aktualisiert, die API-Version 2019-03-01 des Service Fabric-Ressourcenanbieters verwendet</span><span class="sxs-lookup"><span data-stu-id="bbd58-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bbd58-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bbd58-467">Az.SignalR</span></span>
* <span data-ttu-id="bbd58-468">Cmdlets „Update“, „Restart“, „CheckNameAvailability“ und „GetUsage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-469">Az.Sql</span></span>
* <span data-ttu-id="bbd58-470">Beispiel in der Referenzdokumentation für „Get-AzSqlElasticPool“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="bbd58-471">V-Kern-Beispiel zum Erstellen eines Pools für elastische Datenbanken hinzugefügt (New-AzSqlElasticPool)</span><span class="sxs-lookup"><span data-stu-id="bbd58-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="bbd58-472">Überprüfung von „EmailAddresses“ sowie Validierung, dass „EmailAdmins“ nicht auf „false“ festgelegt ist, in „Set-AzSqlServerAdvancedThreatProtectionPolicy“ und „Set-AzSqlDatabaseAdvancedThreatProtectionPolicy“ entfernt, wenn „EmailAddresses“ leer ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="bbd58-473">Entfernen der Einstellungen für Server-/Datenbanküberwachung aktiviert, wenn mehrere Diagnoseeinstellungen vorhanden sind, die eine Überwachungskategorie ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bbd58-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="bbd58-474">Überprüfung von E-Mail-Adressen in mehreren Cmdlets für die SQL-Sicherheitsrisikobewertung korrigiert (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting und Update-AzSqlInstanceVulnerabilityAssessmentSetting)</span><span class="sxs-lookup"><span data-stu-id="bbd58-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-475">Az.Storage</span></span>
* <span data-ttu-id="bbd58-476">Beispiel in der Referenzdokumentation für „Get-AzStorageAccountKey“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="bbd58-477">Beim Upload/Download von Azure-Dateien wird das Beibehalten der SMB-Eigenschaften der Quelldateien (Dateiattribute, Zeitpunkt der Dateierstellung, letzter Schreibzugriff für die Datei) in der Zieldatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="bbd58-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="bbd58-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="bbd58-480">Fehler beim Hochladen von Blockblobs mit Eigenschaften/Metadaten für das für einen Container aktivierte ImmutabilityPolicy-Element behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="bbd58-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="bbd58-482">Unterstützung für die Verwaltung von Azure-Dateifreigaben mit der API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="bbd58-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="bbd58-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbd58-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bbd58-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbd58-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bbd58-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbd58-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="bbd58-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbd58-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-487">Az.Websites</span></span>
* <span data-ttu-id="bbd58-488">Problem behoben, aufgrund dessen webapp-Tags beim Migrieren der App zu neuem ASP gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="bbd58-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="bbd58-489">„Publish-AzureWebapp“ für die Verwendung unter Linux und Windows korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="bbd58-490">Beispiel in Referenzdokumentation „Get-AzWebAppPublishingProfile“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="bbd58-491">2.6.0: August 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="bbd58-492">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-492">General</span></span>
* <span data-ttu-id="bbd58-493">Verschiedene Tippfehler in zahlreichen Modulen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bbd58-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-494">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-495">Unterstützung der benutzerseitig zugewiesenen MSI in Azure Functions-Authentifizierung (#9479)</span><span class="sxs-lookup"><span data-stu-id="bbd58-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="bbd58-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bbd58-496">Az.Aks</span></span>
* <span data-ttu-id="bbd58-497">Problem mit der Ausgabe für „Get-AzAks“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="bbd58-498">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="bbd58-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bbd58-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-499">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-500">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="bbd58-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="bbd58-501">.NET-NuGet-Version aktualisiert, die keine Einschränkungen für „productId“, „apiId“, „groupId“ und „userId“ erzwingt</span><span class="sxs-lookup"><span data-stu-id="bbd58-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="bbd58-502">**Get-AzApiManagementProduct:** Unterstützung für das Abfragen von Produkten mithilfe der API hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="bbd58-503">**New-AzApiManagementApiRevision:** Problem behoben, aufgrund dessen „ApiRevisionDescription“ beim Erstellen einer neuen API-Revision nicht festgelegt wurde https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="bbd58-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="bbd58-504">Tippfehler im Modell „PsApiManagementOAuth2AuthrozationServer“ korrigiert: PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bbd58-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bbd58-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bbd58-505">Az.Batch</span></span>
* <span data-ttu-id="bbd58-506">Tippfehler in Hilfemeldung und Dokumentation korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="bbd58-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bbd58-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-507">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-508">Tippfehler im Hilfsprogramm für die CDN-Modulkonvertierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-509">Az.Compute</span></span>
* <span data-ttu-id="bbd58-510">VmssId zum Cmdlet „New-AzVMConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="bbd58-511">Parameter „TerminateScheduledEvents“ und „TerminateScheduledEventNotBeforeTimeoutInMinutes“ zu „New-AzVmssConfig“ und „Update-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="bbd58-512">HyperVGeneration-Eigenschaft zu VM-Imageobjekt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="bbd58-513">Host- und HostGroup-Features hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="bbd58-514">Neue Cmdlets:   New-AzHostGroup, New-AzHost, Get-AzHostGroup, Get-AzHost, Remove-AzHostGroup, Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="bbd58-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="bbd58-515">Parameter „HostId“ zu „New-AzVMConfig“ und „New-AzVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="bbd58-516">Beispiel in der Dokumentation zu „Invoke-AzVMRunCommand“ zur Verwendung des richtigen Parameternamens aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="bbd58-517">Beschreibung für „-VolumeType“ in der Referenzdokumentation zu „Set-AzVMDiskEncryptionExtension“ und „Set-AzVmssDiskEncryptionExtension“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-518">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-519">Tippfehler in der Dokumentation zu „New-AzDataFactoryEncryptValue“ korrigiert (Großschreibung von „Windows“)</span><span class="sxs-lookup"><span data-stu-id="bbd58-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="bbd58-520">Version des ADF .NET SDK auf 4.1.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="bbd58-521">Parameter „DataProxyIntegrationRuntimeName“, „DataProxyStagingLinkedServiceName“ und „DataProxyStagingPath“ für Befehl „Set-AzureRmDataFactoryV2IntegrationRuntime“ hinzugefügt, um die Einrichtung der selbstgehosteten Integration Runtime als Proxy für die SSIS Integration Runtime zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bbd58-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="bbd58-522">„PSTriggerRun“ zum Anzeigen der ausgelösten Pipelines, Meldungen und Eigenschaften und „PSActivityRun“ zum Anzeigen des Aktivitätstyps aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-524">Hängen von „Get-DataLakeStoreDeletedItem“ aufgrund von Fehlern oder Remoteausnahmen behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bbd58-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-525">Az.EventHub</span></span>
* <span data-ttu-id="bbd58-526">Behebung des Problems #9658: Tippfehler im Parameter „VirtualNteworkRule“ in „Set-AzEventHubNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="bbd58-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="bbd58-527">Behebung des Problems #9558: „Set-AzEventHubNamespace“ verwendet PATCH anstelle von PUT.</span><span class="sxs-lookup"><span data-stu-id="bbd58-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="bbd58-528">Parameter „EnableKafka“ zum Cmdlet „Set-AzEventHubNamespace“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="bbd58-529">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="bbd58-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bbd58-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bbd58-531">Tippfehler („Azure“ in Kleinbuchstaben) in der Dokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-532">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-533">Falscher Parametername in der Hilfedokumentation korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-534">Az.Network</span></span>
* <span data-ttu-id="bbd58-535">„New-AzPrivateLinkServiceIpConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="bbd58-536">Parameter „PublicIpAddress“ ausgemustert, da er auf Serverseite nie verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bbd58-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="bbd58-537">Optionaler Parameter „Primary“ hinzugefügt, der angibt, ob die aktuelle IP-Konfiguration die primäre ist oder nicht</span><span class="sxs-lookup"><span data-stu-id="bbd58-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="bbd58-538">Verbesserte Verarbeitung der Anforderungsfehlerausnahme aus dem SDK: Behebt das Problem, dass vorherige SDK-Ausnahmen nicht richtig behandelt wurden, was dazu führt, dass Schlüsselfehlerdetails nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="bbd58-539">Validierungslogik für Ipv6-IP-Präfix angepasst, damit auf die richtige IPv6-Präfixlänge geprüft wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="bbd58-540">„Get-AzVirtualNetworkSubnetConfig“ aktualisiert: Parametersatz zum Abrufen nach Subnetzressourcen-ID hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="bbd58-541">Aktualisierte Beschreibung des Location-Parameters für „AzNetworkServiceTag“</span><span class="sxs-lookup"><span data-stu-id="bbd58-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-543">Aktualisierte Dokumentation für „New-AzOperationalInsightsLinuxSyslogDataSource“</span><span class="sxs-lookup"><span data-stu-id="bbd58-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="bbd58-544">Beispiel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-544">Added example</span></span>
    - <span data-ttu-id="bbd58-545">Beschreibung für den Parameter „-Name“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="bbd58-546">Beispiel für „New-AzOperationalInsightsWindowsEventDataSource“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="bbd58-547">Beschreibung des Parameters „-Name“ für „New-AzOperationalInsightsWindowsEventDataSource“ geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-549">„Get-AzRecoveryServicesBackupJobDetail.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-550">Az.Resources</span></span>
* <span data-ttu-id="bbd58-551">Unterstützung für die neue API-Version 2019-05-10 für Microsoft.Resource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="bbd58-552">Unterstützung für „copy.count = 0“ für Variablen, Ressourcen und Eigenschaften hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="bbd58-553">Ressourcen mit „condition = false“ oder „copy.count = 0“ werden im vollständigen Modus gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bbd58-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="bbd58-554">Beispiel zum Hinzufügen einer Richtlinie auf Abonnementebene zur Hilfedokumentation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-555">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-556">Behebung des Problems #9658: Tippfehler für Parameter „VirtualNetworkRule“ in „Set-AzServiceBusNetworkRuleSet“</span><span class="sxs-lookup"><span data-stu-id="bbd58-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="bbd58-557">Behebung des Problems #9786: Erstellen einer Regel mit Rechten, die nur das Lauschen zulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="bbd58-558">Neuer Befehl „Test-AzServiceBusNameAvailability“ zum Überprüfen der Verfügbarkeit des Namens für Warteschlange und Thema hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-560">Fehler bei Cmdlets zum Hinzufügen des Knotentyps korrigiert:</span><span class="sxs-lookup"><span data-stu-id="bbd58-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="bbd58-561">Fehler „NullReferenceException“, wenn die Ressourcengruppe andere VMSS enthielt, die nicht mit dem Service Fabric-Cluster in Zusammenhang stehen</span><span class="sxs-lookup"><span data-stu-id="bbd58-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="bbd58-562">Problembehebung: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="bbd58-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="bbd58-563">Fehler behoben, aufgrund dessen bei einem Cmdlet ein Fehler auftrat, wenn sich „virtualNetwork“ in einer anderen Ressourcengruppe befand als der Cluster</span><span class="sxs-lookup"><span data-stu-id="bbd58-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="bbd58-564">Problembehebung: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="bbd58-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="bbd58-565">Cmdlet „Add-AzServiceFabricApplicationCertificate“ ausgemustert</span><span class="sxs-lookup"><span data-stu-id="bbd58-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-566">Az.Sql</span></span>
* <span data-ttu-id="bbd58-567">Dokumentation alter Überwachungs-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-568">Az.Storage</span></span>
* <span data-ttu-id="bbd58-569">Hilfe für „Get/Close-AzStorageFileHandle“ aktualisiert (weitere Szenarien zu Cmdlet-Beispielen hinzugefügt und Parameterbeschreibungen aktualisiert)</span><span class="sxs-lookup"><span data-stu-id="bbd58-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="bbd58-570">Unterstützung von „StandardBlobTier“ in Uploadblobs und Kopierblobs</span><span class="sxs-lookup"><span data-stu-id="bbd58-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="bbd58-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="bbd58-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bbd58-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="bbd58-573">Unterstützung der Aktivierungspriorität im Kopierblob</span><span class="sxs-lookup"><span data-stu-id="bbd58-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="bbd58-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bbd58-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-575">Az.Websites</span></span>
* <span data-ttu-id="bbd58-576">Hinzufügen von Erläuterungen zum Parameter „-AppSettings“ in „Set-AzWebApp“ und „Set-AzWebAppSlot“</span><span class="sxs-lookup"><span data-stu-id="bbd58-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="bbd58-577">2.5.0: Juli 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-578">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-579">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="bbd58-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="bbd58-581">Tippfehler im Beispiel in der Dokumentation zu „Remove-AzApplicationInsightsApiKey“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="bbd58-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-582">Az.Automation</span></span>
* <span data-ttu-id="bbd58-583">Tippfehler in der Ressourcenzeichenfolge korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-585">Unterstützung für NetworkRuleSet hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-586">Az.Compute</span></span>
* <span data-ttu-id="bbd58-587">Fehlende Eigenschaften (ComputerName, OsName, OsVersion und HyperVGeneration) des Objekts für die VM-Instanzenansicht hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bbd58-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bbd58-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bbd58-589">Tippfehler in „Remove-AzContainerRegistryReplication“ für den Replikationsparameter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="bbd58-590">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="bbd58-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-591">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-592">Version des ADF .NET SDK auf 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="bbd58-593">Tippfehler in der Dokumentation für „Get-AzDataFactoryV2PipelineRun“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bbd58-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-594">Az.EventHub</span></span>
* <span data-ttu-id="bbd58-595">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bbd58-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bbd58-596">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bbd58-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-597">Az.KeyVault</span></span>
* <span data-ttu-id="bbd58-598">Unterstützung zum Angeben von KeySize für Zertifikatsrichtlinien hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bbd58-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bbd58-599">Az.LogicApp</span></span>
* <span data-ttu-id="bbd58-600">Korrektur für „Get-AzIntegrationAccountMap“ zum Auflisten aller Zuordnungstypen</span><span class="sxs-lookup"><span data-stu-id="bbd58-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="bbd58-601">Neuer MapType-Parameter für Filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="bbd58-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-602">Az.ManagedServices</span></span>
* <span data-ttu-id="bbd58-603">Unterstützung für API-Version 2019-06-01 (GA) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-604">Az.Network</span></span>
* <span data-ttu-id="bbd58-605">Unterstützung für privaten Endpunkt und privaten Verknüpfungsdienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="bbd58-606">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-606">New cmdlets</span></span>
        - <span data-ttu-id="bbd58-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbd58-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bbd58-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbd58-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bbd58-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="bbd58-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="bbd58-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="bbd58-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbd58-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="bbd58-615">Folgende Befehle für das Feature aktualisiert: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies für Subnetz in VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bbd58-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="bbd58-616">„New-AzVirtualNetworkSubnetConfig“, „Set-AzVirtualNetworkSubnetConfig“ und „Add-AzVirtualNetworkSubnetConfig“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="bbd58-617">Optionaler Parameter „-PrivateEndpointNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den privaten Endpunkt in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="bbd58-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="bbd58-618">Optionaler Parameter „-PrivateLinkServiceNetworkPoliciesFlag“ hinzugefügt, der konfiguriert, ob Netzwerkrichtlinien auf den Privat Link-Dienst in diesem Subnetz angewendet werden sollen</span><span class="sxs-lookup"><span data-stu-id="bbd58-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="bbd58-619">Der Cmdlet-Parameter „ServiceName“ von AzPrivateLinkService wurde aus Gründen der Abwärtskompatibilität in „Name“ mit dem Alias „ServiceName“ umbenannt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="bbd58-620">ICMP-Protokoll für Konfigurationen von Netzwerksicherheitsregeln aktiviert</span><span class="sxs-lookup"><span data-stu-id="bbd58-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="bbd58-621">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-621">Updated cmdlets</span></span>
        - <span data-ttu-id="bbd58-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bbd58-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="bbd58-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="bbd58-625">ConnectionProtocolType (Ikev1/Ikev2) als konfigurierbarer Parameter für „New-AzVirtualNetworkGatewayConnection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="bbd58-626">PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="bbd58-627">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bbd58-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="bbd58-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bbd58-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="bbd58-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="bbd58-631">Application Gateway-Befehl „New-AzApplicationGatewayProbeConfig“ zur Unterstützung des benutzerdefinierten Ports im Test aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="bbd58-632">„New-AzApplicationGatewayProbeConfig“ aktualisiert: Optionaler Parameter „Port“ hinzugefügt, der zum Testen des Back-End-Servers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="bbd58-633">Dieser Parameter gilt für Standard_V2 und WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="bbd58-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-635">Standardversion für gespeicherte Suchvorgänge auf 1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="bbd58-636">Verarbeitung des regulären NULL-Ausdrucks in benutzerdefinierten Protokollen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-638">„Get-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bbd58-639">„Get-AzRecoveryServicesBackupContainer.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="bbd58-640">„Get-AzRecoveryServicesVault.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="bbd58-641">„Wait-AzRecoveryServicesBackupJob.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="bbd58-642">„Set-AzRecoveryServicesVaultContext.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="bbd58-643">„Get-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bbd58-644">„Get-AzRecoveryServicesBackupRecoveryPoint.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="bbd58-645">„Restore-AzRecoveryServicesBackupItem.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="bbd58-646">Dienstaufruf zum Aufheben der Containerregistrierung für Azure-Dateifreigabe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="bbd58-647">„Set-AzRecoveryServicesAsrAlertSetting.md“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-648">Az.Resources</span></span>
- <span data-ttu-id="bbd58-649">Fehlendes Cmdlet entfernt, auf das in der Dokumentation zu „New-AzResourceGroupDeployment“ verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="bbd58-650">Richtlinien-Cmdlets zur Verwendung der neuen API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-651">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-652">Neues Cmdlet zum Erstellen eines SAS-Token hinzugefügt: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="bbd58-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="bbd58-653">Überprüfung und Fehlermeldung für Berechtigungen für „authorizationrules“ hinzugefügt, wenn nur „Verwalten“ zugewiesen wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-654">Az.Sql</span></span>
* <span data-ttu-id="bbd58-655">Fehlende Beispiele für Cmdlet „Set-AzSqlDatabaseSecondary“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="bbd58-656">Festlegen wiederkehrender Überprüfungen der Sicherheitsrisikobewertung ohne Angabe von E-Mail-Adressen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="bbd58-657">Tippfehler in einer Warnmeldung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-658">Az.Storage</span></span>
* <span data-ttu-id="bbd58-659">Beispiel in Referenzdokumentation für „Get-AzStorageAccount“ aktualisiert, sodass der richtige Parametername verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bbd58-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bbd58-660">Az.StorageSync</span></span>
* <span data-ttu-id="bbd58-661">Cmdlet „Invoke-AzStorageSyncChangeDetection“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="bbd58-662">Problem 9551 zur Berücksichtigung von „TierFilesOlderThanDays“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-663">Az.Websites</span></span>
* <span data-ttu-id="bbd58-664">Problem behoben, aufgrund dessen einige SiteConfig-Eigenschaften von „Get-AzWebApp“ und „Set-AzWebApp“ nicht zurückgegeben wurden</span><span class="sxs-lookup"><span data-stu-id="bbd58-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="bbd58-665">Neuer Standortparameter zu „Get-AzDeletedWebApp“ und „Restore-AzDeletedWebApp“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="bbd58-666">Fehler beim Klonen von Web-App-Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="bbd58-667">2.4.0 – Juli 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-668">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-669">Unterstützung für Profil-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="bbd58-670">Unterstützung für Umgebungen und Datenebenen in generierten Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="bbd58-671">Korrektur eines Fehlers, bei dem in einigen Fällen ein falscher Endpunkt für Datenebenen-Cmdlets in Windows PowerShell verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bbd58-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="bbd58-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bbd58-672">Az.Advisor</span></span>
* <span data-ttu-id="bbd58-673">Allgemein verfügbares Release von Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="bbd58-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="bbd58-674">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="bbd58-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-675">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-676">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="bbd58-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="bbd58-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="bbd58-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="bbd58-678">Unterstützung für Abfragen von Abonnements nach Benutzer und Produkt hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="bbd58-679">Unterstützung für Abfragen anhand des Umfangs hinzugefügt, „/“, „/apis“, „/apis/echo-api“</span><span class="sxs-lookup"><span data-stu-id="bbd58-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="bbd58-680">Behebung von Problem https://github.com/Azure/azure-powershell/issues/9307 und https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="bbd58-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="bbd58-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="bbd58-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="bbd58-682">Unterstützung für die Angabe von „ApiVersion“ und „ApiVersionSetId“ beim Importieren von APIs hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-683">Az.Automation</span></span>
* <span data-ttu-id="bbd58-684">Fehler beim Cmdlet „Set-AzAutomationConnectionFieldValue“ für die Verarbeitung des Zeichenfolgewerts behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-685">Az.Compute</span></span>
* <span data-ttu-id="bbd58-686">Parameter „HyperVGeneration“ zu New-AzImageConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-687">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-688">Aktualisierung der Ausgabe von ADF-Cmdlets für das Abrufen von Aktivitäts-, Pipeline- und Auslöserausführungen, um die Pipe „Select-Object“ zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bbd58-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bbd58-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bbd58-689">Az.EventGrid</span></span>
* <span data-ttu-id="bbd58-690">Tippfehler in Dokumentation zu 'New-AzEventGridSubscription' behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-691">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-692">Unterstützung für das erneute Generieren von Autorisierungsrichtlinienschlüsseln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-693">Az.Network</span></span>
* <span data-ttu-id="bbd58-694">„RoutingPreference“ zu öffentlichen IP-Tags hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="bbd58-695">Beispiele für Referenzdokumentation zu „Get-AzNetworkServiceTag“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bbd58-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bbd58-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="bbd58-697">Fehlerbehebung für Nullverweis in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="bbd58-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="bbd58-698">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="bbd58-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-700">Zurückgegebenes CustomLog-Datenquellenmodell in Get-AzOperationalInsightsDataSource korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-702">Fehlerbehebung für Befehl „get-policy“ IaaSVMs</span><span class="sxs-lookup"><span data-stu-id="bbd58-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-703">Az.Resources</span></span>
    - <span data-ttu-id="bbd58-704">Hilfetext für Parameter „-Top“ von „Get-AzPolicyState“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="bbd58-705">Clientseitige Unterstützung von Paginierung für „Get-AzPolicyAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="bbd58-706">Neue Parameter für „Set-AzPolicyAssignment“, „-PolicyParameters“ und „-PolicyParametersObject“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="bbd58-707">Einige Aktualisierungen von Dokumentationen und Beispielen für Policy-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-708">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-709">Korrektur für Problem Nr. 4938: „New-AzureRmServiceBusQueue“ gibt beim Festlegen von „MaxSizeInMegabytes“ „BadRequest“ zurück</span><span class="sxs-lookup"><span data-stu-id="bbd58-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-710">Az.Sql</span></span>
* <span data-ttu-id="bbd58-711">Instanzfailovergruppen-Cmdlets aus Vorschauversion in öffentliche Version hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="bbd58-712">Unterstützung von Azure SQL Server\Datenbanküberwachung mit neuen Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="bbd58-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bbd58-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bbd58-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="bbd58-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bbd58-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="bbd58-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="bbd58-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="bbd58-719">E-Mail-Einschränkungen aus Einstellungen der Sicherheitsrisikobewertung entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-720">Az.Storage</span></span>
* <span data-ttu-id="bbd58-721">Zwei Parameter („-IndexDocument“ und „-ErrorDocument404Path“) in folgendem Cmdlet von erforderlich in optional geändert:</span><span class="sxs-lookup"><span data-stu-id="bbd58-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="bbd58-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bbd58-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="bbd58-723">Hilfe zu „Get-AzStorageBlobContent“ mit neuem Beispiel ergänzt</span><span class="sxs-lookup"><span data-stu-id="bbd58-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="bbd58-724">Anzeige von mehr Fehlerinformationen beim Fehlschlagen eines Cmdlets mit „StorageException“</span><span class="sxs-lookup"><span data-stu-id="bbd58-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="bbd58-725">Unterstützung für das Erstellen oder Aktualisieren von Speicherkonten mit Azure Files AAD-DS-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="bbd58-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="bbd58-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="bbd58-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="bbd58-728">Unterstützung für das Auflisten oder Schließen von Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei</span><span class="sxs-lookup"><span data-stu-id="bbd58-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="bbd58-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bbd58-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="bbd58-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="bbd58-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="bbd58-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="bbd58-731">Az.StorageSync</span></span>
* <span data-ttu-id="bbd58-732">Dieses Modul ist nun als Teil des `Az`-Rollup-Moduls enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="bbd58-733">2.3.2 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-734">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-735">Fehler behoben, aufgrund dessen in manchen Fällen eine falsche URL für Funktionsaufrufe verwendet wurde</span><span class="sxs-lookup"><span data-stu-id="bbd58-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="bbd58-736">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="bbd58-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="bbd58-737">Problem mit Aliasen zwischen AzureRM und Azure-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="bbd58-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="bbd58-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="bbd58-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="bbd58-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-740">Az.Compute</span></span>
* <span data-ttu-id="bbd58-741">Die einfachen Parametersätze „New-AzVm“ und „New-AzVmss“ akzeptieren jetzt den Parameter „ProximityPlacementGroup“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="bbd58-742">Tippfehler in der Referenzdokumentation für „New-AzVM“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="bbd58-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bbd58-743">Az.Dns</span></span>
* <span data-ttu-id="bbd58-744">Tippfehler in den Hilfebeispielen zu „Set-AzDnsZone“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bbd58-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bbd58-745">Az.EventGrid</span></span>
* <span data-ttu-id="bbd58-746">Zur Verwendung der API-Version 2019-06-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="bbd58-747">Neue Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-747">New cmdlets:</span></span>
    - <span data-ttu-id="bbd58-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bbd58-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bbd58-749">Erstellt eine neue Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="bbd58-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bbd58-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bbd58-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bbd58-751">Ruft die Details einer Event Grid-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bbd58-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="bbd58-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="bbd58-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="bbd58-753">Entfernt eine Azure Event Grid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="bbd58-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bbd58-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bbd58-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bbd58-755">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid-Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="bbd58-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="bbd58-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bbd58-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="bbd58-757">Ruft die freigegebenen Zugriffsschlüssel ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="bbd58-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bbd58-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bbd58-759">Erstellt ein neues Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="bbd58-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="bbd58-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bbd58-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="bbd58-761">Ruft die Details eines Event Grid-Domänenthemas oder eine Liste aller Event Grid-Domänenthemen unter der jeweiligen Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bbd58-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="bbd58-762">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="bbd58-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="bbd58-763">Entfernt ein vorhandenes Azure Event Grid-Domänenthema.</span><span class="sxs-lookup"><span data-stu-id="bbd58-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="bbd58-764">Aktualisierte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="bbd58-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bbd58-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="bbd58-766">Neue erforderliche Parameter zur Unterstützung des Pipings für die neue Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bbd58-767">Neue erforderliche Parameter zum Angeben des neuen Event Grid-Domänennamens und/oder Namens des Event Grid-Domänenthemas hinzugefügt, um das Erstellen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="bbd58-768">Neue Parametersätze für Domänen und Domänenthemen hinzugefügt, um die Wiederverwendung vorhandener Parameter zuzulassen (‚z. B. „EndPointType“, „SubjectBeginsWith“ usw.)</span><span class="sxs-lookup"><span data-stu-id="bbd58-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="bbd58-769">Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="bbd58-770">Ablaufdatum des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="bbd58-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="bbd58-771">Erweiterte Filterparameter</span><span class="sxs-lookup"><span data-stu-id="bbd58-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="bbd58-772">Neue Enumeration für „servicebusqueue“ als Ziel hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="bbd58-773">Verwendung der Option „All“ in „-IncludedEventType“ gesperrt und wie folgt ersetzt</span><span class="sxs-lookup"><span data-stu-id="bbd58-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="bbd58-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="bbd58-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="bbd58-775">Neue optionale Parameter („Top“, „ODataQuery“ und „NextLink“) zur Unterstützung der Ergebnispaginierung und -filterung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="bbd58-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bbd58-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="bbd58-777">Neue erforderliche Parameter zur Unterstützung des Pipings für die Event Grid-Domäne und das Event Grid-Domänenthema hinzugefügt, um das Entfernen neuer Abonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="bbd58-778">Neue erforderliche Parameter zum Angeben des Event Grid-Domänennamens und/oder Event Grid-Domänenthemanamens hinzugefügt, um das Entfernen vorhandener Ereignisabonnements unter diesen Ressourcen zuzulassen</span><span class="sxs-lookup"><span data-stu-id="bbd58-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bbd58-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bbd58-779">Az.FrontDoor</span></span>
* <span data-ttu-id="bbd58-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="bbd58-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="bbd58-781">Unterstützung von Transformationen und neuen Wert für den Operator zum automatischen Vervollständigen (RegEx) hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="bbd58-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="bbd58-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="bbd58-783">Neue Werte für automatisches Vervollständigen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-784">Az.Network</span></span>
* <span data-ttu-id="bbd58-785">Unterstützung für Virtual Network-Gatewayressourcen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="bbd58-786">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-786">New cmdlets</span></span>
        - <span data-ttu-id="bbd58-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="bbd58-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="bbd58-788">AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bbd58-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="bbd58-789">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-789">New cmdlets</span></span> 
        - <span data-ttu-id="bbd58-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="bbd58-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="bbd58-791">„PrivatePrivateLinkService“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="bbd58-792">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-792">New cmdlets</span></span> 
        - <span data-ttu-id="bbd58-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbd58-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="bbd58-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbd58-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bbd58-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="bbd58-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="bbd58-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="bbd58-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="bbd58-798">„PrivateEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="bbd58-799">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-799">New cmdlets</span></span>
        - <span data-ttu-id="bbd58-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbd58-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bbd58-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbd58-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bbd58-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="bbd58-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="bbd58-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="bbd58-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="bbd58-804">Folgende Befehle für das Feature aktualisiert: UseLocalAzureIpAddress-Flag für „VpnConnection“</span><span class="sxs-lookup"><span data-stu-id="bbd58-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="bbd58-805">„New-AzVpnConnection§ „ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bbd58-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="bbd58-806">„Set-AzVpnConnection“ aktualisiert: Optionaler Parameter „-UseLocalAzureIpAddress“ hinzugefügt, mit dem angegeben werden kann, dass die lokale Azure-IP-Adresse beim Initiieren der Verbindung als Quelladresse verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="bbd58-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="bbd58-807">Schreibgeschütztes Feld „PeeredConnections“ beim ExpressRoute-Peering hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="bbd58-808">Schreibgeschütztes Feld „GlobalReachEnabled“ in ExpressRoute hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="bbd58-809">Breaking Change-Attribut hinzugefügt, um auf das veraltete Feld „AllowGlobalReach“ im ExpressRouteCircuit-Modell hinzuweisen</span><span class="sxs-lookup"><span data-stu-id="bbd58-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="bbd58-810">Fehler 8756 bei der Verwendung von „TargetListenerID“ mit AzApplicationGatewayRedirectConfiguration-Cmdlets behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="bbd58-811">Fehler in „New-AzApplicationGatewayPathRuleConfig“ behoben, aufgrund dessen der Regelsatz für erneutes Generieren nicht festgelegt werden konnte</span><span class="sxs-lookup"><span data-stu-id="bbd58-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="bbd58-812">Fehler bei der Anzeige von „VirtualNetworkTaps“ in „NetworkInterfaceIpConfiguration“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="bbd58-813">Cortex-Get-Cmdlets zum Auflisten aller Komponenten korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="bbd58-814">Problem beim Erstellen des festen VirtualHub-Verweises für ExpressRouteGateways behoben (VpnGateway)</span><span class="sxs-lookup"><span data-stu-id="bbd58-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="bbd58-815">Unterstützung für Verfügbarkeitszonen in AzureFirewall und NatGateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="bbd58-816">Cmdlet „Get-AzNetworkServiceTag“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="bbd58-817">Unterstützung für mehrere öffentliche IP-Adressen für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="bbd58-818">New-AzFirewall-Cmdlet aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="bbd58-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="bbd58-819">Parameter „-PublicIpAddress“ hinzugefügt, der ein oder mehre öffentliche IP-Adressobjekte akzeptiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="bbd58-820">Parameter „- VirtualNetwork“ hinzugefügt, der ein Virtual Network-Objekt akzeptiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="bbd58-821">Methoden „AddPublicIpAddress“ und „RemovePublicIpAddress“ für Firewallobjekte hinzugefügt (akzeptieren ein öffentliches IP-Adressobjekt als Eingabe)</span><span class="sxs-lookup"><span data-stu-id="bbd58-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="bbd58-822">Parameter „-PublicIpName“ und „-VirtualNetworkName“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="bbd58-823">Folgende Befehle für das Feature aktualisiert: VpnClient-AAD-Authentifizierungsoptionen auf die Gatewayressource des virtuellen Netzwerkgateways festgelegt</span><span class="sxs-lookup"><span data-stu-id="bbd58-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="bbd58-824">„New-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bbd58-825">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionale Parameter „AadTenantUri“, „AadAudienceId“ und „AadIssuerUri“ zum Festlegen der VpnClient-AAD-Authentifizierungsoptionen auf dem Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="bbd58-826">„Set-AzVirtualNetworkGateway“ aktualisiert: Optionaler Switch-Parameter „RemoveAadAuthentication“ zum Entfernen von VpnClient-AAD-Authentifizierungsoptionen aus dem Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-828">Tarif **pergb2018** im Befehl „New-AzureRmOperationalInsightsWorkspace“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="bbd58-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-829">Az.Resources</span></span>
* <span data-ttu-id="bbd58-830">Unterstützung für zusätzliche Optionen zum Exportieren von Vorlagen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="bbd58-831">Parameter „-SkipResourceNameParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bbd58-832">Parameter -SkipAllParameterization“ zu „Export-AzResourceGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="bbd58-833">Parameter „-Resource“ zu „Export-AzResourceGroup“ hinzugefügt, um das Filtern exportierter Ressourcen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bbd58-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-835">Problem beim Hinzufügen des Zertifikats mit „ByExistingKeyVault“ behoben (Abruf des falschen Fingerabdrucks in manchen Fällen)</span><span class="sxs-lookup"><span data-stu-id="bbd58-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-836">Az.Sql</span></span>
* <span data-ttu-id="bbd58-837">Suffix des Advanced Threat Protection-Endpunkts korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="bbd58-838">Durch Advanced Data Security ermöglichte Außerkraftsetzungen der Advanced Threat Protection-Richtlinie korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="bbd58-839">Neue Cmdlets für „Management.Sql“ ermöglichen Kunden das Hinzufügen von TDE-Schlüsseln und Festlegen der TDE-Schutzvorrichtung für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="bbd58-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbd58-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bbd58-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbd58-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bbd58-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbd58-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="bbd58-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bbd58-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="bbd58-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="bbd58-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-845">Az.Storage</span></span>
* <span data-ttu-id="bbd58-846">Unterstützung von „FileStorage“ und „SkuName Premium_ZRS“ beim Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bbd58-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="bbd58-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="bbd58-848">Überarbeitete Beschreibung des Cmdlets für die Unveränderlichkeit von Blobs</span><span class="sxs-lookup"><span data-stu-id="bbd58-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="bbd58-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-850">Az.Websites</span></span>
* <span data-ttu-id="bbd58-851">Optimiert „Get-AzWebAppCertificate“, um nach der Ressourcengruppe auf dem Server zu filtern (nicht auf dem Client)</span><span class="sxs-lookup"><span data-stu-id="bbd58-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="bbd58-852">Switch-Parameter „-UseDisasterRecovery“ für „Get-AzWebAppSnapshot“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="bbd58-853">2.2.0 – Juni 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="bbd58-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-854">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-855">Es wurden Cmdlets aktualisiert, um das rulesEngine-Feature basierend auf der API-Version 2019-04-15 zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-856">Az.Compute</span></span>
* <span data-ttu-id="bbd58-857">Der Parameter `NoWait` wurde hinzugefügt, der den Vorgang startet und sofort zurückkehrt, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bbd58-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="bbd58-858">Aktualisierte Cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bbd58-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bbd58-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-859">Az.EventHub</span></span>
* <span data-ttu-id="bbd58-860">Fehlerbehebung für #9231 – Get-AzEventHubNamespace gibt keine Tags zurück</span><span class="sxs-lookup"><span data-stu-id="bbd58-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="bbd58-861">Fehlerbehebung für #9230 – Get-AzEventHubNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="bbd58-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-862">Az.Network</span></span>
* <span data-ttu-id="bbd58-863">ResourceId und InputObject wurden für NAT Gateway aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="bbd58-864">Es wurde ein Alias für ResourceId und InputObjectr hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bbd58-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="bbd58-866">Fehlerbehebung für Nullverweis in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="bbd58-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-868">Minimale Aufbewahrung in Tagen für IaaSVM-Richtlinie wurde von 1 in 7 geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-869">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-870">Fehlerbehebung für #9182 – Get-AzServiceBusNamespace gibt ResourceGroup anstelle von ResourceGroupName zurück</span><span class="sxs-lookup"><span data-stu-id="bbd58-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-872">Tippfehler in Fehlermeldung für Update-AzServiceFabricReliability wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="bbd58-873">Fehlendes Zeichen in Service Fabric-Befehlszeilen wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-874">Az.Sql</span></span>
* <span data-ttu-id="bbd58-875">Der DnsZonePartner-Parameter für das Cmdlet New-AzureSqlInstance wurde hinzugefügt, um AutoDr für verwaltete Instanzen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bbd58-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="bbd58-876">Das Cmdlet Get-AzSqlDatabaseSecureConnectionPolicy wird eingestellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="bbd58-877">Cmdlets zum Schutz vor Bedrohungen werden in „Advanced Threat Protection“ (Erweiterter Schutz vor Bedrohungen) umbenannt</span><span class="sxs-lookup"><span data-stu-id="bbd58-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="bbd58-878">New-AzSqlInstance – Die Parameter StorageSizeInGB und LicenseType sind jetzt optional</span><span class="sxs-lookup"><span data-stu-id="bbd58-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-879">Az.Websites</span></span>
* <span data-ttu-id="bbd58-880">Das Problem, bei dem die Verwendung von Set-AzWebApp und Set-AzWebAppSlot mit der -WebApp-Eigenschaft die Tags entfernt hat, wurde behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="bbd58-881">2.1.0 – Mai 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="bbd58-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-882">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-883">Es wurden neue Cmdlets zum Verwalten der Diagnose im globalen sowie im API-Bereich erstellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="bbd58-884">**Get-AzApiManagementDiagnostic**: Abrufen der Diagnose, die im globalen oder im API-Bereich konfiguriert wurde</span><span class="sxs-lookup"><span data-stu-id="bbd58-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="bbd58-885">**New-AzApiManagementDiagnostic**: Erstellen neuer Diagnosen im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bbd58-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="bbd58-886">**New-AzApiManagementHttpMessageDiagnostic**: Erstellen einer Diagnoseeinstellung für die zu protokollierenden Kopfzeilen und für die Größe der Bytes für den Text</span><span class="sxs-lookup"><span data-stu-id="bbd58-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="bbd58-887">**New-AzApiManagementPipelineDiagnosticSetting**: Erstellen von Diagnoseeinstellungen für ein-/ausgehende HTTP-Nachrichten für das Gateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="bbd58-888">**New-AzApiManagementSamplingSetting**: Erstellen der Einstellung „Sampling“ für die Anforderungen/Antworten für eine Diagnose</span><span class="sxs-lookup"><span data-stu-id="bbd58-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="bbd58-889">**Remove-AzApiManagementDiagnostic**: Entfernen einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bbd58-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="bbd58-890">**Set-AzApiManagementDiagnostic**: Aktualisieren einer Diagnoseentität im globalen oder API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bbd58-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="bbd58-891">Es wurden neue Cmdlets für die Cacheverwaltung im ApiManagement-Dienst erstellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="bbd58-892">**Get-AzApiManagementCache**: Abrufen der Details des durch den Bezeichner angegebenen Caches oder aller Caches</span><span class="sxs-lookup"><span data-stu-id="bbd58-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="bbd58-893">**New-AzApiManagementCache**: Erstellen eines neuen „standardmäßigen“ Caches oder eines Caches in einer bestimmten „Region“ von Azure</span><span class="sxs-lookup"><span data-stu-id="bbd58-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="bbd58-894">**Remove-AzApiManagementCache**: Entfernen eines Caches</span><span class="sxs-lookup"><span data-stu-id="bbd58-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="bbd58-895">**Update-AzApiManagementCache**: Aktualisieren eines Caches</span><span class="sxs-lookup"><span data-stu-id="bbd58-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="bbd58-896">Es wurden neue Cmdlets zur Verwaltung von API-Schemas erstellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="bbd58-897">**New-AzApiManagementSchema**: Erstellen eines neuen Schemas für eine API</span><span class="sxs-lookup"><span data-stu-id="bbd58-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="bbd58-898">**Get-AzApiManagementSchema**: Abrufen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bbd58-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="bbd58-899">**Remove-AzApiManagementSchema**: Entfernen des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bbd58-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="bbd58-900">**Set-AzApiManagementSchema**: Aktualisieren des in der API konfigurierten Schemas</span><span class="sxs-lookup"><span data-stu-id="bbd58-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="bbd58-901">Es wurde ein neues Cmdlet zum Generieren eines Benutzertokens erstellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="bbd58-902">**New-AzApiManagementUserToken**: Generieren eines neuen Benutzertokens, das standardmäßig für acht Stunden gültig ist. Mit diesem Cmdlet kann das Token für den „GIT“-Benutzer generiert werden./</span><span class="sxs-lookup"><span data-stu-id="bbd58-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="bbd58-903">Es wurde ein neues Cmdlet zum Abrufen des Netzwerkstatus erstellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="bbd58-904">**Get-AzApiManagementNetworkStatus**: Abrufen der Netzwerkstatuskonnektivität von Ressourcen, von denen der API Management-Dienst abhängig ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="bbd58-905">Dies ist hilfreich, wenn Sie den ApiManagement-Dienst in einem virtuellen Netzwerk bereitstellen und überprüfen, ob eine der Abhängigkeiten fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="bbd58-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="bbd58-906">Das Cmdlet **New-AzApiManagement** wurde zum Verwalten des ApiManagement-Diensts aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="bbd58-907">Die Unterstützung für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="bbd58-908">Die Unterstützung zum Aktivieren des Flags „EnableClientCertificate“ für die neue SKU „Consumption“ wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="bbd58-909">Das neue Cmdlet **New-AzApiManagementSslSetting** ermöglicht die Konfiguration der „TLS/SSL“-Einstellung für „Back-End“ und „Front-End“</span><span class="sxs-lookup"><span data-stu-id="bbd58-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="bbd58-910">Dies kann auch dazu verwendet werden, um „Verschlüsselungen“ wie „3DES“ und „ServerProtokolle“ wie „Http2“ für das „Front-End“ eines ApiManagement-Diensts zu konfigurieren</span><span class="sxs-lookup"><span data-stu-id="bbd58-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="bbd58-911">Die Unterstützung für die Konfiguration des Hostnamens „DeveloperPortal“ wurde zum ApiManagement-Dienst hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="bbd58-912">Die **Get-AzApiManagementSsoToken**-Cmdlets wurden aktualisiert, um das Objekt „PsApiManagement“ als Eingabe zu übernehmen</span><span class="sxs-lookup"><span data-stu-id="bbd58-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="bbd58-913">Das Cmdlet wurde aktualisiert, um Fehlermeldungen inline anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="bbd58-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="bbd58-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Fehlercode: ValidationError-Fehlermeldung: Mindestens ein Feld enthält ungültige Werte: Fehlerdetails: [Code=ValidationError, Message=Fehler in Element 'log-to-eventhub' in Zeile 3, Spalte 10: Protokollierungstool nicht gefunden, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="bbd58-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="bbd58-915">Cmdlet **Export-AzApiManagementApi** wurde für den Export von APIs im Format „OpenApi 3.0“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="bbd58-916">Cmdlet **Import-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bbd58-917">Zum Importieren der API aus der „OpenApi 3.0“-Dokumentspezifikation</span><span class="sxs-lookup"><span data-stu-id="bbd58-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="bbd58-918">Zur Außerkraftsetzung der „PsApiManagementSchema“-Eigenschaft, die in einem beliebigen Dokument („Swagger“, „Wadl“, „Wsdl“, „OpenApi“) angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="bbd58-919">Zur Außerkraftsetzung der „ServiceUrl“-Eigenschaft, die in einem beliebigen Dokument angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="bbd58-920">Cmdlet **Get-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="bbd58-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="bbd58-921">Cmdlet **Set-AzApiManagementPolicy** wurde aktualisiert, um die Richtlinie im Format ohne XML-Escapezeichen mit „rawxml“ und im Format mit XML-Escapezeichen mit „xml“ zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="bbd58-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="bbd58-922">Cmdlet **New-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="bbd58-923">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="bbd58-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bbd58-924">Zum Erstellen einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="bbd58-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="bbd58-925">Zum Klonen einer API mithilfe von „SourceApiId“ und „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="bbd58-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="bbd58-926">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bbd58-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bbd58-927">Cmdlet **Set-AzApiManagementApi** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="bbd58-928">Zum Konfigurieren der API mit dem „OpenId“-Autorisierungsserver</span><span class="sxs-lookup"><span data-stu-id="bbd58-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="bbd58-929">Zum Aktualisieren einer API in einem „ApiVersionSet“</span><span class="sxs-lookup"><span data-stu-id="bbd58-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="bbd58-930">Möglichkeit zum Konfigurieren von „SubscriptionRequired“ im API-Bereich</span><span class="sxs-lookup"><span data-stu-id="bbd58-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="bbd58-931">Cmdlet **New-AzApiManagementRevision** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="bbd58-932">Zum Klonen (Kopiertags, Produkte, Vorgänge und Richtlinien) einer vorhandenen Version mithilfe von „SourceApiRevision“</span><span class="sxs-lookup"><span data-stu-id="bbd58-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="bbd58-933">Die neue Version übernimmt die „ApiId“ des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="bbd58-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="bbd58-934">Zum Bereitstellen einer „ApiRevisionDescription“</span><span class="sxs-lookup"><span data-stu-id="bbd58-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="bbd58-935">Zur Außerkraftsetzung der „ServiceUrl“ beim Klonen einer API</span><span class="sxs-lookup"><span data-stu-id="bbd58-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="bbd58-936">Cmdlet **New-AzApiManagementIdentityProvider** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="bbd58-937">Zum Konfigurieren von „AAD“ oder „AADB2C“ mit einer „Authority“</span><span class="sxs-lookup"><span data-stu-id="bbd58-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="bbd58-938">Zum Einrichten von „SignupPolicy“, „SigninPolicy“, „ProfileEditingPolicy“ und „PasswordResetPolicy“</span><span class="sxs-lookup"><span data-stu-id="bbd58-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="bbd58-939">Cmdlet **New-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bbd58-940">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bbd58-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bbd58-941">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bbd58-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bbd58-942">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bbd58-943">Cmdlet **Set-AzApiManagementSubscription** wurde aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="bbd58-944">Zum Berücksichtigen für das neue „SubscriptonModel“ mithilfe von „Scope“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bbd58-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="bbd58-945">Zum Berücksichtigen für das alte Abonnementmodell mithilfe von „ProductId“ und „UserId“</span><span class="sxs-lookup"><span data-stu-id="bbd58-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="bbd58-946">Die Unterstützung zum Aktivieren von „AllowTracing“ auf Abonnementebene wurde hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="bbd58-947">Folgende Cmdlets wurden aktualisiert, um „ResourceId“ als Eingabe zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="bbd58-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="bbd58-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="bbd58-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="bbd58-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="bbd58-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="bbd58-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="bbd58-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="bbd58-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="bbd58-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="bbd58-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bbd58-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="bbd58-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="bbd58-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="bbd58-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="bbd58-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="bbd58-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="bbd58-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="bbd58-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="bbd58-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="bbd58-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="bbd58-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="bbd58-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="bbd58-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="bbd58-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-960">Az.Automation</span></span>
* <span data-ttu-id="bbd58-961">Get-AzAutomationJobOutputRecord wurde aktualisiert, um JSON- und Textdatensatzwerte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="bbd58-962">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="bbd58-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="bbd58-963">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="bbd58-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="bbd58-964">Das Verhalten von Start-AzAutomationDscCompilationJob wurde geändert, um den Auftrag einfach zu starten, anstatt auf dessen Abschluss zu warten</span><span class="sxs-lookup"><span data-stu-id="bbd58-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="bbd58-965">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="bbd58-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="bbd58-966">Fehlerbehebung für Get-AzAutomationDscNode, wenn die Verwendung von „-Name“ alle Knoten zurückgibt</span><span class="sxs-lookup"><span data-stu-id="bbd58-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="bbd58-967">Jetzt wird nur der übereinstimmende Knoten zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="bbd58-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-968">Az.Compute</span></span>
* <span data-ttu-id="bbd58-969">Parameter „ProtectFromScaleIn“ und „ProtectFromScaleSetAction“ wurden zum Cmdlet „Update-AzVmssVM“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="bbd58-970">Der jetzt festgelegte wimple-Parameter „New-AzVM“ verwendet standardmäßig einen verfügbaren Standort, wenn „East US“ (USA, Osten) nicht unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-972">Das ADLS-SDK wurde aktualisiert, um „HttpClient“ zu verwenden und Datenebenentests wurden mit dem Azure-Framework integriert</span><span class="sxs-lookup"><span data-stu-id="bbd58-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-973">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-974">Fehlerbehebung bei falschen Parameternamen in Hilfebeispielen</span><span class="sxs-lookup"><span data-stu-id="bbd58-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-975">Az.Network</span></span>
* <span data-ttu-id="bbd58-976">DisableBgpRoutePropagation-Flag wurde zur Ausgabe der effektiven Routentabelle hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="bbd58-977">Aktualisiertes Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="bbd58-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="bbd58-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="bbd58-979">Fehlerbehebung von doppeltem Bindestrich in Dokumentation von New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd58-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-980">Az.Resources</span></span>
* <span data-ttu-id="bbd58-981">Neues Cmdlet „Get-AzureRmDenyAssignment“ zum Abrufen von Ablehnungszuweisungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-982">Az.Sql</span></span>
* <span data-ttu-id="bbd58-983">„Advanced Threat Protection“-Cmdlets in „Advanced Data Security“ umbenennen und Sicherheitsrisikobewertung standardmäßig aktivieren</span><span class="sxs-lookup"><span data-stu-id="bbd58-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="bbd58-984">2.0.0: Mai 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-985">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-986">Authentifizierungsbibliothek aktualisiert, um ADFS-Probleme mit der Authentifizierung per Benutzername/Kennwort zu beheben</span><span class="sxs-lookup"><span data-stu-id="bbd58-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-988">Ausschließliche Anzeige des Bing-Haftungsausschlusses für Bing-Suchdienste</span><span class="sxs-lookup"><span data-stu-id="bbd58-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="bbd58-989">Fehler behoben, der zu einem Fehler bei der Kontoerstellung führte</span><span class="sxs-lookup"><span data-stu-id="bbd58-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-990">Az.Compute</span></span>
* <span data-ttu-id="bbd58-991">Feature für die Näherungsplatzierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="bbd58-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="bbd58-992">Die folgenden neuen Cmdlets wurden hinzugefügt:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="bbd58-993">Der neue Parameter „ProximityPlacementGroupId“ wurde zu den folgenden Cmdlets hinzugefügt:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="bbd58-994">Der Parameter „StorageAccountType“ wurde zu „New-AzGalleryImageVersion“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="bbd58-995">„TargetRegion“ von „New-AzGalleryImageVersion“ kann „StorageAccountType“ enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="bbd58-996">Switch-Parameter „SkipShutdown“ wurde zu „Stop-AzVM“ und „Stop-AzVmss“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="bbd58-997">Wichtige Änderungen</span><span class="sxs-lookup"><span data-stu-id="bbd58-997">Breaking changes</span></span>
    - <span data-ttu-id="bbd58-998">„Set-AzVMBootDiagnostics“ in „Set-AzVMBootDiagnostic“ geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="bbd58-999">„Export-AzLogAnalyticThrottledRequests“ in „Export-AzLogAnalyticThrottledRequests“ geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="bbd58-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="bbd58-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="bbd58-1001">Erste allgemein verfügbare Version der Azure-Bereitstellungs-Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="bbd58-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="bbd58-1002">Az.Dns</span></span>
* <span data-ttu-id="bbd58-1003">Automatische Delegierung des DNS-Namenservers</span><span class="sxs-lookup"><span data-stu-id="bbd58-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="bbd58-1004">Das Cmdlet zum Erstellen einer DNS-Zone akzeptiert den übergeordneten Zonennamen als zusätzlichen optionalen Parameter.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="bbd58-1005">NS-Einträge in der übergeordneten Zone für neu erstellte untergeordnete Zone hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="bbd58-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="bbd58-1007">Erste allgemein verfügbare Version der Azure Frontdoor-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="bbd58-1008">WAF-Cmdlets so umbenannt, dass sie „Waf“ enthalten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="bbd58-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bbd58-1009">Az.HDInsight</span></span>
* <span data-ttu-id="bbd58-1010">Zwei Cmdlets entfernt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="bbd58-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bbd58-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="bbd58-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bbd58-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bbd58-1013">Neues Cmdlet „Set-AzHDInsightGatewayCredential“ hinzugefügt, um „Grant-AzHDInsightHttpServicesAccess“ zu ersetzen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="bbd58-1014">Cmdlet „Get-AzHDInsightJobOutput“ aktualisiert, um zwischen Leserrolle und HDInsight-Bedienerrolle zu unterscheiden:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="bbd58-1015">Benutzer mit der Rolle „Leser“ müssen den Parameter „DefaultStorageAccountKey“ explizit angeben, andernfalls treten Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="bbd58-1016">Benutzer mit der Rolle des HDInsight-Bedieners sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1017">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-1018">Neue Cmdlets für SQR-API (Scheduled Query Rule, geplante Abfrageregel)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="bbd58-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="bbd58-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="bbd58-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="bbd58-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="bbd58-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="bbd58-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="bbd58-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="bbd58-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="bbd58-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="bbd58-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="bbd58-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="bbd58-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bbd58-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bbd58-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bbd58-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bbd58-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="bbd58-1030">[Weitere Informationen](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) zur SQR-API</span><span class="sxs-lookup"><span data-stu-id="bbd58-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="bbd58-1031">„Az.Monitor.md“ aktualisiert, um Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch) einzuschließen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1032">Az.Network</span></span>
* <span data-ttu-id="bbd58-1033">Unterstützung für NAT-Gatewayressource hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="bbd58-1034">Neue Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-1034">New cmdlets</span></span>
        - <span data-ttu-id="bbd58-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="bbd58-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="bbd58-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="bbd58-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="bbd58-1039">Aktualisierte Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="bbd58-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bbd58-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="bbd58-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="bbd58-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="bbd58-1042">Folgende Befehle für das Feature aktualisiert: Benutzerdefinierte Routen für Brooklyn-Gateway festgelegt/entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="bbd58-1043">„New-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="bbd58-1044">„Set-AzVirtualNetworkGateway“ aktualisiert: Zusätzlicher optionaler Parameter „-CustomRoute“ hinzugefügt, um die Adresspräfixe als benutzerdefinierte Routen für das Gateway festlegen zu können.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bbd58-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="bbd58-1046">Unterstützung für die Abfrage von Richtlinienauswertungsdetails</span><span class="sxs-lookup"><span data-stu-id="bbd58-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="bbd58-1047">Parameter „-Expand“ zu „Get-AzPolicyState“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="bbd58-1048">Unterstützung für „-Expand PolicyEvaluationDetails“</span><span class="sxs-lookup"><span data-stu-id="bbd58-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-1050">Unterstützung für abonnementübergreifende Azure-zu-Azure-Sitewiederherstellung</span><span class="sxs-lookup"><span data-stu-id="bbd58-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="bbd58-1051">Markierung anstehender wichtiger Änderungen für Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="bbd58-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="bbd58-1052">Fehlerbehebung für Azure Site Recovery-Wiederherstellungsplan und -Aktionsplan</span><span class="sxs-lookup"><span data-stu-id="bbd58-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="bbd58-1053">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Netzwerkzuordnung für Azure zu Azure</span><span class="sxs-lookup"><span data-stu-id="bbd58-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="bbd58-1054">Fehlerbehebung für die Aktualisierung der Azure Site Recovery-Schutzrichtung für Azure zu Azure für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="bbd58-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="bbd58-1055">Weitere kleinere Korrekturen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="bbd58-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bbd58-1056">Az.Relay</span></span>
* <span data-ttu-id="bbd58-1057">Korrektur von Tippfehlern in Kundennachrichten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-1059">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1060">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1061">Upgrade auf Speicherclientbibliothek 10.0.1 (Namespace aller Objekte von diesem SDK von „Microsoft.WindowsAzure.Storage. *“ in „Microsoft.Azure.Storage.* “ geändert)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="bbd58-1062">Upgrade auf Microsoft.Azure.Management.Storage 11.0.0, um die neue API-Version 2019-04-01 zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="bbd58-1063">Art des Standardspeicherkontos bei der Speicherkontoerstellung von „Storage“ in „StorageV2“ geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="bbd58-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="bbd58-1065">Vom Speicherkonto-Cmdlet ausgegebener SKU-Name (Sku.Name) durch Hinzufügen eines Unterstrichs an SKU-Eingabename angepasst (Beispiel: „StandardLRS“ > „Standard_LRS“).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="bbd58-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="bbd58-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="bbd58-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1069">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1070">Die Eigenschaft „Kind“ wird nun für PSSite-Objekte festgelegt, die von „Get-AzWebApp“ zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="bbd58-1071">„Get-AzWebApp\*Metrics“ und „Get-AzAppServicePlanMetrics“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="bbd58-1072">1.8.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bbd58-1073">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bbd58-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="bbd58-1074">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bbd58-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="bbd58-1075">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bbd58-1076">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bbd58-1077">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bbd58-1078">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bbd58-1079">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bbd58-1080">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1081">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1082">„Uninstall-AzureRm“ aktualisiert, um Module unter Mac ordnungsgemäß zu löschen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="bbd58-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bbd58-1083">Az.Batch</span></span>
* <span data-ttu-id="bbd58-1084">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bbd58-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-1085">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-1086">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-1088">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1089">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1090">Problem mit der AEM-Installation behoben, wenn die Ressourcen-IDs von Datenträgern Ressourcengruppen in Kleinbuchstaben enthielten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="bbd58-1091">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1092">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-1093">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-1094">„SsisProperties“ hinzugefügt, falls „NodeCount“ für verwaltete Integration Runtime nicht NULL ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1096">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bbd58-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bbd58-1097">Az.EventGrid</span></span>
* <span data-ttu-id="bbd58-1098">Hilfetext für Endpunkt aktualisiert, um anzugeben, dass Ressourcen erstellt werden müssen, bevor die Cmdlets zum Erstellen/Aktualisieren von Ereignisabonnements verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bbd58-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-1099">Az.EventHub</span></span>
* <span data-ttu-id="bbd58-1100">Neue Cmdlets für „NetworkRuleSet“ des Namespace hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="bbd58-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="bbd58-1101">Az.HDInsight</span></span>
* <span data-ttu-id="bbd58-1102">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-1103">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-1104">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bbd58-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-1105">Az.KeyVault</span></span>
* <span data-ttu-id="bbd58-1106">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1107">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="bbd58-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bbd58-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="bbd58-1109">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="bbd58-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bbd58-1110">Az.Media</span></span>
* <span data-ttu-id="bbd58-1111">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1112">Az.Monitor</span></span>
  * <span data-ttu-id="bbd58-1113">Neue Cmdlets für metrikbasierte GenV2-Warnungsregel (nicht klassisch)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="bbd58-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="bbd58-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="bbd58-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="bbd58-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="bbd58-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bbd58-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bbd58-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bbd58-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="bbd58-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="bbd58-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="bbd58-1119">Monitor SDK auf Version 0.22.0-preview aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1120">Az.Network</span></span>
* <span data-ttu-id="bbd58-1121">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1122">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="bbd58-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="bbd58-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="bbd58-1124">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-1126">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="bbd58-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="bbd58-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="bbd58-1128">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-1130">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1131">Tabellenformat für SQL auf Azure-VM aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="bbd58-1132">Alternative Methode zum Abrufen des Speicherorts in „AzureFileShare“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="bbd58-1133">„ScheduleRunDays“ in SchedulePolicy-Objekt gemäß Zeitzone aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bbd58-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bbd58-1134">Az.RedisCache</span></span>
* <span data-ttu-id="bbd58-1135">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1136">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1137">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1138">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1139">Abhängigkeit vom Monitor SDK durch allgemeinen Code ersetzt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="bbd58-1140">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1141">Verbesserter Prozess für Klassifizierung mehrerer Spalten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="bbd58-1142">SKU-Eigenschaften (SKU-Name, Familie, Kapazität) in Antwort von „Get-AzSqlServerServiceObjective“ aufgenommen und standardmäßig als Tabelle formatiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="bbd58-1143">Möglichkeit zum Ausführen von „Get-AzSqlServerServiceObjective“ nach Standort, ohne dass bereits ein Server in der Region vorhanden sein muss</span><span class="sxs-lookup"><span data-stu-id="bbd58-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="bbd58-1144">Unterstützung für Zeitzonenparameter bei der Erstellung einer verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="bbd58-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="bbd58-1145">Dokumentation für Platzhalter korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1146">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1147">„Set-AzWebApp“ und „Set-AzWebAppSlot“ korrigiert, sodass die Tags bei der Ausführung nicht entfernt werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="bbd58-1148">Cmdlets, die Nomen im Plural enthalten, auf Nomen im Singular aktualisiert. Namen im Plural wurden als veraltet gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="bbd58-1149">WebSites SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="bbd58-1150">AdminSiteName-Eigenschaft aus „PSAppServicePlan“ entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="bbd58-1151">1.7.0: April 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bbd58-1152">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bbd58-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="bbd58-1153">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bbd58-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="bbd58-1154">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bbd58-1155">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bbd58-1156">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bbd58-1157">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bbd58-1158">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bbd58-1159">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1160">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1161">„Add-AzEnvironment“ und „Set-AzEnvironment“ aktualisiert, um den Parameter „AzureAnalysisServicesEndpointResourceId“ zu akzeptieren</span><span class="sxs-lookup"><span data-stu-id="bbd58-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bbd58-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="bbd58-1163">ServiceClient wird in Cmdlets für die Datenebene verwendet, und die ursprüngliche Authentifizierungslogik wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="bbd58-1164">„Add-AzureASAccount“ wird als Wrapper von „Connect-AzAccount“ festgelegt, um einen Breaking Change zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1165">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1166">Fehler des Cmdlets „Fixed New-AzAutomationSoftwareUpdateConfiguration“ für Einschlüsse behoben.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="bbd58-1167">Die Parameter „IncludedKbNumber“ und „IncludedPackageNameMask“ sollten nun funktionieren.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="bbd58-1168">Fehlerbehebung für eine dynamische Gruppe der Azure Automation-Updateverwaltung</span><span class="sxs-lookup"><span data-stu-id="bbd58-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1169">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1170">Parameter „HyperVGeneration“ zu „New-AzDiskConfig“ und „New-AzSnapshotConfig“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="bbd58-1171">Zulassen der VM-Erstellung mit einem Katalogimage aus anderen Mandanten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="bbd58-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="bbd58-1173">Problem im Parameter „-Command“ von „New-AzContainerGroup“ behoben, das dazu führte, dass ein nachgestelltes leeres Argument hinzugefügt wurde</span><span class="sxs-lookup"><span data-stu-id="bbd58-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-1174">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-1175">Version des ADF .NET SDK auf 3.0.2 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="bbd58-1176">Cmdlet „Set-AzDataFactoryV2“ mit zusätzlichen Parametern für RepoConfiguration-Einstellungen aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1177">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1178">Verarbeitung von Anbietern für „Get-AzResource“ bei der Angabe der Parameter „-ResourceId“ oder „-ResourceGroupName“, „-Name“ und „-ResourceType“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="bbd58-1179">Fehlerbehandlung für „Test-AzDeployment“ und „Test-AzResourceGroupDeployment“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="bbd58-1180">Behandlung von außerhalb der Bereitstellungsüberprüfung aufgetretenen Fehlern und stattdessen Aufnahme in die Ausgabe des Befehls</span><span class="sxs-lookup"><span data-stu-id="bbd58-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="bbd58-1181">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bbd58-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="bbd58-1182">Switch-Parameter „-IgnoreDynamicParameters“ zu Bereitstellungs-Cmdlets hinzugefügt, um Aufforderung in Skript- und Auftragsszenarien zu überspringen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="bbd58-1183">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="bbd58-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1184">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1185">Unterstützung für Klassifizierung von Datenbankdaten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1186">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1187">Melden eines ausführlichen Fehlers beim Erstellen des Storage-Kontexts mit dem Parameter „-UseConnectedAccount“, aber ohne Azure-Anmeldekonto</span><span class="sxs-lookup"><span data-stu-id="bbd58-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="bbd58-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbd58-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="bbd58-1189">Unterstützung für das Verwalten von Blobdiensteigenschaften eines bestimmten Storage-Kontos mit einer API der Verwaltungsebene</span><span class="sxs-lookup"><span data-stu-id="bbd58-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="bbd58-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bbd58-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bbd58-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bbd58-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="bbd58-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="bbd58-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="bbd58-1194">Unterstützung von „-AsJob“ für Cmdlets für den Upload und Download von Blobs und Dateien</span><span class="sxs-lookup"><span data-stu-id="bbd58-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="bbd58-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bbd58-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="bbd58-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="bbd58-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bbd58-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="bbd58-1199">1.6.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="bbd58-1200">Highlights seit der letzten Hauptversion</span><span class="sxs-lookup"><span data-stu-id="bbd58-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="bbd58-1201">Allgemeine Verfügbarkeit des `Az`-Moduls</span><span class="sxs-lookup"><span data-stu-id="bbd58-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="bbd58-1202">Weitere Informationen zum `Az`-Modul finden Sie unter folgendem Link: https://aka.ms/azps-announce.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="bbd58-1203">Vervollständigung für Location, ResourceGroup und ResourceName hinzugefügt: https://azure.microsoft.com/blog/completers-in-azure-powershell/.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="bbd58-1204">Unterstützung für Platzhalter zu Get-Cmdlets für Az.Compute und Az.Network hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="bbd58-1205">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bbd58-1206">Unterstützung für Python 2-Runbooks in Az.Automation hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="bbd58-1207">Az.LogicApp: Neue Cmdlets für Integrationskonto-Assemblys und -Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1208">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1209">Änderung an der Azure Automation-Updateverwaltung, um die folgenden neuen Features zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="bbd58-1210">Dynamische Gruppierung</span><span class="sxs-lookup"><span data-stu-id="bbd58-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="bbd58-1211">Pre-/Post-Skripts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1211">Pre-Post script</span></span>
    * <span data-ttu-id="bbd58-1212">Neustarteinstellung</span><span class="sxs-lookup"><span data-stu-id="bbd58-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1213">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1214">Problem mit der Pfadauflösung in „Get-AzVmBootDiagnosticsData“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="bbd58-1215">Computeclientbibliothek auf 25.0.0. aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bbd58-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-1216">Az.KeyVault</span></span>
* <span data-ttu-id="bbd58-1217">Unterstützung für Platzhalterzeichen zu KeyVault-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1218">Az.Network</span></span>
* <span data-ttu-id="bbd58-1219">Threat Intelligence-Unterstützung für Azure Firewall hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="bbd58-1220">Ressource der obersten Ebene für Application Gateway-Firewallrichtlinie und benutzerdefinierte Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-1222">SnapshotRetentionInDays in Azure-VM-Richtlinie hinzugefügt, um sofortigen Wiederherstellungspunkt zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="bbd58-1223">Pipe-Unterstützung für das Aufheben der Registrierung eines Containers hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1224">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1225">Unterstützung für Platzhalterzeichen für Get-AzResource und Get-AzResourceGroup aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="bbd58-1226">Anmeldeinformationen aktualisiert, die beim Senden generischer Aufrufe an ARM verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1227">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1228">Der Cmdlet-Parameter der Bedrohungserkennung (ExcludeDetectionType) wurde von „DetectionType“ in „string[]“ geändert, um ihn zukunftssicher zu machen, wenn neue DetectionTypes-Elemente hinzugefügt werden, und um AutoVervollständigen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1229">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1230">Unterstützung von Get-/Set-/Remove-Verwaltungsrichtlinien für Speicherkonto hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="bbd58-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bbd58-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bbd58-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="bbd58-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="bbd58-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="bbd58-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bbd58-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="bbd58-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1237">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1238">ARM-Vorlagenfehler behoben, der zu einem Problem beim Klonen aller Slots mithilfe von „New-AzWebApp -IncludeSourceWebAppSlots“ führte</span><span class="sxs-lookup"><span data-stu-id="bbd58-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="bbd58-1239">1.5.0: März 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1240">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1241">Der Befehl „Register-AzModule“ wurde hinzugefügt, um von AutoRest generierte Cmdlets zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="bbd58-1242">Beispiele für „Connect-AzAccount“ wurden aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1243">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1244">Problem behoben, das beim Abrufen bestimmter monatlicher Zeitpläne in verschiedenen Azure Automation-Cmdlets auftrat</span><span class="sxs-lookup"><span data-stu-id="bbd58-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="bbd58-1245">„Get-AzAutomationDscNode“ wurde korrigiert, da nur die 20 obersten Knoten zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="bbd58-1246">Jetzt werden alle Knoten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bbd58-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-1247">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-1248">Neue Powershell-Cmdlets zum Aktivieren/Deaktivieren von HTTPS für benutzerdefinierte Domänen hinzugefügt und alte Cmdlets außer Betrieb genommen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1249">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1250">Unterstützung für Platzhalterzeichen zu Get-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-1251">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-1252">Version des ADF .NET SDK auf 3.0.1 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bbd58-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bbd58-1253">Az.LogicApp</span></span>
* <span data-ttu-id="bbd58-1254">„ListWorkflows“ wurde korrigiert, da nur die erste Seite mit Ergebnissen abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1255">Az.Network</span></span>
* <span data-ttu-id="bbd58-1256">Unterstützung für Platzhalterzeichen zu Network-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-1258">SQL Server jetzt in Azure-VM-Support enthalten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="bbd58-1259">SDK-Update</span><span class="sxs-lookup"><span data-stu-id="bbd58-1259">SDK Update</span></span>
* <span data-ttu-id="bbd58-1260">VMappContainer-Überprüfung in „Get-ProtectableItem“ entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="bbd58-1261">„Name“ und „ServerName“ als Parameter für „Get-ProtectableItem“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1262">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1263">Parameter `-TemplateObject` zu Bereitstellungs-Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="bbd58-1264">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="bbd58-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="bbd58-1265">Problem beim Piping des Ergebnisses von `Get-AzResource` an `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="bbd58-1266">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="bbd58-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="bbd58-1267">Problem mit JSON-Datentypänderung beim Ausführen von `Set-AzResource` behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="bbd58-1268">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="bbd58-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1269">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1270">„AuditingEndpointsCommunicator“ wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="bbd58-1271">Das Verhalten eines Grenzfalls beim Erstellen neuer Diagnoseeinstellungen wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1272">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1273">Unterstützung von „Kind BlockBlobStorage“ beim Erstellen eines Speicherkontos: New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbd58-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="bbd58-1274">1.4.0 – Februar 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="bbd58-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="bbd58-1276">Cmdlet „AddAzureASAccount“ als veraltet markiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1277">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1278">Hilfe für „Import-AzAutomationDscNodeConfiguration“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="bbd58-1279">Überprüfung des Konfigurationsnamens zu Cmdlet „Import-AzAutomationDscConfiguration“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="bbd58-1280">Fehlerbehandlung für Cmdlet „Import-AzAutomationDscConfiguration“ verbessert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-1282">„CustomSubdomainName“ als neuer optionaler Parameter für Cmdlet „New-AzCognitiveServicesAccount“ hinzugefügt, das zum Angeben der Unterdomäne für die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1283">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1284">Problem mit ID-Parametersätzen behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="bbd58-1285">„Get-AzVMExtension“ aktualisiert, sodass alle installierten Erweiterungen aufgelistet werden, wenn der Name-Parameter nicht angegeben ist</span><span class="sxs-lookup"><span data-stu-id="bbd58-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="bbd58-1286">Parameter „Tag“ und „ResourceId“ zum Cmdlet „Update-AzImage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="bbd58-1287">„Get-AzVmssVM“ ohne Instanz-ID und mit „InstanceView“ können virtuelle VMSS-Computer mit Instanzansicht auflisten.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1289">Cmdlets zum Auflisten und Wiederherstellen gelöschter ADL-Elemente hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="bbd58-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-1290">Az.EventHub</span></span>
* <span data-ttu-id="bbd58-1291">Neue boolesche Eigenschaft „SkipEmptyArchives“ zum Überspringen leerer Archive in Klasse „CaptureDescription“ von EventHub hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="bbd58-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-1292">Az.KeyVault</span></span>
* <span data-ttu-id="bbd58-1293">Kennzeichnung in „Set-AzKeyVaultSecret“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bbd58-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bbd58-1294">Az.LogicApp</span></span>
* <span data-ttu-id="bbd58-1295">SKU „Basic“ für Integrationskonten hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="bbd58-1296">XSLT 2.0, XSLT 3.0 und Liquid-Zuordnungstypen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="bbd58-1297">Neue Cmdlets für Integrationskonto-Assemblys</span><span class="sxs-lookup"><span data-stu-id="bbd58-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="bbd58-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bbd58-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bbd58-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bbd58-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bbd58-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bbd58-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="bbd58-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bbd58-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="bbd58-1302">Neue Cmdlets für Integrationskonto-Batchkonfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="bbd58-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bbd58-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bbd58-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="bbd58-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="bbd58-1307">Logik-App-SDK auf Version 4.1.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="bbd58-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1308">Az.Monitor</span></span>
* <span data-ttu-id="bbd58-1309">Hilfe für „Get-AzMetric“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1310">Az.Network</span></span>
* <span data-ttu-id="bbd58-1311">Hilfebeispiel für „Add-AzApplicationGatewayCustomError“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="bbd58-1313">Zusätzliche Unterstützung für Datenquelle von „New-ApplicationInsights“ und „Get-ApplicationInsights“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="bbd58-1314">Neue Art von „ApplicationInsights“ zum Abrufen von bestimmten und von allen ApplicationInsights-Datenquellen für einen Workspace hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="bbd58-1315">Cmdlet „New-AzOperationalInsightsApplicationInsightsDataSource“ zum Erstellen einer Datenquelle anhand des angegebenen Ressourcenparameters für „Application-Insights“ hinzugefügt: „subscriptionId“, „resourceGroupName“ und „name“.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="bbd58-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1316">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1317">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bbd58-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bbd58-1318">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bbd58-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="bbd58-1319">Behebung des Problems: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="bbd58-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="bbd58-1320">Fehler korrigiert, der die wiederholte Erstellung von „KeyCredentials“ verhindert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1321">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1322">Unterstützung für SQL DB Hyperscale-Tarif hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="bbd58-1323">Fehler korrigiert, aufgrund dessen die Wiederherstellung wegen der Festlegung unnötiger Eigenschaften in der Wiederherstellungsanforderung fehlschlagen konnte</span><span class="sxs-lookup"><span data-stu-id="bbd58-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1324">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1325">Beispiel in „Get-AzWebAppSlotMetrics“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="bbd58-1326">1.3.0: Februar 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1327">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1328">Update auf die aktuelle Version von ClientRuntime durchgeführt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bbd58-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="bbd58-1330">Allgemeine Verfügbarkeit für Az.AnalysisServices-Modul</span><span class="sxs-lookup"><span data-stu-id="bbd58-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1331">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1332">AEM-Erweiterung: Unterstützung für UltraSSD und P60-, P70- und P80-Datenträger hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="bbd58-1333">Hilfebeschreibung für „Set-AzVMBootDiagnostics“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="bbd58-1334">Hilfebeschreibung und Beispiel für „Update-AzImage“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="bbd58-1336">Allgemeine Verfügbarkeit für Az.RecoveryServices-Modul.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1337">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1338">Kennzeichnung für Ressourcengruppen korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="bbd58-1339">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="bbd58-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="bbd58-1340">Problem behoben, bei dem „-ErrorAction“ von `Get-AzureRmRoleAssignment` nicht berücksichtigt wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="bbd58-1341">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="bbd58-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1342">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1343">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="bbd58-1344">Problem behoben, bei dem eine fehlende Anmeldung am Azure-Konto bei der Ausführung von SQL-Cmdlets zu einer nullref-Ausnahme führt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="bbd58-1345">nullref-Ausnahme in Get-AzSqlCapability korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="bbd58-1346">1.2.1: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1347">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1348">Release mit richtiger Version der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="bbd58-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="bbd58-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="bbd58-1350">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="bbd58-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="bbd58-1352">Release mit aktualisierter Authentifizierungsabhängigkeit</span><span class="sxs-lookup"><span data-stu-id="bbd58-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="bbd58-1353">1.2.0: Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1354">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1355">Interaktive und Benutzername/Kennwort-Authentifizierung ausschließlich für Windows PowerShell 5.1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="bbd58-1356">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bbd58-1357">Warnmeldung in PS Core für „Uninstall-AzureRm“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="bbd58-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="bbd58-1358">Az.Aks</span></span>
* <span data-ttu-id="bbd58-1359">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="bbd58-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1360">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1361">Unterstützung für Python 2-Runbooks hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="bbd58-1362">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="bbd58-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="bbd58-1363">Az.Cdn</span></span>
* <span data-ttu-id="bbd58-1364">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1365">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1366">Cmdlet „Invoke-AzVMReimage“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="bbd58-1367">Parameter „TempDisk“ zu „Set-AzVmss“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="bbd58-1368">Warnmeldung von „New-AzVM“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="bbd58-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="bbd58-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="bbd58-1370">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="bbd58-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="bbd58-1371">Az.DataFactory</span></span>
* <span data-ttu-id="bbd58-1372">Version des ADF .NET SDK auf 3.0.0 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1374">Problem mit ADLS-Endpunkt bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="bbd58-1375">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="bbd58-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="bbd58-1376">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-1377">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-1378">Codierungsformat zu Cmdlet „Add-IotHubRoutingEndpoint“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="bbd58-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-1379">Az.KeyVault</span></span>
* <span data-ttu-id="bbd58-1380">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1381">Az.Network</span></span>
* <span data-ttu-id="bbd58-1382">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1383">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1384">Fehlerhafte Beispiele in Referenzdokumentation zu „New-AzADAppCredential“ und „New-AzADSpCredential“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="bbd58-1385">Problem behoben, bei dem der Pfad für den Parameter „-TemplateFile“ nicht aufgelöst wurde, bevor Cmdlets für die Bereitstellung von Ressourcengruppen ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="bbd58-1386">Az.Resources: Richtige Dokumentation für Standardwert von „New-AzureRmPolicyDefinition -Mode“ bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="bbd58-1387">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="bbd58-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="bbd58-1388">Az.Resources: Behebung des Problems: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="bbd58-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="bbd58-1389">Formatierungsproblem für Objekt „PSResourceGroupDeployment“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="bbd58-1390">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="bbd58-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-1392">Rollback beim Hinzufügen eines Zertifikats zum VMSS-Modell, Auslösung einer Ausnahme. Fehlerbehebung: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="bbd58-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="bbd58-1393">Einige Fehlermeldungen wurden korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1393">Fix some error messages.</span></span>
* <span data-ttu-id="bbd58-1394">Fehler bei Clustererstellung mit ARM-Standardvorlage für „New-AzServiceFabriCluster“ behoben, bei dem die Migration zu Az nicht funktioniert hat.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="bbd58-1395">Fehler behoben beim Hinzufügen eines Cluster-/Anwendungszertifikats ausschließlich zu VM Scale Sets, die zum Cluster gehören, indem die Cluster-ID in der Erweiterung überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bbd58-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bbd58-1396">Az.SignalR</span></span>
* <span data-ttu-id="bbd58-1397">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1398">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1399">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bbd58-1400">Parameterbeschreibung für den Parameter „LicenseType“ mit möglichen Werten aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="bbd58-1401">Fehler behoben, bei dem die Aktualisierung der Identität der verwalteten Instanz nicht funktioniert hat, wenn es sich um die einzige aktualisierte Eigenschaft gehandelt hat</span><span class="sxs-lookup"><span data-stu-id="bbd58-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="bbd58-1402">Unterstützung für die benutzerdefinierte Sortierung auf verwalteter Instanz</span><span class="sxs-lookup"><span data-stu-id="bbd58-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1403">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1404">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bbd58-1405">Ausführliche Fehlermeldung beim Abrufen/Festlegen der klassischen Protokollierung bzw. Metriken für Storage Premium-Konto, da für das Storage Premium-Konto die klassische Protokollierung bzw. Metriken nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="bbd58-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bbd58-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="bbd58-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="bbd58-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="bbd58-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="bbd58-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="bbd58-1409">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1410">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1411">Fehlerhafte URLs für Onlinehilfe aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="bbd58-1412">„New-AzWebAppSSLBinding“ korrigiert, damit das Zertifikat in die richtige Ressourcengruppe bzw. an den richtigen Speicherort hochgeladen wird, wenn die App in einer ASE gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="bbd58-1413">„New-AzWebAppSSLBinding“ korrigiert, damit die Tags beim Binden eines SSL-Zertifikats an eine App nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="bbd58-1414">1.1.0 – Januar 2019</span><span class="sxs-lookup"><span data-stu-id="bbd58-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="bbd58-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1415">Az.Accounts</span></span>
* <span data-ttu-id="bbd58-1416">Bereich „Local“ zu „Enable-AzureRmAlias“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1417">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1418">Name ist jetzt optional im ID-Parametersatz für „Restart/Start/Stop/Remove/Set-AzVM“ und „Save-AzVMImage“</span><span class="sxs-lookup"><span data-stu-id="bbd58-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="bbd58-1419">Beschreibung der ID in Hilfedateien aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="bbd58-1420">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1422">Aktualisierung der SDK-Version der Datenebene auf 1.1.14 für SDK-Fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="bbd58-1423">Behandlung von negativen acesstime- and modificationtime-Werten für „getfilestatus“ und „liststatus“ korrigiert, asynchrones Abbruchtoken korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="bbd58-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="bbd58-1424">Az.EventGrid</span></span>
* <span data-ttu-id="bbd58-1425">Zur Verwendung der API-Version 2019-01-01 aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="bbd58-1426">Aktualisierung der folgenden Cmdlets zur Unterstützung des neuen Szenarios in der API-Version 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="bbd58-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="bbd58-1427">New-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bbd58-1428">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bbd58-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bbd58-1429">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bbd58-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bbd58-1430">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="bbd58-1431">Update-AzureRmEventGridSubscription: Neue optionale Parameter zum Angeben folgender Werte hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="bbd58-1432">Gültigkeitsdauer des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="bbd58-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="bbd58-1433">Maximale Anzahl von Übermittlungsversuchen für die Ereignisse</span><span class="sxs-lookup"><span data-stu-id="bbd58-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="bbd58-1434">Endpunkt für unzustellbare Nachrichten</span><span class="sxs-lookup"><span data-stu-id="bbd58-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="bbd58-1435">Neue Enumerationswerte („storageQueue“ und „hybridConnection“) für die EndpointType-Option in den Cmdlets „New-AzureRmEventGridSubscription“ und „Update-AzureRmEventGridSubscription“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="bbd58-1436">Anzeige einer Warnmeldung, wenn das Erstellen oder Aktualisieren des Ereignisabonnements voraussichtlich eine manuelle Aktion des Benutzers zur Folge hat</span><span class="sxs-lookup"><span data-stu-id="bbd58-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="bbd58-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="bbd58-1437">Az.IotHub</span></span>
* <span data-ttu-id="bbd58-1438">Auf die aktuelle Version des Iot Hub SDK aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="bbd58-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="bbd58-1439">Az.LogicApp</span></span>
* <span data-ttu-id="bbd58-1440">„Get-AzLogicApp“ listet alle Apps ohne angegebenen Namen auf</span><span class="sxs-lookup"><span data-stu-id="bbd58-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1441">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1442">Problem mit dem Parametersatz bei Angabe der Parameter „-ODataQuery“ und „-ResourceId“ für „Get-AzResource“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="bbd58-1443">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="bbd58-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="bbd58-1444">Behandlung des Parameters „-Custom“ in „New/Set-AzPolicyDefinition“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bbd58-1445">Tippfehler in der Dokumentation für „New-AzDeployment“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="bbd58-1446">Parameter „-MailNickname“ als obligatorisch festgelegt für „New-AzADUser“</span><span class="sxs-lookup"><span data-stu-id="bbd58-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="bbd58-1447">Weitere Informationen finden Sie hier: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="bbd58-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="bbd58-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="bbd58-1448">Az.SignalR</span></span>
* <span data-ttu-id="bbd58-1449">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1450">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1451">Abhängigkeit des Speicherverwaltungsclients zur allgemeinen SDK-Implementierung konvertiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="bbd58-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1452">Az.Storage</span></span>
* <span data-ttu-id="bbd58-1453">Festlegung des „StorageAccountName“ des Speicherkontexts als tatsächlichen Namen des Speicherkontos, wenn dieser mit „SAS-Token“, „OAuth“ oder „Anonym“ erstellt wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="bbd58-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="bbd58-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="bbd58-1455">Erstellen von SAS-Token des Blob-Momentaufnahmeobjekts mit dem Parameter „-FullUri“, Festlegung des zurückgegebenen URI als Momentaufnahme-URI</span><span class="sxs-lookup"><span data-stu-id="bbd58-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="bbd58-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="bbd58-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1457">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1458">Fehler bei der Datumsanalyse in „Get-AzDeletedWebApp“ behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="bbd58-1459">Problem mit der Abwärtskompatibilität beim Az.Accounts-Modul behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="bbd58-1460">1.0.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="bbd58-1461">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-1461">General</span></span>

- <span data-ttu-id="bbd58-1462">Allgemeine Verfügbarkeit des Az-Moduls</span><span class="sxs-lookup"><span data-stu-id="bbd58-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="bbd58-1463">Onlinehilfe für jedes Modul</span><span class="sxs-lookup"><span data-stu-id="bbd58-1463">Online help for each module</span></span>
- <span data-ttu-id="bbd58-1464">Ausführlichere Informationen und eine Roadmap finden Sie auf der [Seite mit der Ankündigung zu Az](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="bbd58-1465">Informationen zur Migration aus AzureRM finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="bbd58-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="bbd58-1466">Az.Accounts</span></span>
- <span data-ttu-id="bbd58-1467">Geändert von Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="bbd58-1468">Feste Tabellenformate für Profil- und Kontexttypen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bbd58-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="bbd58-1470">Korrekturen für #7002</span><span class="sxs-lookup"><span data-stu-id="bbd58-1470">Fixes for #7002</span></span>
- <span data-ttu-id="bbd58-1471">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="bbd58-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="bbd58-1472">Az.Batch</span></span>
- <span data-ttu-id="bbd58-1473">Möglichkeit zum Anzeigen der ausgeführten Version des Azure Batch-Knoten-Agents auf den VMs eines Pools mit der neuen `NodeAgentInformation`-Eigenschaft für `PSComputeNode` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="bbd58-1474">Der `Caching`-Standardwert für `PSDataDisk` lautet jetzt nicht mehr `None`, sondern `ReadWrite`.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="bbd58-1475">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="bbd58-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="bbd58-1476">Az.Billing</span></span>
- <span data-ttu-id="bbd58-1477">Kombination von Billing-, Consumption- und UsageAggregates-Cmdlets. Ausführliche Informationen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="bbd58-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="bbd58-1479">Vervollständigungen für SkuName und Typem für den Vorgang New-AzureRmCognitiveServicesAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="bbd58-1480">GetSkusWithAccountParamSetName-Parametersatz aus Get-AzCognitiveServicesAccountSkus entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bbd58-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="bbd58-1482">ManagedIdentity-Unterstützung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="bbd58-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="bbd58-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="bbd58-1484">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="bbd58-1486">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="bbd58-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1487">Az.Monitor</span></span>
- <span data-ttu-id="bbd58-1488">Az.Insights in Az.Monitor umbenannt und weitere weniger wichtige grundlegende Änderungen durchgeführt. Informationen hierzu finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="bbd58-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="bbd58-1489">Az.KeyVault</span></span>
- <span data-ttu-id="bbd58-1490">Veraltete PurgeDisabled-Eigenschaft aus Ausgabetypen entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="bbd58-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="bbd58-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="bbd58-1492">Cmdlets des Az.MachineLearningCompute-Moduls eingebunden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="bbd58-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="bbd58-1493">Az.Media</span></span>
- <span data-ttu-id="bbd58-1494">Veralteten -Tags-Alias aus New-AzMediaService entfernt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bbd58-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1495">Az.Network</span></span>
<span data-ttu-id="bbd58-1496">Unterstützung für das Konfigurieren von RewriteRuleSets im Application Gateway hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="bbd58-1497">Neu hinzugefügte Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="bbd58-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="bbd58-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bbd58-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="bbd58-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbd58-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="bbd58-1506">Cmdlets mit optionalem Parameter -RewriteRuleSet aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="bbd58-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbd58-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="bbd58-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bbd58-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="bbd58-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="bbd58-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="bbd58-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="bbd58-1512">New-AzureRmApplicationGatewayUrlPathMapConfig: KeyVault-Unterstützung mithilfe von Identität zum Application Gateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="bbd58-1513">Cmdlets mit optionalem Parameter aktualisiert: -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bbd58-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="bbd58-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd58-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bbd58-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd58-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="bbd58-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="bbd58-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="bbd58-1517">Cmdlet New-AzApplicationGateway mit optionalem Parameter -UserAssignedIdentity aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="bbd58-1518">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="bbd58-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="bbd58-1520">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="bbd58-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1521">Az.Profile</span></span>
- <span data-ttu-id="bbd58-1522">Modulnamen in Az.Accounts geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="bbd58-1524">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="bbd58-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1525">Az.Resources</span></span>
- <span data-ttu-id="bbd58-1526">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bbd58-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="bbd58-1528">Unterstützung für das Angeben des Zertifikats anhand des allgemeinen Namens und Fingerabdrucks</span><span class="sxs-lookup"><span data-stu-id="bbd58-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="bbd58-1529">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="bbd58-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bbd58-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="bbd58-1531">Allgemeine Verfügbarkeit für PowerShell-Cmdlets für SIgnalR</span><span class="sxs-lookup"><span data-stu-id="bbd58-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="bbd58-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1532">Az.Sql</span></span>
- <span data-ttu-id="bbd58-1533">Neue Erkennungstypen Data_Exfiltration und Unsafe_Action zu Cmdlets für Bedrohungserkennung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="bbd58-1534">Dokumentationsbeispiele für Cmdlets für SQL-Überwachung aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="bbd58-1535">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="bbd58-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1536">Az.Storage</span></span>
- <span data-ttu-id="bbd58-1537">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bbd58-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1538">Az.Websites</span></span>
- <span data-ttu-id="bbd58-1539">Informationen zu weniger wichtigen grundlegenden Änderungen finden Sie im [Migrationsleitfaden](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="bbd58-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="bbd58-1540">0.7.0 – Dezember 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="bbd58-1541">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-1541">General</span></span>

* <span data-ttu-id="bbd58-1542">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="bbd58-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="bbd58-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1543">Az.Compute</span></span>

* <span data-ttu-id="bbd58-1544">Unterstützung für UltraSSD und Katalogimages in einfachen Parametersätzen für `New-AzVm(ss)`-Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="bbd58-1546">Nachgestellten Schrägstrich für die Domäne des ADLS-Kontos korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="bbd58-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="bbd58-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="bbd58-1548">Einige fehlerhafte Links behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="bbd58-1549">In den Artikeln zu New-AzureRmFrontDoor und Set-AzureRmFrontDoor den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorHealthProbeSettingObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="bbd58-1550">Im Artikel zu New-AzureRmFrontDoorManagedRuleObject den Artikel-Link zum Cmdlet „New-AzureRmFrontDoorRuleGroupOverrideObject“ korrigiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="bbd58-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="bbd58-1552">Clientseitige Validierungen für Wiederherstellungsvorgänge von Azure-Dateifreigaben hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="bbd58-1553">storageAccountName und storageAccountResourceGroupName für AFS-Wiederherstellung optional gemacht.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="bbd58-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1554">Az.Resources</span></span>

* <span data-ttu-id="bbd58-1555">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="bbd58-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="bbd58-1556">Get-AzureRmRoleAssignment für die Verwendung des Abonnementbereichs aktualisiert, wenn dieser beim Anfordern von klassischen Administratoren angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="bbd58-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1557">Az.Sql</span></span>

* <span data-ttu-id="bbd58-1558">Geringe Änderungen für anstehenden Übergang von AzureRM zu Az</span><span class="sxs-lookup"><span data-stu-id="bbd58-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="bbd58-1559">Problem mit der Verwendung von Get-AzureRmSqlDatabaseVulnerabilityAssessment mit .NET Core behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="bbd58-1560">Dokumentation mit Hilfemeldungen zu Cmdlets für die SQL-Überwachung geändert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="bbd58-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1561">Az.Storage</span></span>

* <span data-ttu-id="bbd58-1562">-EnableHierarchicalNamespace zu New-AzureRmStorageAccount hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="bbd58-1563">Problem behoben, bei dem für das Copy File-Cmdlet am Ziel kein Quellkontext wiederverwendet werden kann, wenn -DestContext nicht eingegeben wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="bbd58-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bbd58-1565">Unterstützung der Konfiguration von statischen Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="bbd58-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bbd58-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="bbd58-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="bbd58-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="bbd58-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1568">Az.Websites</span></span>

* <span data-ttu-id="bbd58-1569">Set-AzureRmWebApp und Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bbd58-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="bbd58-1570">Neuen Parameter (-AzureStoragePath) zum Angeben von Azure Storage-Pfaden hinzugefügt, die in Windows- und Linux-Container-Apps bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="bbd58-1571">Verwenden Sie die Ausgabe des neuen Cmdlets New-AzureRmWebAppAzureStoragePath als Parameter zum Festlegen der Azure Storage-Pfade.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="bbd58-1572">0.6.1 – November 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="bbd58-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="bbd58-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="bbd58-1574">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="bbd58-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="bbd58-1575">Az.Automation</span></span>
* <span data-ttu-id="bbd58-1576">Swagger-basierte Azure Automation-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bbd58-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="bbd58-1577">Cmdlets zur Updateverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="bbd58-1578">Cmdlets zur Quellcodeverwaltung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="bbd58-1579">Cmdlet „Remove-AzureRmAutomationHybridWorkerGroup“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="bbd58-1580">DSC-Befehl für die Knotenregistrierung korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="bbd58-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1581">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1582">Identitätsproblem für SystemAssigned-Identität korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="bbd58-1583">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="bbd58-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="bbd58-1585">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="bbd58-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="bbd58-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="bbd58-1587">Beschreibung der Beispiele für Marketplace-Cmdlets aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="bbd58-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1588">Az.Network</span></span>
* <span data-ttu-id="bbd58-1589">Folgende Cmdlets hinzugefügt: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="bbd58-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="bbd58-1590">ICMP wieder unterstützten AzureFirewall-Netzwerkprotokollen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="bbd58-1591">Cmdlet „Test-AzureRmNetworkWatcherConnectivity“ aktualisiert und Überprüfung für Ziel-ID, Adresse und Port hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="bbd58-1592">Probleme mit Arbeitsspeicherauslastung in der VirtualNetwork-Zuordnung behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="bbd58-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="bbd58-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="bbd58-1594">Problem beim Ändern der Richtlinie für eine geschützte Dateifreigabe behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="bbd58-1595">Richtlinienzeitzone in Großschreibung geändert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="bbd58-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="bbd58-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="bbd58-1597">Korrigiertes Beispiel in „New-AzureRmRecoveryServicesAsrProtectableItem“</span><span class="sxs-lookup"><span data-stu-id="bbd58-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="bbd58-1598">Abhängigkeiten für Typzuordnungsproblem aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="bbd58-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="bbd58-1599">Az.Relay</span></span>
* <span data-ttu-id="bbd58-1600">Optionaler Parameter „-KeyValue“ zu Cmdlet „New-AzureRmRelayKey“ hinzugefügt, der dem Benutzer das Angeben von „KeyValue“ ermöglicht</span><span class="sxs-lookup"><span data-stu-id="bbd58-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="bbd58-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1601">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1602">Hilfedokumentation für ressourcenidentitätsbezogene Parameter in `New-AzureRmPolicyAssignment` und `Set-AzureRmPolicyAssignment` aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="bbd58-1603">Beispiel für „New-AzureRmPolicyDefinition“ hinzugefügt, das „-Metadata“ nutzt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="bbd58-1604">Korrektur, um Beibehaltung von Groß-/Kleinschreibung in Tagschlüsseln in „NetStandard“ zu ermöglichen: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="bbd58-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="bbd58-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-1606">Benachrichtigung über veraltete Elemente für anstehende wichtige Änderungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="bbd58-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1607">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1608">Neue Cmdlets für CRUD-Vorgänge in verwalteten Azure SQL-Datenbank-Instanzen und verwalteten Azure SQL-Datenbanken hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="bbd58-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bbd58-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bbd58-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bbd58-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="bbd58-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="bbd58-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bbd58-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bbd58-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bbd58-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bbd58-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bbd58-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="bbd58-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bbd58-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="bbd58-1617">Erweiterte Verwaltung von Überwachungsrichtlinien auf einem Server oder in einer Datenbank aktiviert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="bbd58-1618">Neuer Parameter (PredicateExpression) hinzugefügt, um die Filterung von Überwachungsprotokollen zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="bbd58-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="bbd58-1619">Cmdlets wurden angepasst, sodass sie SQL-Clients anstelle von Legacyclients verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="bbd58-1620">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="bbd58-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bbd58-1621">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="bbd58-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="bbd58-1622">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="bbd58-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="bbd58-1623">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="bbd58-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="bbd58-1624">Problem bei Verwendung von „Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings“ mit festgelegtem Parameter für den Speicherkontonamen behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="bbd58-1625">0.5.0 – November 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="bbd58-1626">Allgemein</span><span class="sxs-lookup"><span data-stu-id="bbd58-1626">General</span></span>
* <span data-ttu-id="bbd58-1627">Ressourcenvervollständigungen für viele Kern-Cmdlets hinzugefügt (diese ermöglichen das Durchlaufen von vorhandenen Ressourcennamen per TAB-TASTE, wenn Cmdlets interaktiv aufgerufen werden)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="bbd58-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1628">Az.Profile</span></span>
* <span data-ttu-id="bbd58-1629">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="bbd58-1630">Parameter „TenantId“ im Cmdlet „Connect-AzAccount“ in „Tenant“ umbenannt und Alias für „TenantId“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="bbd58-1631">Beschreibung von „TenantId“ für „Connect-AzAccount“ aktualisiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="bbd58-1632">Fehlermeldung für fehlgeschlagene Anmeldung bei Angabe der Mandantendomäne korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="bbd58-1633">Problem in Bezug auf Kontextnamenskonflikt für Konten ohne Abonnements im Mandanten behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="bbd58-1634">Problem mit DataLake-Endpunkten bei Verwendung von MSI behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="bbd58-1635">Problem behoben, das zur Auslösung von „Disconnect-AzAccount“ führte, wenn keine Verbindung bestand</span><span class="sxs-lookup"><span data-stu-id="bbd58-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-1637">Vorgang „Get-AzCognitiveServicesAccountSkus“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1638">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1639">Cmdlets Add-AzVmssVMDataDisk und Remove-AzVmssVMDataDisk hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="bbd58-1640">„Get-AzVMImage“ zeigt „AutomaticOSUpgradeProperties“ an</span><span class="sxs-lookup"><span data-stu-id="bbd58-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="bbd58-1641">Problem behoben, aufgrund dessen die Optionswerte „SetAzVMChefExtension -BootstrapOptions“ und „-JsonAttribute“ nicht im JSON-Format festgelegt wurden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1643">Aktualisierung des DataLake-Pakets auf 1.1.10</span><span class="sxs-lookup"><span data-stu-id="bbd58-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="bbd58-1644">Standardmäßige Parallelität zu Multithreadvorgängen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="bbd58-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1645">Az.Insights</span></span>
* <span data-ttu-id="bbd58-1646">Problem Nr. 7267 behoben (Bereich für automatische Skalierung)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="bbd58-1647">Probleme beim Erstellen einer neuen Regel für die automatische Skalierung, aufgrund derer die aufgelisteten Parameter nicht richtig festgelegt wurden (Es wurde stets der Standardwert festgelegt.)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="bbd58-1648">Problem Nr. 7513 behoben [Insights] „Set-AzDiagnosticSetting“ erfordert die explizite Angabe von Kategorien während der Erstellung der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="bbd58-1649">Nun erfordert das Cmdlet nicht die explizite Angabe der Kategorien, die während der Erstellung aktiviert werden sollen. Das bedeutet, es funktioniert wie dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1650">Az.Network</span></span>
* <span data-ttu-id="bbd58-1651">„PeeringType“ wurde geändert und ist nun ein erforderlicher Parameter für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="bbd58-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="bbd58-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="bbd58-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="bbd58-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bbd58-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="bbd58-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="bbd58-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbd58-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="bbd58-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bbd58-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="bbd58-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="bbd58-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="bbd58-1659">Cmdlets für Richtlinienwartung hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1660">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1661">Fehlerbehebung für https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="bbd58-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="bbd58-1662">Zulassen der Auflistung von Ressourcen mithilfe des Parameters „-ResourceId“ für „Get-AzResource“</span><span class="sxs-lookup"><span data-stu-id="bbd58-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="bbd58-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="bbd58-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="bbd58-1664">Schreibgeschützte Eigenschaft „MigrationState“ zu „PSServiceBusMigrationConfigurationAttributes“ hinzugefügt, was das Ermitteln des Migrationsstatus ermöglicht</span><span class="sxs-lookup"><span data-stu-id="bbd58-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="bbd58-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="bbd58-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="bbd58-1666">Hinzufügen des Zertifikats zu Linux VMSS korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="bbd58-1667">„Add-AzServiceFabricClusterCertificate“ korrigiert</span><span class="sxs-lookup"><span data-stu-id="bbd58-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="bbd58-1668">Verwenden des richtigen Fingerabdrucks aus dem neuen Zertifikat (Azure/service-fabric-issues#932)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="bbd58-1669">Richtige Anzeige von Ausnahmen (Azure/service-fabric-issues#1054)</span><span class="sxs-lookup"><span data-stu-id="bbd58-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="bbd58-1670">„Update-AzServiceFabricDurability“ korrigiert, um die Clusterkonfiguration zu aktualisieren, bevor der VMSS-Vorgang „CreateOrUpdate“ gestartet wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="bbd58-1671">0.4.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="bbd58-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1672">Az.Profile</span></span>
* <span data-ttu-id="bbd58-1673">Problem mit „Get-AzSubscription“ in Cloud Shell behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="bbd58-1674">Allgemeiner Code aktualisiert, sodass die aktuelle Version von „ClientRuntime“ verwendet wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1675">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1676">Neue Größen zur Whitelist von VM-Größen hinzugefügt, für die bei Verwendung des einfachen Parametersatzes für „New-AzVm“ der beschleunigte Netzwerkbetrieb aktiviert wird</span><span class="sxs-lookup"><span data-stu-id="bbd58-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="bbd58-1677">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="bbd58-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbd58-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="bbd58-1679">Unterstützung für VNET-Regeln hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="bbd58-1680">Get-AzDataLakeStoreVirtualNetworkRule: Dient zum Abrufen oder Auflisten der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="bbd58-1681">Add-AzDataLakeStoreVirtualNetworkRule: Fügt dem angegebenen Data Lake Store-Konto eine Regel für das virtuelle Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bbd58-1682">Set-AzDataLakeStoreVirtualNetworkRule: Ändert die angegebene Regel für das virtuelle Netzwerk in das angegebene Data Lake Store-Konto.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="bbd58-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Dient zum Löschen der Azure Data Lake Store-Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1684">Az.Network</span></span>
* <span data-ttu-id="bbd58-1685">Cmdlet „Test-AzNetworkWatcherConnectivity“ aktualisiert, Protokollwert wird jetzt an Back-End übergeben.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="bbd58-1686">ResourceName-Argumentvervollständigung zu allen Cmdlets hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1687">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1688">Problem behoben, aufgrund dessen „Get-AzRoleDefinition“ eine unverständliche Ausnahme auslöst (wenn das Standardprofil kein Abonnement enthält und kein Bereich festgelegt ist), indem im Szenario eine aussagekräftige Ausnahme hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="bbd58-1689">Außerdem wurde der Standardparametersatz auf „RoleDefinitionNameParameterSet“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="bbd58-1690">0.3.0 – Oktober 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="bbd58-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1691">Azure.Storage</span></span>
* <span data-ttu-id="bbd58-1692">Fehler beim Kopieren von Blobs/Dateien behoben, aufgrund dessen bei einem Metadatenproblem des Ziels keine Metadaten kopiert wurden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="bbd58-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="bbd58-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="bbd58-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="bbd58-1695">Der Abruf der Speicherressourcennutzung eines bestimmten Standorts wird jetzt unterstützt, und das Hinzufügen einer Warnmeldung für den Abruf der globalen Speicherressourcennutzung ist überflüssig.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="bbd58-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bbd58-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="bbd58-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="bbd58-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="bbd58-1698">„Get-AzCognitiveServicesAccountSkus“ wird ohne vorhandenes Konto unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="bbd58-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="bbd58-1699">Az.Compute</span></span>
* <span data-ttu-id="bbd58-1700">Korrektur von „Get-AzVM -ResourceGroupName <rg>“, sodass ggf. mehr als 50 Ergebnisse zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="bbd58-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="bbd58-1701">Der Cmdlet-Hilfe zu „New-AzVmss“ wurde ein Beispiel für „SimpleParameterSet“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="bbd58-1702">Tippfehler in der Azure Disk Encryption-Statusmeldung behoben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="bbd58-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="bbd58-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="bbd58-1704">Die Version des ADF .Net-SDK wurde auf 2.3.0 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="bbd58-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="bbd58-1705">Az.Network</span></span>
* <span data-ttu-id="bbd58-1706">NetworkProfile-Funktionalität wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="bbd58-1707">Neue Cmdlets hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1707">new cmdlets added</span></span>
    - <span data-ttu-id="bbd58-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="bbd58-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="bbd58-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="bbd58-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="bbd58-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="bbd58-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="bbd58-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="bbd58-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="bbd58-1714">Dienstzuordnungslink in Subnetzmodell hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="bbd58-1715">Cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="bbd58-1716">Cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="bbd58-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="bbd58-1717">Az.RedisCache</span></span>
* <span data-ttu-id="bbd58-1718">Künftig sind beliebige Zeichenfolgen als Größenparameter zulässig.</span><span class="sxs-lookup"><span data-stu-id="bbd58-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="bbd58-1719">P5 in Popup „PSArgumentCompleter“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="bbd58-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="bbd58-1720">Az.Resources</span></span>
* <span data-ttu-id="bbd58-1721">Fehlender Parameter „-Mode“ zu „Set-AzPolicyDefinition“ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="bbd58-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="bbd58-1722">Cmdlet-Fehler bei „Get-AzProviderOperation“ für Vorgänge mit Ursprung behoben, der den Benutzer enthält</span><span class="sxs-lookup"><span data-stu-id="bbd58-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="bbd58-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="bbd58-1723">Az.Sql</span></span>
* <span data-ttu-id="bbd58-1724">Problem behoben, aufgrund dessen einige Sicherungs-Cmdlets das aktuelle Azure-Abonnements nicht erkannt haben</span><span class="sxs-lookup"><span data-stu-id="bbd58-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="bbd58-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="bbd58-1725">Az.Websites</span></span>
* <span data-ttu-id="bbd58-1726">Neues Cmdlet „Get-AzWebAppContainerContinuousDeploymentUrl“ zum Abrufen der Webhook-URL von Continuous Deployment für Container</span><span class="sxs-lookup"><span data-stu-id="bbd58-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="bbd58-1727">Neue Cmdlets „New-AzWebAppContainerPSSession“ und „Enter-WebAppContainerPSSession“ zum Initiieren einer PowerShell-Remotesitzung in einer Windows-Container-App</span><span class="sxs-lookup"><span data-stu-id="bbd58-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="bbd58-1728">0.2.0 – September 2018</span><span class="sxs-lookup"><span data-stu-id="bbd58-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="bbd58-1729">Erste Version</span><span class="sxs-lookup"><span data-stu-id="bbd58-1729">Initial Release</span></span>
