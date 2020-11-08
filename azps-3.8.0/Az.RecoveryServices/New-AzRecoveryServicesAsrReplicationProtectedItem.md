---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 3d9cd1bface4175e60b45d6865815f1a4ea964f4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997390"
---
# <span data-ttu-id="750da-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="750da-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="750da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="750da-102">SYNOPSIS</span></span>
<span data-ttu-id="750da-103">Aktiviert die Replikation für ein ASR-geschütztes Element, indem ein geschütztes Replikat Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="750da-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="750da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="750da-104">SYNTAX</span></span>

### <span data-ttu-id="750da-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="750da-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="750da-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="750da-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="750da-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="750da-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="750da-112">DESCRIPTION</span></span>
<span data-ttu-id="750da-113">Mit dem Cmdlet **New-AzRecoveryServicesAsrReplicationProtectedItem** wird ein neues geschütztes Replikat Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="750da-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="750da-114">Verwenden Sie dieses Cmdlet, um die Replikation für ein ASR-geschütztes Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="750da-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="750da-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="750da-115">EXAMPLES</span></span>

### <span data-ttu-id="750da-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="750da-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="750da-117">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="750da-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="750da-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="750da-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="750da-119">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Szenario "vmWare in Azure").</span><span class="sxs-lookup"><span data-stu-id="750da-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="750da-120">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="750da-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="750da-121">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="750da-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="750da-122">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="750da-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="750da-123">Startet den Replikations geschützten Element Erstellungsvorgang für den angegebenen VmId und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="750da-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="750da-124">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="750da-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="750da-125">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement, einschließlich selektiver Datenträger, und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs (vmWare to Azure-Szenario) mit ausgewählten Datenträgern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="750da-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="750da-126">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="750da-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="750da-127">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="750da-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="750da-128">Startet den Replikations geschützten Element Erstellungsvorgang für den angegebenen VmId und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Azure to Azure-Szenario). Für die Failover-VM-Details, die in Cmdlet für Verschlüsselung übergeben werden, werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="750da-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

## <span data-ttu-id="750da-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="750da-129">PARAMETERS</span></span>

### <span data-ttu-id="750da-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="750da-130">-Account</span></span>
<span data-ttu-id="750da-131">Das ausführende Konto, das für die Push-Installation des mobilitätsdiensts verwendet werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="750da-131">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="750da-132">Muss eine aus der Liste der ausführende Konten in der ASR-Fabric sein.</span><span class="sxs-lookup"><span data-stu-id="750da-132">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="750da-133">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-133">-AzureToAzure</span></span>
<span data-ttu-id="750da-134">Parameter "Switch" gibt an, dass das replizierte Element in Azure to Azure-Szenario erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="750da-134">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="750da-135">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="750da-135">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="750da-136">Gibt die Datenträgerkonfiguration für die Verwendung von VM für Azure to Azure Disaster Recovery-Szenario an.</span><span class="sxs-lookup"><span data-stu-id="750da-136">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="750da-137">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="750da-137">-AzureVmId</span></span>
<span data-ttu-id="750da-138">Gibt die Azure VM-ID für den Disaster Recovery-Schutz im Wiederherstellungsbereich an.</span><span class="sxs-lookup"><span data-stu-id="750da-138">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="750da-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="750da-139">-DefaultProfile</span></span>
<span data-ttu-id="750da-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="750da-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="750da-141">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="750da-141">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="750da-142">Gibt die geheim-URL der Datenträgerverschlüsselung mit der Version (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-142">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="750da-143">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="750da-143">-DiskEncryptionSetId</span></span>
<span data-ttu-id="750da-144">Gibt die Ressourcen-ID des Datenträger Verschlüsselungs Satzes an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-144">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="750da-145">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="750da-145">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="750da-146">Gibt die Datenträgerverschlüsselung Secret Vault-ID (Azure Disk Encryption) an, die nach einem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-146">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="750da-147">-Disktype</span><span class="sxs-lookup"><span data-stu-id="750da-147">-DiskType</span></span>
<span data-ttu-id="750da-148">Gibt den Typ der verwalteten VM-Wiederherstellungsfestplatte an.</span><span class="sxs-lookup"><span data-stu-id="750da-148">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="750da-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-149">-HyperVToAzure</span></span>
<span data-ttu-id="750da-150">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen Hyper-V-Computer, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="750da-150">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="750da-151">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="750da-151">-IncludeDiskId</span></span>
<span data-ttu-id="750da-152">Die Liste der Datenträger, die für die Replikation einzubeziehen sind.</span><span class="sxs-lookup"><span data-stu-id="750da-152">The list of disks to include for replication.</span></span> <span data-ttu-id="750da-153">Standardmäßig sind alle Datenträger enthalten.</span><span class="sxs-lookup"><span data-stu-id="750da-153">By default all disks are included.</span></span>

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

### <span data-ttu-id="750da-154">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="750da-154">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="750da-155">Gibt die Datenträgerkonfiguration für vMWare Disk ID an, die vor dem angegebenen, geschützten Element geschützt werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-155">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="750da-156">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="750da-156">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="750da-157">Gibt die URL des Datenträger Verschlüsselungsschlüssels mit der Version (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-157">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="750da-158">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="750da-158">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="750da-159">Gibt den Schlüssel für die Datenträgerverschlüsselung an – Vault-ID (Azure Disk Encryption), die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-159">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="750da-160">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="750da-160">-LogStorageAccountId</span></span>
<span data-ttu-id="750da-161">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-161">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="750da-162">-Name</span><span class="sxs-lookup"><span data-stu-id="750da-162">-Name</span></span>
<span data-ttu-id="750da-163">Gibt einen Namen für das geschützte ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="750da-163">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="750da-164">Der Name muss innerhalb des Tresors eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="750da-164">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="750da-165">-OS</span><span class="sxs-lookup"><span data-stu-id="750da-165">-OS</span></span>
<span data-ttu-id="750da-166">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="750da-166">Specifies the operating system family.</span></span>
<span data-ttu-id="750da-167">Die akzeptablen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="750da-167">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="750da-168">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="750da-168">-OSDiskName</span></span>
<span data-ttu-id="750da-169">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="750da-169">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="750da-170">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="750da-170">-ProcessServer</span></span>
<span data-ttu-id="750da-171">Der Prozess Server, mit dem dieser Computer repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-171">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="750da-172">Verwenden Sie die Liste der Prozess Server im ASR-Fabric, die dem Konfigurationsserver entspricht, um eine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="750da-172">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="750da-173">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="750da-173">-ProtectableItem</span></span>
<span data-ttu-id="750da-174">Gibt das zu schützende ASR-Element Objekt an, für das die Replikation aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="750da-174">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="750da-175">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="750da-175">-ProtectionContainerMapping</span></span>
<span data-ttu-id="750da-176">Gibt das Container Zuordnungsobjekt für ASR-Schutz an, das der für die Replikation zu verwendenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="750da-176">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="750da-177">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="750da-177">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="750da-178">Die ID des Verfügbarkeits Verzeichnisses, in dem der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-178">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="750da-179">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="750da-179">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="750da-180">Gibt die verfügbarkeitszone des Wiederherstellungs-VM nach einem Failover an.</span><span class="sxs-lookup"><span data-stu-id="750da-180">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="750da-181">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="750da-181">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="750da-182">Die ID des virtuellen Azure-Netzwerks, in dem der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-182">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="750da-183">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="750da-183">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="750da-184">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-184">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="750da-185">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="750da-185">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="750da-186">Das Subnetz im virtuellen Recovery Azure-Netzwerk, in das der fehlerhafte virtuelle Computer im Fall eines Failovers angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="750da-186">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="750da-187">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="750da-187">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="750da-188">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="750da-188">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="750da-189">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="750da-189">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="750da-190">Gibt die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts an, auf den ein Failover für diesen virtuellen Computer durch die Ressource durch</span><span class="sxs-lookup"><span data-stu-id="750da-190">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="750da-191">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="750da-191">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="750da-192">Gibt den Arm-Bezeichner der Ressourcengruppe an, in der der virtuelle Computer im Fall eines Failovers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="750da-192">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="750da-193">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="750da-193">-RecoveryVmName</span></span>
<span data-ttu-id="750da-194">Der Name des nach dem Failover erstellten Wiederherstellungs-VM.</span><span class="sxs-lookup"><span data-stu-id="750da-194">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="750da-195">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="750da-195">-ReplicationGroupName</span></span>
<span data-ttu-id="750da-196">Gibt den Namen der Replikationsgruppe an, der zum Erstellen von konsistenten Multi-VM-Wiederherstellungspunkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="750da-196">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="750da-197">Standardmäßig wird jedes geschützte Replikat Element in einer eigenen Gruppe erstellt, und es werden keine konsistenten Wiederherstellungspunkte mit mehreren virtuellen Computern generiert.</span><span class="sxs-lookup"><span data-stu-id="750da-197">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="750da-198">Verwenden Sie diese Option nur, wenn Sie mehrere VM-konsistente Wiederherstellungspunkte auf einer Gruppe von Computern erstellen müssen, indem Sie alle Computer auf die gleiche Replikationsgruppe schützen.</span><span class="sxs-lookup"><span data-stu-id="750da-198">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="750da-199">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="750da-199">-VmmToVmm</span></span>
<span data-ttu-id="750da-200">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen Hyper-v-Computer, der zwischen VMM-verwalteten Hyper-v-Websites repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="750da-200">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="750da-201">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="750da-201">-VMwareToAzure</span></span>
<span data-ttu-id="750da-202">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen VMware-Computer oder physikalischen Server, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="750da-202">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="750da-203">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="750da-203">-WaitForCompletion</span></span>
<span data-ttu-id="750da-204">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs warten soll, bevor er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="750da-204">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="750da-205">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="750da-205">-Confirm</span></span>
<span data-ttu-id="750da-206">Fordert zur Bestätigung auf, bevor der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="750da-206">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="750da-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="750da-207">-WhatIf</span></span>
<span data-ttu-id="750da-208">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="750da-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="750da-209">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="750da-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="750da-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="750da-210">CommonParameters</span></span>
<span data-ttu-id="750da-211">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="750da-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="750da-212">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="750da-212">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="750da-213">Eingaben</span><span class="sxs-lookup"><span data-stu-id="750da-213">INPUTS</span></span>

### <span data-ttu-id="750da-214">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="750da-214">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="750da-215">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="750da-215">OUTPUTS</span></span>

### <span data-ttu-id="750da-216">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="750da-216">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="750da-217">Notizen</span><span class="sxs-lookup"><span data-stu-id="750da-217">NOTES</span></span>

## <span data-ttu-id="750da-218">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="750da-218">RELATED LINKS</span></span>

[<span data-ttu-id="750da-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="750da-219">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="750da-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="750da-220">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="750da-221">Satz-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="750da-221">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
