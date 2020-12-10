---
title: Migrationsleitfaden für Az 2.0.0
description: Dieser Migrationsleitfaden enthält eine Liste mit grundlegenden Änderungen, die in Az-Version 2.0 an Azure PowerShell vorgenommen wurden.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d6dac1514fffa140f6d785be9a1a0e8be58476eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856503"
---
# <a name="migration-guide-for-az-200"></a>Migrationsleitfaden für Az 2.0.0

In diesem Dokument werden die Änderungen beschrieben, die zwischen den Versionen 1.0.0 und 2.0.0 von Az vorgenommen wurden. 

## <a name="table-of-contents"></a>Inhaltsverzeichnis
- [Grundlegende Änderungen am Modul](#module-breaking-changes)
  - [Az.Compute](#azcompute)
  - [Az.HDInsight](#azhdinsight)
  - [Az.Storage](#azstorage)

## <a name="module-breaking-changes"></a>Grundlegende Änderungen am Modul

### <a name="azcompute"></a>Az.Compute

- Der Parameter `Managed` wurde aus den Cmdlets `New-AzAvailabilitySet` und `Update-AzAvailabilitySet` entfernt, um die Verwendung von ```Sku = Aligned``` zu unterstützen.

  #### <a name="before"></a>vor

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- Aus Konsistenzgründen wurde der Parameter `Image` aus den Parametersätzen „ByName“ und „ByResourceId“ in `Update-AzImage` entfernt. 
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber das übergebene „ImageName“ nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Restart-AzVM` entfernt.
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Start-AzVM` entfernt.
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Stop-AzVM` entfernt.
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Remove-AzVM` entfernt.
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Set-AzVM` entfernt.
  
  #### <a name="before"></a>vor

  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- Aus Konsistenzgründen wurde der Parameter `Name` aus den Parametersätzen „ByObject“ und „ByResourceId“ in `Save-AzVMImage` entfernt. 
  
  #### <a name="before"></a>vor
  Beachten Sie, dass der nachfolgende Code funktionsfähig ist, aber der übergebene Name nicht verwendet wird, sodass das Entfernen dieses Parameters keine Auswirkung auf die Funktion hat.
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a>Nach
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- Die ProtectionPolicy-Eigenschaft wurde hinzugefügt, um die Eigenschaft `ProtectFromScaleIn` in `PSVirtualMachineScaleSetVM` zu kapseln.

  #### <a name="before"></a>vor

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a>Nach

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- Die ```EncryptionSettingsCollection```-Eigenschaft wurde hinzugefügt, um die `EncryptionSettings` Eigenschaft in `PSDisk` einzuschließen.

  #### <a name="before"></a>vor

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

  #### <a name="after"></a>Nach

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

- Die ```EncryptionSettingsCollection```-Eigenschaft wurde hinzugefügt, um die `EncryptionSettings` Eigenschaft in `PSSnapshot` einzuschließen.

  #### <a name="before"></a>vor

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

  #### <a name="after"></a>Nach

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

- Die `VirtualMachineProfile`-Eigenschaft wurde aus `PSVirtualMachineScaleSet` entfernt.

  #### <a name="before"></a>vor

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a>Nach

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- Cmdlet `Set-AzVMBootDiagnostic` entfernt Alias für `Set-AzVMBootDiagnostics`.

  #### <a name="before"></a>vor

  Es werden veraltete Aliasnamen verwendet.

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- Cmdlet `Export-AzLogAnalyticThrottledRequest` entfernt Alias für `Export-AzLogAnalyticThrottledRequests`.

  #### <a name="before"></a>vor

  Es werden veraltete Aliasnamen verwendet.

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a>Az.HDInsight

- Die Cmdlets `Grant-AzHDInsightHttpServicesAccess` und `Revoke-AzHDInsightHttpServicesAccess` wurden entfernt. Diese sind nicht mehr erforderlich, da der HTTP-Zugriff auf alle HDInsight-Cluster immer aktiviert ist.
- Ein neues `Set-AzHDInsightGatewayCredential`-Cmdlet wurde hinzugefügt. Verwenden Sie dieses Cmdlet, um den HTTP-Benutzernamen und das Kennwort für das Gateway zu ändern (ersetzt `Grant-AzHDInsightHttpServicesAccess`).
- Das Cmdlet `Get-AzHDInsightJobOutput` wurde aktualisiert, um den detaillierten rollenbasierten Zugriff auf den Speicherschlüssel zu unterstützen.
    - Benutzer mit den Rollen HDInsight-Clusteroperator, -mitwirkender oder -besitzer sind davon nicht betroffen.
    - Benutzer, die nur über die Rolle „Leser“ verfügen, müssen den Parameter `DefaultStorageAccountKey` explizit angeben.

Weitere Informationen zu diesen rollenbasierten Zugriffsänderungen finden Sie unter [aka.ms/hdi-config-update](/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations).

  #### <a name="before"></a>vor

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a>Benutzer, die nur über die Rolle „Leser“ für das Cmdlet „Get-AzHDInsightJobOutput“ verfügen.

  ####  <a name="before"></a>vor

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a>Nach

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a>Az.Storage

- Namespaces für Typen, die von den Cmdlets „Blob“, „Warteschlange“ und „Datei“ zurückgegeben werden, haben ihren Namespace von `Microsoft.WindowsAzure.Storage` zu `Microsoft.Azure.Storage` geändert.  Obwohl es sich hierbei technisch gesehen nicht um eine Breaking Change-Änderung gemäß der Breaking Change-Richtlinie handelt, kann es erforderlich sein, einige Änderungen im Code vorzunehmen, die die Methoden des Storage .NET SDKs verwenden, um mit den von diesen Cmdlets zurückgegebenen Objekten zu interagieren.

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a>Beispiel 1:  Hinzufügen einer Nachricht zu einer Warteschlange (CloudQueueMessage-Objektnamespace wird geändert)

  Vorher: 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  Nachher:

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a>Beispiel 2:  Abrufen von Blob-/Dateiattributen mit AccessCondition (AccessCondition-Objektnamespace wird geändert)

  Vorher: 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  Nachher:

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- Obwohl es sich hierbei technisch gesehen nicht um eine Breaking Change-Änderung handelt, werden Sie feststellen, dass sich die Ausgabeunterschiede in der Sku.Name-Eigenschaft von Speicherkonten, die von `New/Get/Set-AzStorageAccount`-Änderungen zurückgegeben wurden, wie folgt darstellen. (Nach der Änderung sind aus- und eingegebenes „SkuName“ ausgerichtet.)
  - „StandardLRS“ -> „Standard_LRS“;
  - „StandardGRS“ -> „Standard_GRS“;
  - „StandardRAGRS“ -> „Standard_RAGRS“;
  - „StandardZRS“ -> „Standard_ZRS“;
  - „PremiumLRS“ -> „Premium_LRS“;

- Das standardmäßige Dienstverhalten beim Erstellen eines Speicherkontos ohne Angabe einer Art hat sich geändert.  In früheren Versionen, als ein Speicherkonto ohne `Kind` angegeben wurde, wurde das Speicherkonto der Art `Storage` verwendet. In der neuen Version `StorageV2` ist der Standardwert `Kind`. Wenn Sie ein V1-Speicherkonto der Art „Storage“ erstellen müssen, fügen Sie den Parameter „-Kind Storage“ hinzu.

  #### <a name="example--create-a-storage-account-default-kind-change"></a>Beispiel: Erstellen eines Speicherkontos (Änderung der Standardart)  

  Vorher:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  Nachher:

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```