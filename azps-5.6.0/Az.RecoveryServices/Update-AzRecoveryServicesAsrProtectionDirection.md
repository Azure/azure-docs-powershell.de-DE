---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: c6e25b9b8ec7fe22f76ccec954312914af8dd53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938499"
---
# <span data-ttu-id="cbafb-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="cbafb-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="cbafb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbafb-102">SYNOPSIS</span></span>
<span data-ttu-id="cbafb-103">Aktualisiert die Replikationsrichtung für das angegebene replikationsgeschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="cbafb-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="cbafb-104">Wird verwendet, um ein fehlgeschlagenes über repliziertes Element oder einen Wiederherstellungsplan erneut zu schützen/umgekehrt zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="cbafb-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="cbafb-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbafb-105">SYNTAX</span></span>

### <span data-ttu-id="cbafb-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="cbafb-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbafb-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cbafb-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbafb-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbafb-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbafb-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="cbafb-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbafb-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbafb-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cbafb-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbafb-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="cbafb-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbafb-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="cbafb-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbafb-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cbafb-115">DESCRIPTION</span></span>
<span data-ttu-id="cbafb-116">Das **Cmdlet Update-AzRecoveryServicesAsrProtectionDirectionDirection** aktualisiert die Replikationsrichtung für das angegebene Azure Site Recovery-Objekt nach Abschluss eines Commit-Failovervorgangs.</span><span class="sxs-lookup"><span data-stu-id="cbafb-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="cbafb-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cbafb-117">EXAMPLES</span></span>

### <span data-ttu-id="cbafb-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cbafb-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="cbafb-119">Starten Sie den Updaterichtungsvorgang für den angegebenen Wiederherstellungsplan und gibt das ASR-Auftragsobjekt zurück, das zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cbafb-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="cbafb-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cbafb-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="cbafb-121">Starten Sie den Updaterichtungsvorgang für das angegebene replikationsgeschützte Element in der Azure-Zielregion, das durch die Schutzcontainerzuordnung und die Verwendung von Cachespeicher (in derselben Region wie VM) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cbafb-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="cbafb-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cbafb-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="cbafb-123">Starten Sie den Updaterichtungsvorgang für das angegebene replikationsgeschützte Element in der Azure-Zielregion, das durch die Schutzcontainerzuordnung und die bereitgestellte Datenträgerreplikationskonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cbafb-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="cbafb-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cbafb-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="cbafb-125">Starten Sie den Updaterichtungsvorgang für das angegebene verschlüsselte replikationsgeschützte Element in der Azure-Zielregion, das durch die Schutzcontainerzuordnung und die bereitgestellte Datenträgerreplikationskonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cbafb-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="cbafb-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="cbafb-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="cbafb-127">Starten Sie den Updaterichtungsvorgang für das angegebene replikationsgeschützte Element in der Azure-Zielregion, das durch die Schutzcontainerzuordnung und die Verwendung des Cachespeichers (in derselben Region wie die VM) und der Näherungsplatzierungsgruppe definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cbafb-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="cbafb-128">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cbafb-128">PARAMETERS</span></span>

### <span data-ttu-id="cbafb-129">-Konto</span><span class="sxs-lookup"><span data-stu-id="cbafb-129">-Account</span></span>
<span data-ttu-id="cbafb-130">Das -Konto für die Pushinstallation des Mobilitätsdiensts wird bei Bedarf ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbafb-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="cbafb-131">Muss eins aus der Liste der als Konten in der ASR-Fabric ausgeführten Sein.</span><span class="sxs-lookup"><span data-stu-id="cbafb-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-132">-AzureToAzure</span></span>
<span data-ttu-id="cbafb-133">Gibt die Notfallwiederherstellung von Azure zu Azure an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-133">Specifies the Azure to Azure disaster recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbafb-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="cbafb-135">Gibt die Datenträgerkonfiguration für die Notfallwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-135">Specifies the disk configuration for disaster recovery.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="cbafb-136">-AzureToVMware</span></span>
<span data-ttu-id="cbafb-137">Gibt das Szenario "Azure zu vMWare" an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-137">Specifies the switch azure to vMWare scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="cbafb-138">-DataStore</span></span>
<span data-ttu-id="cbafb-139">Der VMware-Datenspeicher, der für die vmdisk verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-139">The VMware data-store to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbafb-140">-DefaultProfile</span></span>
<span data-ttu-id="cbafb-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cbafb-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cbafb-142">-Richtung</span><span class="sxs-lookup"><span data-stu-id="cbafb-142">-Direction</span></span>
<span data-ttu-id="cbafb-143">Gibt die Richtung an, die für den Aktualisierungsvorgang nach einem Failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="cbafb-144">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="cbafb-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cbafb-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="cbafb-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="cbafb-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="cbafb-146">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="cbafb-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="cbafb-148">Gibt die geheime URL der Datenträgerverschlüsselung mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="cbafb-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="cbafb-150">Gibt die geheime Datenträgerverschlüsselungs-Tresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-151">-HyperVToAzure</span></span>
<span data-ttu-id="cbafb-152">Schützen Sie einen virtuellen Hyper-V-Computer nach dem Failback erneut.</span><span class="sxs-lookup"><span data-stu-id="cbafb-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="cbafb-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="cbafb-154">Gibt die URL des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="cbafb-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="cbafb-156">Gibt den Datenträgerverschlüsselungsschlüssel keyVault ID(Azure Disk Encryption) an, der nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbafb-157">-LogStorageAccountId</span></span>
<span data-ttu-id="cbafb-158">Gibt die Speicherkonto-ID an, um das Replikationsprotokoll von VMs zu speichern.</span><span class="sxs-lookup"><span data-stu-id="cbafb-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="cbafb-159">-MasterTarget</span></span>
<span data-ttu-id="cbafb-160">Masterzielserverdetails.</span><span class="sxs-lookup"><span data-stu-id="cbafb-160">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="cbafb-161">-ProcessServer</span></span>
<span data-ttu-id="cbafb-162">Process Server, der für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-162">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="cbafb-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="cbafb-164">SchutzcontainerMapping, das für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-164">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="cbafb-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="cbafb-166">Der Verfügbarkeitssatz, in dem der virtuelle Computer beim Failover erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="cbafb-166">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbafb-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="cbafb-168">Gibt die ID des Azure-Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbafb-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="cbafb-170">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung von azure VM an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="cbafb-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="cbafb-172">Die Ressourcen-ID des Wiederherstellungs-Clouddiensts, auf den dieser virtuelle Computer failovern soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cbafb-173">-RecoveryPlan</span></span>
<span data-ttu-id="cbafb-174">Gibt ein ASR-Wiederherstellungsplanobjekt an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-174">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="cbafb-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="cbafb-176">Die Ressourcen-ID der Platzierungsgruppe für die Wiederherstellungsnäherung, auf die dieser virtuelle Computer failovern soll.</span><span class="sxs-lookup"><span data-stu-id="cbafb-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cbafb-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="cbafb-178">WiederherstellungsressourceGruppen-ID für geschützte Vm.</span><span class="sxs-lookup"><span data-stu-id="cbafb-178">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbafb-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cbafb-180">Gibt ein geschütztes Element für die ASR-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="cbafb-180">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="cbafb-181">-RetentionVolume</span></span>
<span data-ttu-id="cbafb-182">Aufbewahrungsvolumen auf dem zu verwendende Masterzielserver.</span><span class="sxs-lookup"><span data-stu-id="cbafb-182">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="cbafb-183">-VmmToVmm</span></span>
<span data-ttu-id="cbafb-184">Aktualisieren Sie die Replikationsrichtung für einen Fehler über einen virtuellen Hyper-V-Computer, der zwischen zwei VMM-verwalteten Hyper-V-Websites geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="cbafb-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="cbafb-185">-VMwareToAzure</span></span>
<span data-ttu-id="cbafb-186">Aktualisieren sie die Replikationsrichtung von VMware auf Azure.</span><span class="sxs-lookup"><span data-stu-id="cbafb-186">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafb-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cbafb-187">-Confirm</span></span>
<span data-ttu-id="cbafb-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cbafb-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbafb-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbafb-189">-WhatIf</span></span>
<span data-ttu-id="cbafb-190">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbafb-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbafb-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbafb-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbafb-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbafb-192">CommonParameters</span></span>
<span data-ttu-id="cbafb-193">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbafb-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbafb-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbafb-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbafb-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cbafb-195">INPUTS</span></span>

### <span data-ttu-id="cbafb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cbafb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="cbafb-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbafb-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cbafb-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cbafb-198">OUTPUTS</span></span>

### <span data-ttu-id="cbafb-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cbafb-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cbafb-200">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cbafb-200">NOTES</span></span>

## <span data-ttu-id="cbafb-201">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cbafb-201">RELATED LINKS</span></span>
