---
title: Migrationsleitfaden für Az 2.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Az-Version 2.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ebe18c24881f146b7cf885892c7869cd7167d511
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410399"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="df8a7-103">Migrationsleitfaden für Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="df8a7-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="df8a7-104">In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 1.0.0 und 2.0.0 von Az vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="df8a7-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="df8a7-105">Inhaltsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="df8a7-105">Table of Contents</span></span>
- [<span data-ttu-id="df8a7-106">Grundlegende Änderungen am Modul</span><span class="sxs-lookup"><span data-stu-id="df8a7-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="df8a7-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="df8a7-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="df8a7-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="df8a7-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="df8a7-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="df8a7-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="df8a7-110">Grundlegende Änderungen am Modul</span><span class="sxs-lookup"><span data-stu-id="df8a7-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="df8a7-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="df8a7-111">Az.Compute</span></span>

- <span data-ttu-id="df8a7-112">Der Parameter `Managed` wurde aus den Cmdlets `New-AzAvailabilitySet` und `Update-AzAvailabilitySet` entfernt, um die Verwendung von ```Sku = Aligned``` zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-113">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-114">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="df8a7-115">Aus Konsistenzgründen wurde der Parameter `Image` aus den Parametersätzen „ByName“ und „ByResourceId“ in `Update-AzImage` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="df8a7-116">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-116">Before</span></span>

  <span data-ttu-id="df8a7-117">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber das übergebene „ImageName“ nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-118">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="df8a7-119">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Restart-AzVM` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="df8a7-120">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-120">Before</span></span>

  <span data-ttu-id="df8a7-121">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-122">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="df8a7-123">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Start-AzVM` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="df8a7-124">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-124">Before</span></span>

  <span data-ttu-id="df8a7-125">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-126">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="df8a7-127">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Stop-AzVM` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="df8a7-128">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-128">Before</span></span>

  <span data-ttu-id="df8a7-129">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-130">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="df8a7-131">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Remove-AzVM` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="df8a7-132">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-132">Before</span></span>

  <span data-ttu-id="df8a7-133">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-134">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="df8a7-135">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Set-AzVM` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="df8a7-136">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-136">Before</span></span>

  <span data-ttu-id="df8a7-137">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-138">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="df8a7-139">Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Save-AzVMImage` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="df8a7-140">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-140">Before</span></span>
  <span data-ttu-id="df8a7-141">Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.</span><span class="sxs-lookup"><span data-stu-id="df8a7-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="df8a7-142">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="df8a7-143">Die ProtectionPolicy-Eigenschaft wurde hinzugefügt, um die Eigenschaft `ProtectFromScaleIn` in `PSVirtualMachineScaleSetVM` zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="df8a7-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-144">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-145">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="df8a7-146">Die ```EncryptionSettingsCollection```-Eigenschaft wurde hinzugefügt, um die `EncryptionSettings` Eigenschaft in `PSDisk` einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-147">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-148">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="df8a7-149">Die ```EncryptionSettingsCollection```-Eigenschaft wurde hinzugefügt, um die `EncryptionSettings` Eigenschaft in `PSSnapshot` einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-150">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-151">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="df8a7-152">Die `VirtualMachineProfile`-Eigenschaft wurde aus `PSVirtualMachineScaleSet` entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-153">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-154">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="df8a7-155">Cmdlet `Set-AzVMBootDiagnostic` entfernt Alias für `Set-AzVMBootDiagnostics`.</span><span class="sxs-lookup"><span data-stu-id="df8a7-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-156">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-156">Before</span></span>

  <span data-ttu-id="df8a7-157">Es werden veraltete Aliasnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="df8a7-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-158">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="df8a7-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` entfernt Alias für `Export-AzLogAnalyticThrottledRequests`.</span><span class="sxs-lookup"><span data-stu-id="df8a7-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-160">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-160">Before</span></span>

  <span data-ttu-id="df8a7-161">Es werden veraltete Aliasnamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="df8a7-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-162">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="df8a7-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="df8a7-163">Az.HDInsight</span></span>

- <span data-ttu-id="df8a7-164">Die Cmdlets `Grant-AzHDInsightHttpServicesAccess` und `Revoke-AzHDInsightHttpServicesAccess` wurden entfernt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="df8a7-165">Diese sind nicht mehr erforderlich, da der HTTP-Zugriff auf alle HDInsight-Cluster immer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="df8a7-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="df8a7-166">Ein neues `Set-AzHDInsightGatewayCredential`-Cmdlet wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="df8a7-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="df8a7-167">Verwenden Sie dieses Cmdlet, um den HTTP-Benutzernamen und das Kennwort für das Gateway zu ändern (ersetzt `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="df8a7-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="df8a7-168">Das Cmdlet `Get-AzHDInsightJobOutput` wurde aktualisiert, um den detaillierten rollenbasierten Zugriff auf den Speicherschlüssel zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="df8a7-169">Benutzer mit den Rollen HDInsight-Clusteroperator, -mitwirkender oder -besitzer sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="df8a7-170">Benutzer, die nur über die Rolle „Leser“ verfügen, müssen den Parameter `DefaultStorageAccountKey` explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="df8a7-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="df8a7-171">Weitere Informationen zu diesen rollenbasierten Zugriffsänderungen finden Sie unter [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update).</span><span class="sxs-lookup"><span data-stu-id="df8a7-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="df8a7-172">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-173">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="df8a7-174">Benutzer, die nur über die Rolle „Leser“ für das Cmdlet „Get-AzHDInsightJobOutput“ verfügen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="df8a7-175">vor</span><span class="sxs-lookup"><span data-stu-id="df8a7-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="df8a7-176">Nach</span><span class="sxs-lookup"><span data-stu-id="df8a7-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="df8a7-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="df8a7-177">Az.Storage</span></span>

- <span data-ttu-id="df8a7-178">Namespaces für Typen, die von den Cmdlets „Blob“, „Warteschlange“ und „Datei“ zurückgegeben werden, haben ihren Namespace von `Microsoft.WindowsAzure.Storage` zu `Microsoft.Azure.Storage` geändert.</span><span class="sxs-lookup"><span data-stu-id="df8a7-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="df8a7-179">Obwohl es sich hierbei technisch gesehen nicht um eine Breaking Change-Änderung gemäß der Breaking Change-Richtlinie handelt, kann es erforderlich sein, einige Änderungen im Code vorzunehmen, die die Methoden des Storage .NET SDKs verwenden, um mit den von diesen Cmdlets zurückgegebenen Objekten zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="df8a7-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="df8a7-180">Beispiel 1:  Hinzufügen einer Nachricht zu einer Warteschlange (CloudQueueMessage-Objektnamespace wird geändert)</span><span class="sxs-lookup"><span data-stu-id="df8a7-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="df8a7-181">Vorher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="df8a7-182">Nachher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="df8a7-183">Beispiel 2:  Abrufen von Blob-/Dateiattributen mit AccessCondition (AccessCondition-Objektnamespace wird geändert)</span><span class="sxs-lookup"><span data-stu-id="df8a7-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="df8a7-184">Vorher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="df8a7-185">Nachher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="df8a7-186">Obwohl es sich hierbei technisch gesehen nicht um eine Breaking Change-Änderung handelt, werden Sie feststellen, dass sich die Ausgabeunterschiede in der Sku.Name-Eigenschaft von Speicherkonten, die von `New/Get/Set-AzStorageAccount`-Änderungen zurückgegeben wurden, wie folgt darstellen.</span><span class="sxs-lookup"><span data-stu-id="df8a7-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="df8a7-187">(Nach der Änderung sind aus- und eingegebenes „SkuName“ ausgerichtet.)</span><span class="sxs-lookup"><span data-stu-id="df8a7-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="df8a7-188">„StandardLRS“ -> „Standard_LRS“;</span><span class="sxs-lookup"><span data-stu-id="df8a7-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="df8a7-189">„StandardGRS“ -> „Standard_GRS“;</span><span class="sxs-lookup"><span data-stu-id="df8a7-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="df8a7-190">„StandardRAGRS“ -> „Standard_RAGRS“;</span><span class="sxs-lookup"><span data-stu-id="df8a7-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="df8a7-191">„StandardZRS“ -> „Standard_ZRS“;</span><span class="sxs-lookup"><span data-stu-id="df8a7-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="df8a7-192">„PremiumLRS“ -> „Premium_LRS“;</span><span class="sxs-lookup"><span data-stu-id="df8a7-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="df8a7-193">Das standardmäßige Dienstverhalten beim Erstellen eines Speicherkontos ohne Angabe einer Art hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="df8a7-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="df8a7-194">In früheren Versionen, als ein Speicherkonto ohne `Kind` angegeben wurde, wurde das Speicherkonto der Art `Storage` verwendet. In der neuen Version `StorageV2` ist der Standardwert `Kind`.</span><span class="sxs-lookup"><span data-stu-id="df8a7-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="df8a7-195">Wenn Sie ein V1-Speicherkonto der Art „Storage“ erstellen müssen, fügen Sie den Parameter „-Kind Storage“ hinzu.</span><span class="sxs-lookup"><span data-stu-id="df8a7-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="df8a7-196">Beispiel: Erstellen eines Speicherkontos (Änderung der Standardart)</span><span class="sxs-lookup"><span data-stu-id="df8a7-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="df8a7-197">Vorher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="df8a7-198">Nachher:</span><span class="sxs-lookup"><span data-stu-id="df8a7-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
