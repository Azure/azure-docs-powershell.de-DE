---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d2178e4eaf417ff9db0b7c5b83aa22cc7e131f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919320"
---
# <span data-ttu-id="ff40a-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="ff40a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff40a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff40a-103">Ermöglicht die Replikation für ein asr-geschütztes Element, indem ein replikationsgeschütztes Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="ff40a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff40a-104">SYNTAX</span></span>

### <span data-ttu-id="ff40a-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff40a-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff40a-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="ff40a-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff40a-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff40a-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff40a-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff40a-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff40a-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="ff40a-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff40a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ff40a-112">DESCRIPTION</span></span>
<span data-ttu-id="ff40a-113">Das **Cmdlet New-AzRecoveryServicesAsrReplicationProtectedItem** erstellt ein neues replikationsgeschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="ff40a-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="ff40a-114">Verwenden Sie dieses Cmdlet, um die Replikation für ein ASR-schutzfähiges Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ff40a-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="ff40a-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ff40a-115">EXAMPLES</span></span>

### <span data-ttu-id="ff40a-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff40a-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="ff40a-117">Startet den replikationsgeschützten Elementerstellungsvorgang für das angegebene asR-geschützte Element und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="ff40a-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ff40a-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ff40a-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="ff40a-119">Startet den replikationsgeschützten Elementerstellungsvorgang für das angegebene asR-geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird(vmWare in Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="ff40a-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="ff40a-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ff40a-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="ff40a-121">Startet den replikationsgeschützten Elementerstellungsvorgang für das angegebene asR-geschützte Element und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="ff40a-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="ff40a-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ff40a-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="ff40a-123">Startet den replikationsgeschützten Elementerstellungsvorgang für die angegebene VmId und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="ff40a-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="ff40a-124">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ff40a-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="ff40a-125">Startet den replikationsgeschützten Elementerstellungsvorgang für das angegebene ASR-schutzfähige Element, einschließlich selektiver Datenträger, und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs (vmWare in Azure-Szenario) mit ausgewählten Datenträgern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="ff40a-126">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="ff40a-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="ff40a-127">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="ff40a-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="ff40a-128">Startet den replikationsgeschützten Elementerstellungsvorgang für die angegebene VmId und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario). Für die im Cmdlet für die Verschlüsselung übergebenen Failover-VM-Details werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff40a-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="ff40a-129">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="ff40a-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="ff40a-130">Startet den replikationsgeschützten Elementerstellungsvorgang für einen virtuellen Computer in der Platzierungsgruppe Näherung und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="ff40a-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="ff40a-131">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ff40a-131">PARAMETERS</span></span>

### <span data-ttu-id="ff40a-132">-Konto</span><span class="sxs-lookup"><span data-stu-id="ff40a-132">-Account</span></span>
<span data-ttu-id="ff40a-133">Das -Konto für die Pushinstallation des Mobilitätsdiensts wird bei Bedarf ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff40a-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="ff40a-134">Muss eins aus der Liste der als Konten in der ASR-Fabric ausgeführten Sein.</span><span class="sxs-lookup"><span data-stu-id="ff40a-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-135">-AzureToAzure</span></span>
<span data-ttu-id="ff40a-136">Der Parameter Switch gibt an, dass das replizierte Element in Azure in azure szenario erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff40a-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="ff40a-138">Gibt die Datenträgerkonfiguration an, mit der vm für Azure zu Azure notfallwiederherstellungsszenario verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="ff40a-139">-AzureVmId</span></span>
<span data-ttu-id="ff40a-140">Gibt die Azure VM-ID für den Notfallwiederherstellungsschutz in der Wiederherstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff40a-141">-DefaultProfile</span></span>
<span data-ttu-id="ff40a-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ff40a-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="ff40a-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="ff40a-144">Gibt die geheime URL der Datenträgerverschlüsselung mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="ff40a-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="ff40a-146">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssatzs an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ff40a-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="ff40a-148">Gibt die geheime Datenträgerverschlüsselungs-Tresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="ff40a-149">-DiskType</span></span>
<span data-ttu-id="ff40a-150">Gibt den verwalteten Datenträgertyp der Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-151">-HyperVToAzure</span></span>
<span data-ttu-id="ff40a-152">Parameter wechseln, um anzugeben, dass es sich bei dem replizierten Element um einen virtuellen Hyper-V-Computer handelt, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="ff40a-153">-IncludeDiskId</span></span>
<span data-ttu-id="ff40a-154">Die Liste der Datenträger, die für die Replikation enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="ff40a-154">The list of disks to include for replication.</span></span> <span data-ttu-id="ff40a-155">Standardmäßig sind alle Datenträger enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff40a-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="ff40a-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="ff40a-157">Gibt die Datenträgerkonfigurationseingabe für vMWare-Datenträger-ID an, um vor dem angegebenen schützenden Element zu schützen.</span><span class="sxs-lookup"><span data-stu-id="ff40a-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ff40a-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ff40a-159">Gibt die URL des Datenträgerverschlüsselungsschlüssels mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="ff40a-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="ff40a-161">Gibt die Schlüssel-Tresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff40a-162">-LogStorageAccountId</span></span>
<span data-ttu-id="ff40a-163">Gibt die Log- oder Cachespeicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-164">-Name</span><span class="sxs-lookup"><span data-stu-id="ff40a-164">-Name</span></span>
<span data-ttu-id="ff40a-165">Gibt einen Namen für das geschützte Element für die ASR-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="ff40a-166">Der Name muss innerhalb des Tresors eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ff40a-166">The name must be unique within the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-167">-OS</span><span class="sxs-lookup"><span data-stu-id="ff40a-167">-OS</span></span>
<span data-ttu-id="ff40a-168">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-168">Specifies the operating system family.</span></span>
<span data-ttu-id="ff40a-169">Die zulässigen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="ff40a-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="ff40a-170">-OSDiskName</span></span>
<span data-ttu-id="ff40a-171">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="ff40a-172">-ProcessServer</span></span>
<span data-ttu-id="ff40a-173">Der Prozessserver, der zum Replizieren dieses Computers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="ff40a-174">Verwenden Sie die Liste der Prozessserver im ASR-Fabric, die dem Konfigurationsserver entsprechen, um einen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ff40a-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-175">-ProtectableItem</span></span>
<span data-ttu-id="ff40a-176">Gibt das schützende Elementobjekt für ASR an, für das die Replikation aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ff40a-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="ff40a-178">Gibt das ASR-Schutzcontainerzuordnungsobjekt an, das der Replikationsrichtlinie entspricht, die für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="ff40a-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="ff40a-180">Die ID des AvailabilitySets, auf das der Computer im Falle eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="ff40a-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="ff40a-182">Gibt die Verfügbarkeitszone der Wiederherstellungs-VM nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="ff40a-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="ff40a-184">Die ID des virtuellen Azure-Netzwerks, auf das der Computer im Falle eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff40a-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ff40a-186">Gibt die ID des Azure-Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="ff40a-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="ff40a-188">Das Subnetz innerhalb des virtuellen Wiederherstellungsnetzwerks azure, an das der Fehler über den virtuellen Computer im Falle eines Failovers angefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ff40a-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff40a-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="ff40a-190">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung von azure VM an.</span><span class="sxs-lookup"><span data-stu-id="ff40a-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="ff40a-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="ff40a-192">Gibt die Ressourcen-ID des Wiederherstellungs-Clouddiensts an, auf den dieser virtuelle Computer failovern soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ff40a-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="ff40a-194">Geben Sie die näherungsplatzierungsgruppe-ID an, die von der Failover-Vm im Zielwiederherstellungsbereich verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="ff40a-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="ff40a-196">Gibt den ARM der Ressourcengruppe an, in der der virtuelle Computer im Falle eines Failovers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="ff40a-197">-RecoveryVmName</span></span>
<span data-ttu-id="ff40a-198">Name der nach dem Failover erstellten Wiederherstellungs-VM.</span><span class="sxs-lookup"><span data-stu-id="ff40a-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="ff40a-199">-ReplicationGroupName</span></span>
<span data-ttu-id="ff40a-200">Gibt den Namen der Replikationsgruppe an, der zum Erstellen konsistenter Wiederherstellungspunkte mit mehreren VIRTUELLEN Instanzen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="ff40a-201">Standardmäßig wird jedes replikationsgeschützte Element in einer eigenen Gruppe erstellt, und konsistente Wiederherstellungspunkte mit mehreren VIRTUELLEN Instanzen werden nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="ff40a-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="ff40a-202">Verwenden Sie diese Option nur, wenn Sie konsistente Wiederherstellungspunkte mit mehreren VIRTUELLEN Computern für eine Gruppe von Computern erstellen müssen, indem Sie alle Computer in derselben Replikationsgruppe schützen.</span><span class="sxs-lookup"><span data-stu-id="ff40a-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-203">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ff40a-203">-UseManagedDisk</span></span>
<span data-ttu-id="ff40a-204">Gibt an, ob der virtuelle Azure-Computer, der beim Failover erstellt wird, verwaltete Datenträger verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="ff40a-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="ff40a-205">Es akzeptiert entweder "Wahr" oder "Falsch".</span><span class="sxs-lookup"><span data-stu-id="ff40a-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-206">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="ff40a-206">-VmmToVmm</span></span>
<span data-ttu-id="ff40a-207">Parameter wechseln, um anzugeben, dass es sich bei dem replizierten Element um einen virtuellen Hyper-V-Computer handelt, der zwischen VMM-verwalteten Hyper-V-Websites repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-208">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="ff40a-208">-VMwareToAzure</span></span>
<span data-ttu-id="ff40a-209">Parameter wechseln, um anzugeben, dass es sich bei dem replizierten Element um einen virtuellen VMware-Computer oder physischen Server handelt, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-210">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ff40a-210">-WaitForCompletion</span></span>
<span data-ttu-id="ff40a-211">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs warten soll, bevor es zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="ff40a-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-212">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff40a-212">-Confirm</span></span>
<span data-ttu-id="ff40a-213">Fordert sie zur Bestätigung auf, bevor Sie den Vorgang starten.</span><span class="sxs-lookup"><span data-stu-id="ff40a-213">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff40a-214">-WhatIf</span></span>
<span data-ttu-id="ff40a-215">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff40a-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff40a-216">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff40a-216">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff40a-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff40a-217">CommonParameters</span></span>
<span data-ttu-id="ff40a-218">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff40a-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff40a-219">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff40a-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff40a-220">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ff40a-220">INPUTS</span></span>

### <span data-ttu-id="ff40a-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="ff40a-222">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ff40a-222">OUTPUTS</span></span>

### <span data-ttu-id="ff40a-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ff40a-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ff40a-224">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ff40a-224">NOTES</span></span>

## <span data-ttu-id="ff40a-225">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ff40a-225">RELATED LINKS</span></span>

[<span data-ttu-id="ff40a-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ff40a-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="ff40a-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ff40a-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
