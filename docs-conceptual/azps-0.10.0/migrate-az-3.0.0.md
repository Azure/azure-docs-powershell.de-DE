---
title: Migrationsleitfaden für Az 3.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Az-Version 3.0 an Azure PowerShell vorgenommen wurden.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: e88752e0c997efc4f49161e358072803cb63450a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "81445525"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="03ea1-103">Migrationsleitfaden für Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="03ea1-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="03ea1-104">In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 2.0.0 und 3.0.0 von Az vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="03ea1-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="03ea1-105">Migrationsleitfaden für Az 3.0.0</span><span class="sxs-lookup"><span data-stu-id="03ea1-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="03ea1-106">Batch</span><span class="sxs-lookup"><span data-stu-id="03ea1-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="03ea1-107">Inkompatibilität mit früheren Versionen von `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="03ea1-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="03ea1-108">Compute</span><span class="sxs-lookup"><span data-stu-id="03ea1-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="03ea1-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="03ea1-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="03ea1-110">IotHub</span><span class="sxs-lookup"><span data-stu-id="03ea1-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="03ea1-111">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03ea1-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="03ea1-112">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03ea1-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="03ea1-113">Inkompatibilität mit früheren Versionen von `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="03ea1-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="03ea1-114">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="03ea1-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="03ea1-115">SQL</span><span class="sxs-lookup"><span data-stu-id="03ea1-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="03ea1-116">Batch</span><span class="sxs-lookup"><span data-stu-id="03ea1-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="03ea1-117">`Get-AzBatchNodeAgentSku` wurde entfernt und durch `Get-AzBatchSupportedImage` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="03ea1-118">`Get-AzBatchSupportedImage` gibt die gleichen Daten wie `Get-AzBatchNodeAgentSku` zurück, allerdings in einem benutzerfreundlicheren Format.</span><span class="sxs-lookup"><span data-stu-id="03ea1-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="03ea1-119">Neue nicht verifizierte Images werden nun ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="03ea1-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="03ea1-120">Zusätzlich sind weitere Informationen zu `Capabilities` und `BatchSupportEndOfLife` für jedes Image vorhanden.</span><span class="sxs-lookup"><span data-stu-id="03ea1-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-121">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="03ea1-122">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="03ea1-123">Inkompatibilität mit früheren Versionen des Az.Resources-Moduls</span><span class="sxs-lookup"><span data-stu-id="03ea1-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="03ea1-124">Version 2.0.1 des Moduls „Az.Batch“ ist mit früheren Versionen (Version 1.7.0 oder früher) des Moduls „Az.Resources“ inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="03ea1-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="03ea1-125">Das führt dazu, dass Version 1.7.0 des Moduls „Az.Resources“ nicht importiert werden kann, wenn Version 2.0.1 des Moduls „Az.Batch“ importiert wird.</span><span class="sxs-lookup"><span data-stu-id="03ea1-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="03ea1-126">Aktualisieren Sie zum Beheben dieses Problems einfach das Modul „Az.Resources“ auf Version 1.7.1 oder eine höhere Version, oder installieren Sie einfach die aktuelle Version des Moduls „Az“.</span><span class="sxs-lookup"><span data-stu-id="03ea1-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="03ea1-127">Compute</span><span class="sxs-lookup"><span data-stu-id="03ea1-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="03ea1-128">Für `UploadSizeInBytes` wird anstelle von `DiskSizeGB` der Parameter `New-AzDiskConfig` verwendet, wenn „CreateOption“ auf „Upload“ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="03ea1-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-129">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="03ea1-130">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="03ea1-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="03ea1-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="03ea1-132">Das Cmdlet `Get-AzHDInsightJobOutput` wurde aktualisiert, um den detaillierten rollenbasierten Zugriff auf den Speicherschlüssel zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="03ea1-133">Benutzer mit den Rollen HDInsight-Clusteroperator, -mitwirkender oder -besitzer sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="03ea1-134">Benutzer, die nur über die Rolle „Leser“ verfügen, müssen den Parameter `DefaultStorageAccountKey` explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="03ea1-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-135">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="03ea1-136">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="03ea1-137">Cmdlet `Add-AzHDInsightConfigValue` hat den Alias für `Add-AzHDInsightConfigValues` entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-138">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-138">Before</span></span>
<span data-ttu-id="03ea1-139">Es werden veraltete Aliasnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="03ea1-140">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="03ea1-141">Ein neues `Disable-AzHDInsightMonitoring`-Cmdlet wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="03ea1-142">Verwenden Sie dieses Cmdlet, um die Überwachung in einem HDInsight-Cluster zu deaktivieren (ersetzt `Disable-AzHDInsightOperationsManagementSuite` und `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="03ea1-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-143">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="03ea1-144">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="03ea1-145">Ein neues `Enable-AzHDInsightMonitoring`-Cmdlet wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="03ea1-146">Verwenden Sie dieses Cmdlet, um die Überwachung in einem HDInsight-Cluster zu aktivieren (ersetzt `Enable-AzHDInsightOperationsManagementSuite` und `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="03ea1-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-147">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="03ea1-148">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="03ea1-149">Ein neues `Get-AzHDInsightMonitoring`-Cmdlet wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="03ea1-150">Verwenden Sie dieses Cmdlet, um den Status der Installationsüberwachung in einem Azure HDInsight-Cluster abzurufen (ersetzt `Get-AzHDInsightOperationsManagementSuite` und `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="03ea1-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-151">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="03ea1-152">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="03ea1-153">Cmdlet `Get-HDInsightProperty` hat den Alias für `Get-AzHDInsightProperties` entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-154">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-154">Before</span></span>
<span data-ttu-id="03ea1-155">Es werden veraltete Aliasnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="03ea1-156">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="03ea1-157">Die Cmdlets `Grant-AzHDInsightRdpServicesAccess` und `Revoke-AzHDInsightRdpServicesAccess` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="03ea1-158">Diese sind nicht mehr erforderlich, da Cluster mit dem Windows-Betriebssystemtyp nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="03ea1-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="03ea1-159">Erstellen Sie stattdessen einen Cluster mit dem Linux-Betriebssystemtyp.</span><span class="sxs-lookup"><span data-stu-id="03ea1-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="03ea1-160">Der Ausgabetyp von `Remove-AzHDInsightCluster` wurde von `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` in `bool` geändert.</span><span class="sxs-lookup"><span data-stu-id="03ea1-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-161">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="03ea1-162">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="03ea1-163">Das Cmdlet ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="03ea1-164">Es gibt keinen Ersatz dafür.</span><span class="sxs-lookup"><span data-stu-id="03ea1-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="03ea1-165">Der Ausgabetyp von `Set-AzHDInsightGatewayCredential` wurde von `HttpConnectivitySettings` in `AzureHDInsightGatewaySettings` geändert.</span><span class="sxs-lookup"><span data-stu-id="03ea1-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="03ea1-166">IotHub</span><span class="sxs-lookup"><span data-stu-id="03ea1-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="03ea1-167">Dieser Alias wird entfernt. Verwenden Sie stattdessen `New-AzIotHubImportDevice`.</span><span class="sxs-lookup"><span data-stu-id="03ea1-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-168">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="03ea1-169">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="03ea1-170">Dieser Alias wird entfernt. Verwenden Sie stattdessen `New-AzIotHubExportDevice`.</span><span class="sxs-lookup"><span data-stu-id="03ea1-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-171">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="03ea1-172">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="03ea1-173">Der Parameter `EventHubEndPointName` ist veraltet und wird nicht ersetzt, weil IotHub nur einen integrierten Endpunkt (events) enthält, der System- und Gerätenachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="03ea1-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-174">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="03ea1-175">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="03ea1-176">Der Parameter `EventHubEndPointName` ist veraltet und wird nicht ersetzt, weil IotHub nur einen integrierten Endpunkt (events) enthält, der System- und Gerätenachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="03ea1-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-177">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="03ea1-178">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="03ea1-179">Der Parameter `EventHubEndPointName` ist veraltet und wird nicht ersetzt, weil IotHub nur einen integrierten Endpunkt (events) enthält, der System- und Gerätenachrichten verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="03ea1-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-180">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="03ea1-181">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="03ea1-182">Der Parameter `OperationsMonitoringProperties` ist veraltet und wird nicht ersetzt, weil IotHub nicht mehr den integrierten Endpunkt (operationsMonitoringEvents) verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="03ea1-183">RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="03ea1-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="03ea1-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` und `ASRRecoveryPlanGroup.EndGroupActions` werden aus der Ausgabe entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="03ea1-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` und `ASRRecoveryPlanGroup.EndGroupActions` werden aus der Ausgabe entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="03ea1-186">Der Parameter „IncludeDiskId“ wird geändert, um das direkte Schreiben auf einen verwalteten Datenträger in Azure Site Recovery zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-187">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="03ea1-188">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="03ea1-189">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="03ea1-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="03ea1-190">Inkompatibilität mit früheren Versionen des Az.Batch-Moduls</span><span class="sxs-lookup"><span data-stu-id="03ea1-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="03ea1-191">Version 1.7.1 des Moduls „Az.Resources“ ist mit früheren Versionen (Version 1.1.2 oder früher) des Moduls „Az.Batch“ inkompatibel.</span><span class="sxs-lookup"><span data-stu-id="03ea1-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="03ea1-192">Das führt dazu, dass Version 1.1.2 des Moduls „Az.Batch“ nicht importiert werden kann, wenn Version 1.7.1 des Moduls „Az.Resources“ importiert wird.</span><span class="sxs-lookup"><span data-stu-id="03ea1-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="03ea1-193">Aktualisieren Sie zum Beheben dieses Problems das Modul „Az.Batch“ auf Version 2.0.1 oder eine höhere Version, oder installieren Sie einfach die aktuelle Version des Moduls „Az“.</span><span class="sxs-lookup"><span data-stu-id="03ea1-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="03ea1-194">ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="03ea1-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="03ea1-195">`Add-ServiceFabricApplicationCertificate` wurde entfernt, da dieses Szenario von `Add-AzVmssSecret` abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="03ea1-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-196">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="03ea1-197">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="03ea1-198">Sql</span><span class="sxs-lookup"><span data-stu-id="03ea1-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="03ea1-199">Beachten Sie, dass die sichere Verbindung veraltet ist und der Befehl daher entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="03ea1-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="03ea1-200">Verwenden Sie zum Anzeigen der Verbindungszeichenfolgen das Blatt „SQL-Datenbank“ im Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="03ea1-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="03ea1-201">Der Alias `Get-AzSqlDatabaseIndexRecommendations` wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="03ea1-202">Verwenden Sie stattdessen `Get-AzSqlDatabaseIndexRecommendation`.</span><span class="sxs-lookup"><span data-stu-id="03ea1-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="03ea1-203">Der Alias `Get-AzSqlDatabaseRestorePoints` wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="03ea1-204">Verwenden Sie stattdessen `Get-AzSqlDatabaseRestorePoint`.</span><span class="sxs-lookup"><span data-stu-id="03ea1-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="03ea1-205">Das Cmdlet `Get-AzSqlDatabaseAudit` ersetzt dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="03ea1-206">Der Ausgabetyp wird von dem vorhandenen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel“ in den neuen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel“ geändert. Die Eigenschaften `AuditState`, `StorageAccountName` und</span><span class="sxs-lookup"><span data-stu-id="03ea1-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="03ea1-207">`StorageAccountSubscriptionId` werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="03ea1-208">Skripts können Speicherkontoinformationen aus der neuen `StorageAccountResourceId`-Eigenschaft abrufen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-209">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="03ea1-210">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="03ea1-211">Das Cmdlet `Set-AzSqlDatabaseAudit` ersetzt dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="03ea1-212">Der Ausgabetyp wird von dem vorhandenen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel“ in den neuen Typ „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="03ea1-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-213">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-214">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="03ea1-215">Das Cmdlet `Get-AzSqlServerAudit` ersetzt dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="03ea1-216">Der Ausgabetyp wird von dem vorhandenen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel“ in den neuen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel“ geändert.</span><span class="sxs-lookup"><span data-stu-id="03ea1-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="03ea1-217">Die Eigenschaften `AuditState`, `StorageAccountName` und `StorageAccountSubscriptionId` werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="03ea1-218">Skripts, die die Eigenschaften `StorageAccountName` und `StorageAccountSubscriptionId` verwenden, können diese Informationen aus der neuen Eigenschaft `StorageAccountResourceId` abrufen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-219">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="03ea1-220">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="03ea1-221">Das Cmdlet `Set-AzSqlServerAudit` ersetzt dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ea1-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="03ea1-222">Der Ausgabetyp wird von dem vorhandenen Typ „Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel“ in den neuen Typ „bool“ geändert.</span><span class="sxs-lookup"><span data-stu-id="03ea1-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-223">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="03ea1-224">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-225">Das Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` wird durch `Get-AzSqlServerAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-226">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-227">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-228">Das Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` wird durch `Clear-AzSqlServerAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-229">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-230">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-231">Das Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` wird durch `Update-AzSqlServerAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-232">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="03ea1-233">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-234">Das Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` wird durch `Get-AzSqlDatabaseAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-235">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-236">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-237">Das Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` wird durch `Update-AzSqlDatabaseAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-238">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="03ea1-239">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="03ea1-240">Das Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` wird durch `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-241">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-242">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-243">Das Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` wird durch `Update-AzSqlDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-244">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="03ea1-245">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-246">Das Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` wird durch `Get-AzSqlDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-247">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-248">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-249">Das Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` wird durch `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-250">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-251">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-252">Das Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` wird durch `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-253">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="03ea1-254">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-255">Das Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` wird durch `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-256">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-257">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-258">Das Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` wird durch `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-259">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-260">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-261">Das Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` wird durch `Update-AzSqlInstanceVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-262">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="03ea1-263">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-264">Das Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` wird durch `Get-AzSqlInstanceVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-265">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-266">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-267">Das Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` wird durch `Clear-AzSqlInstanceVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-268">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-269">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-270">Das Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` wird durch `Update-AzSqlServerVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-271">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="03ea1-272">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-273">Das Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` wird durch `Get-AzSqlServerVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-274">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-275">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="03ea1-276">Das Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` wird durch `Clear-AzSqlServerVulnerabilityAssessmentSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-277">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-278">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="03ea1-279">Das Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` wird gelöscht und durch kein anderes Cmdlet ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="03ea1-280">Das Cmdlet `Get-AzSqlServerThreatDetectionPolicy` wird durch `Get-AzSqlServerThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-281">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="03ea1-282">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="03ea1-283">Das Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` wird durch `Clear-AzSqlServerThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-284">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-285">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="03ea1-286">Das Cmdlet `Set-AzSqlServerThreatDetectionPolicy` wird durch `Update-AzSqlServerThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-287">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="03ea1-288">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="03ea1-289">Das Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` wird durch `Get-AzSqlDatabaseThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-290">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="03ea1-291">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="03ea1-292">Das Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` wird durch `Update-AzSqlDatabaseThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-293">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="03ea1-294">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="03ea1-295">Das Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` wird durch `Clear-AzSqlDatabaseThreatDetectionSetting` ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="03ea1-296">vor</span><span class="sxs-lookup"><span data-stu-id="03ea1-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="03ea1-297">Nach</span><span class="sxs-lookup"><span data-stu-id="03ea1-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
