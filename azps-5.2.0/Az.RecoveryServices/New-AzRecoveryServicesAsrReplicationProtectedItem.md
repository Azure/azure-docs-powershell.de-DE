---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359566"
---
# <span data-ttu-id="8fd0b-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="8fd0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd0b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd0b-103">Ermöglicht die Replikation für ein asR-geschütztes Element, indem ein replikationsgeschütztes Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="8fd0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fd0b-104">SYNTAX</span></span>

### <span data-ttu-id="8fd0b-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="8fd0b-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd0b-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="8fd0b-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd0b-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd0b-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd0b-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd0b-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-110">AzureToAzure</span></span>
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

### <span data-ttu-id="8fd0b-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="8fd0b-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="8fd0b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fd0b-112">DESCRIPTION</span></span>
<span data-ttu-id="8fd0b-113">Das **Cmdlet "New-AzRecoveryServicesAsrReplicationProtectedItem"** erstellt ein neues replikationsgeschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="8fd0b-114">Verwenden Sie dieses Cmdlet, um die Replikation für ein asr-fähiges Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="8fd0b-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8fd0b-115">EXAMPLES</span></span>

### <span data-ttu-id="8fd0b-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8fd0b-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="8fd0b-117">Startet den Vorgang zum Erstellen eines replikationsgeschützten Elements für das angegebene schützende ASR-Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8fd0b-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8fd0b-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="8fd0b-119">Startet den Vorgang zum Erstellen von replikationsgeschützten Element für das angegebene asR-geschützte Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang (vmWare zu Azure-Szenario) nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="8fd0b-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8fd0b-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="8fd0b-121">Startet den replikationsgeschützten Elementerstellungsvorgang für das angegebene asR-geschützte Element und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="8fd0b-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="8fd0b-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="8fd0b-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="8fd0b-123">Startet den replikationsgeschützten Elementerstellungsvorgang für die angegebene VmId und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="8fd0b-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="8fd0b-124">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="8fd0b-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="8fd0b-125">Startet den Vorgang zum Erstellen eines replikationsgeschützten Elements für das angegebene asR-geschützte Element, einschließlich selektiver Datenträger, und gibt den ASR-Auftrag zurück, mit dem der Vorgang (vmWare zu Azure-Szenario) mit ausgewählten Datenträgern nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="8fd0b-126">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="8fd0b-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="8fd0b-127">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="8fd0b-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="8fd0b-128">Startet den replikationsgeschützten Elementerstellungsvorgang für die angegebene VmId und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird (Azure-zu-Azure-Szenario). Für die Failover-VM-Details, die zum Verschlüsseln im Cmdlet übergeben werden, werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="8fd0b-129">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="8fd0b-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="8fd0b-130">Startet den replikationsgeschützten Elementerstellungsvorgang für einen virtuellen Computer in der Näherungsplatzierungsgruppe und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird (Azure-zu-Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="8fd0b-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="8fd0b-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fd0b-131">PARAMETERS</span></span>

### <span data-ttu-id="8fd0b-132">-Konto</span><span class="sxs-lookup"><span data-stu-id="8fd0b-132">-Account</span></span>
<span data-ttu-id="8fd0b-133">Das Konto "Ausführen als", das verwendet werden soll, um die Installation des Diensts Mobility bei Bedarf zu pushen.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="8fd0b-134">Must be one from the list of run as accounts in the ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="8fd0b-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-135">-AzureToAzure</span></span>
<span data-ttu-id="8fd0b-136">Der Parameter "Switch" gibt an, dass das replizierte Element in Azure zu Azure erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="8fd0b-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8fd0b-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="8fd0b-138">Gibt die Datenträgerkonfiguration an, die für das Notfallwiederherstellungsszenario "Vm für Azure zu Azure" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="8fd0b-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-139">-AzureVmId</span></span>
<span data-ttu-id="8fd0b-140">Gibt die Azure VM-ID für den Notfallwiederherstellungsschutz in der Wiederherstellungsregion an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="8fd0b-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd0b-141">-DefaultProfile</span></span>
<span data-ttu-id="8fd0b-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8fd0b-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8fd0b-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8fd0b-144">Gibt die geheime Festplattenverschlüsselungs-URL mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8fd0b-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8fd0b-146">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="8fd0b-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8fd0b-148">Gibt die geheime Speichertresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8fd0b-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="8fd0b-149">-DiskType</span></span>
<span data-ttu-id="8fd0b-150">Gibt den verwalteten Datenträgertyp der Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="8fd0b-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-151">-HyperVToAzure</span></span>
<span data-ttu-id="8fd0b-152">Parameter wechseln, um anzugeben, dass das replizierte Element ein virtueller Hyper-V-Computer ist, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="8fd0b-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-153">-IncludeDiskId</span></span>
<span data-ttu-id="8fd0b-154">Die Liste der Datenträger, die für die Replikation enthalten sein müssen.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-154">The list of disks to include for replication.</span></span> <span data-ttu-id="8fd0b-155">Standardmäßig sind alle Datenträger enthalten.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="8fd0b-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="8fd0b-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="8fd0b-157">Gibt die Datenträgerkonfigurationseingabe für die vMWare-Datenträger-ID an, um vor bestimmten schützenden Elemente zu schützen.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="8fd0b-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8fd0b-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8fd0b-159">Gibt die URL des Datenträgerverschlüsselungsschlüssels mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8fd0b-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8fd0b-161">Gibt die Schlüssel-Tresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8fd0b-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-162">-LogStorageAccountId</span></span>
<span data-ttu-id="8fd0b-163">Gibt die Protokoll- oder Cachespeicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="8fd0b-164">-Name</span><span class="sxs-lookup"><span data-stu-id="8fd0b-164">-Name</span></span>
<span data-ttu-id="8fd0b-165">Gibt einen Namen für das asr-replikationsgeschützte Element an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="8fd0b-166">Der Name muss innerhalb des Tresors eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="8fd0b-167">-OS</span><span class="sxs-lookup"><span data-stu-id="8fd0b-167">-OS</span></span>
<span data-ttu-id="8fd0b-168">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-168">Specifies the operating system family.</span></span>
<span data-ttu-id="8fd0b-169">Die zulässigen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="8fd0b-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="8fd0b-170">-OSDiskName</span></span>
<span data-ttu-id="8fd0b-171">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="8fd0b-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="8fd0b-172">-ProcessServer</span></span>
<span data-ttu-id="8fd0b-173">Der Prozessserver, der zum Replizieren dieses Computers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="8fd0b-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="8fd0b-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-175">-ProtectableItem</span></span>
<span data-ttu-id="8fd0b-176">Gibt das schützende ASR-Elementobjekt an, für das Replikation aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="8fd0b-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8fd0b-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="8fd0b-178">Gibt das ASR-Schutzcontainerzuordnungsobjekt an, das der für die Replikation zu verwendenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="8fd0b-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="8fd0b-180">Die ID des AvailabilitySet, auf den der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="8fd0b-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="8fd0b-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="8fd0b-182">Gibt die Verfügbarkeitszone der Wiederherstellungs-VM nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="8fd0b-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="8fd0b-184">Die ID des virtuellen Azure-Netzwerks, auf das der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="8fd0b-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8fd0b-186">Gibt die ID des Azure -Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="8fd0b-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="8fd0b-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="8fd0b-188">Das Subnetz innerhalb des wiederherstellungs virtuellen Azure-Netzwerks, an das der Fehler über den virtuellen Computer im Falle eines Failovers angefügt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="8fd0b-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="8fd0b-190">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung der Azure VM an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="8fd0b-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="8fd0b-192">Gibt die Ressourcen-ID des Wiederherstellungs-Clouddiensts an, zu dem dieser virtuelle Computer über einen Failover führen soll.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8fd0b-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="8fd0b-194">Geben Sie die von der Failover-VM im Zielwiederherstellungsbereich zu verwendende Näherungsplatzierungsgruppe-ID an.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="8fd0b-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8fd0b-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8fd0b-196">Gibt den ARM der Ressourcengruppe an, in der der virtuelle Computer im Fall eines Failovers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="8fd0b-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="8fd0b-197">-RecoveryVmName</span></span>
<span data-ttu-id="8fd0b-198">Name der wiederherstellungs-VM, die nach dem Failover erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="8fd0b-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd0b-199">-ReplicationGroupName</span></span>
<span data-ttu-id="8fd0b-200">Gibt den Namen der Replikationsgruppe an, mit dem konsistente Wiederherstellungspunkte für mehrere VIRTUELLE Computer erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="8fd0b-201">Standardmäßig wird jedes replikationsgeschützte Element in einer eigenen Gruppe erstellt, und konsistente Wiederherstellungspunkte für mehrere VM werden nicht generiert.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="8fd0b-202">Verwenden Sie diese Option nur, wenn Sie einheitliche Wiederherstellungspunkte für mehrere virtuelle Computer für eine Gruppe von Computern erstellen müssen, indem Sie alle Computer mit derselben Replikationsgruppe schützen.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="8fd0b-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8fd0b-203">-VmmToVmm</span></span>
<span data-ttu-id="8fd0b-204">Wechseln Sie den Parameter, um anzugeben, dass das replizierte Element ein virtueller Hyper-V-Computer ist, der zwischen VMM-verwalteten Hyper-V-Websites repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="8fd0b-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8fd0b-205">-VMwareToAzure</span></span>
<span data-ttu-id="8fd0b-206">Wechseln Sie den Parameter, um anzugeben, dass es sich bei dem replizierten Element um einen virtuellen VMware-Computer oder physischen Server handelt, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="8fd0b-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8fd0b-207">-WaitForCompletion</span></span>
<span data-ttu-id="8fd0b-208">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs warten soll, bevor es zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="8fd0b-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fd0b-209">-Confirm</span></span>
<span data-ttu-id="8fd0b-210">Fordert vor dem Starten des Vorgangs zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="8fd0b-211">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8fd0b-211">-WhatIf</span></span>
<span data-ttu-id="8fd0b-212">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd0b-213">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd0b-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd0b-214">CommonParameters</span></span>
<span data-ttu-id="8fd0b-215">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd0b-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd0b-216">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fd0b-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd0b-217">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8fd0b-217">INPUTS</span></span>

### <span data-ttu-id="8fd0b-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="8fd0b-219">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8fd0b-219">OUTPUTS</span></span>

### <span data-ttu-id="8fd0b-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="8fd0b-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8fd0b-221">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8fd0b-221">NOTES</span></span>

## <span data-ttu-id="8fd0b-222">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8fd0b-222">RELATED LINKS</span></span>

[<span data-ttu-id="8fd0b-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8fd0b-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="8fd0b-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8fd0b-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
