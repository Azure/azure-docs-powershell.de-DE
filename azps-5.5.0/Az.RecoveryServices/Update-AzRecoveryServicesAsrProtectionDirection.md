---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151092"
---
# <span data-ttu-id="3f995-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="3f995-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="3f995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f995-102">SYNOPSIS</span></span>
<span data-ttu-id="3f995-103">Aktualisiert die Replikationsrichtung für das angegebene replikationsgeschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="3f995-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="3f995-104">Wird verwendet, um ein fehlgeschlagenes Element oder einen Wiederherstellungsplan erneut zu schützen/umgekehrt zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="3f995-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="3f995-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f995-105">SYNTAX</span></span>

### <span data-ttu-id="3f995-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f995-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f995-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3f995-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f995-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f995-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f995-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="3f995-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f995-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-111">AzureToAzure</span></span>
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

### <span data-ttu-id="3f995-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3f995-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="3f995-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="3f995-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f995-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="3f995-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f995-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f995-115">DESCRIPTION</span></span>
<span data-ttu-id="3f995-116">Das **Cmdlet "Update-AzRecoveryServicesAsrProtectionDirection"** aktualisiert die Replikationsrichtung für das angegebene Azure-Websitewiederherstellungsobjekt nach Abschluss eines Commit-Failovervorgangs.</span><span class="sxs-lookup"><span data-stu-id="3f995-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="3f995-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f995-117">EXAMPLES</span></span>

### <span data-ttu-id="3f995-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f995-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="3f995-119">Starten Sie den Aktualisierungsrichtungsvorgang für den angegebenen Wiederherstellungsplan, und gibt das ASR-Auftragsobjekt zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="3f995-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="3f995-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3f995-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="3f995-121">Starten Sie den Aktualisierungsrichtungsvorgang für das angegebene replikationsgeschützte Element in der Ziel-Azure-Region, die durch die Schutzcontainerzuordnung definiert ist, und verwenden Sie Cachespeicher (in derselben Region wie VM).</span><span class="sxs-lookup"><span data-stu-id="3f995-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="3f995-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3f995-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="3f995-123">Starten Sie den Aktualisierungsrichtungsvorgang für das angegebene replikationsgeschützte Element in der Ziel-Azure-Region, das durch die Schutzcontainerzuordnung und die bereitgestellte Datenträgerreplikationskonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f995-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="3f995-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3f995-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="3f995-125">Starten Sie den Aktualisierungsrichtungsvorgang für das angegebene verschlüsselte replikationsgeschützte Element in der Ziel-Azure-Region, das durch die Schutzcontainerzuordnung und die bereitgestellte Datenträgerreplikationskonfiguration definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f995-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="3f995-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="3f995-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="3f995-127">Starten Sie den Aktualisierungsrichtungsvorgang für das angegebene replikationsgeschützte Element in der durch die Schutzcontainerzuordnung definierten Azure-Zielregion, und verwenden Sie den Cachespeicher (in derselben Region wie VM) und die Näherungsplatzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="3f995-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="3f995-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f995-128">PARAMETERS</span></span>

### <span data-ttu-id="3f995-129">-Konto</span><span class="sxs-lookup"><span data-stu-id="3f995-129">-Account</span></span>
<span data-ttu-id="3f995-130">Das Konto "Ausführen als", das verwendet werden soll, um die Installation des Diensts Mobility bei Bedarf zu pushen.</span><span class="sxs-lookup"><span data-stu-id="3f995-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="3f995-131">Must be one from the list of run as accounts in the ASR fabric.</span><span class="sxs-lookup"><span data-stu-id="3f995-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="3f995-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-132">-AzureToAzure</span></span>
<span data-ttu-id="3f995-133">Gibt die Notfallwiederherstellung von Azure zu Azure an.</span><span class="sxs-lookup"><span data-stu-id="3f995-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="3f995-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f995-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="3f995-135">Gibt die Datenträgerkonfiguration für die Notfallwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="3f995-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="3f995-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="3f995-136">-AzureToVMware</span></span>
<span data-ttu-id="3f995-137">Gibt das Szenario "Azure zu vMWare" an.</span><span class="sxs-lookup"><span data-stu-id="3f995-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="3f995-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="3f995-138">-DataStore</span></span>
<span data-ttu-id="3f995-139">Der VMware-Datenspeicher, der für die virtuellen Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="3f995-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f995-140">-DefaultProfile</span></span>
<span data-ttu-id="3f995-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f995-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3f995-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="3f995-142">-Direction</span></span>
<span data-ttu-id="3f995-143">Gibt die Richtung an, die nach einem Failover für den Aktualisierungsvorgang verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="3f995-144">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="3f995-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f995-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="3f995-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="3f995-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="3f995-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="3f995-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="3f995-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="3f995-148">Gibt die geheime Festplattenverschlüsselungs-URL mit version(Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="3f995-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="3f995-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="3f995-150">Gibt die geheime Speichertresor-ID (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="3f995-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-151">-HyperVToAzure</span></span>
<span data-ttu-id="3f995-152">Schützen Sie einen virtuellen Hyper-V-Computer nach einem Failback erneut.</span><span class="sxs-lookup"><span data-stu-id="3f995-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="3f995-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="3f995-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="3f995-154">Gibt die URL des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="3f995-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="3f995-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="3f995-156">Gibt die Schlüssel-ID des Datenträgerverschlüsselungsschlüssels (Azure-Datenträgerverschlüsselung) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="3f995-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3f995-157">-LogStorageAccountId</span></span>
<span data-ttu-id="3f995-158">Gibt die Speicherkonto-ID zum Speichern des Replikationsprotokolls von VMs an.</span><span class="sxs-lookup"><span data-stu-id="3f995-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="3f995-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="3f995-159">-MasterTarget</span></span>
<span data-ttu-id="3f995-160">Masterzielserverdetails.</span><span class="sxs-lookup"><span data-stu-id="3f995-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="3f995-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="3f995-161">-ProcessServer</span></span>
<span data-ttu-id="3f995-162">Prozessserver, der für die Replikation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="3f995-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="3f995-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="3f995-164">SchutzcontainerMapping für die Replikation.</span><span class="sxs-lookup"><span data-stu-id="3f995-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="3f995-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="3f995-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="3f995-166">Der Verfügbarkeitssatz, in dem der virtuelle Computer beim Failover erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="3f995-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="3f995-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3f995-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="3f995-168">Gibt die ID des Azure -Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f995-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="3f995-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3f995-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="3f995-170">Gibt das Speicherkonto für die Startdiagnose für die Wiederherstellung der Azure VM an.</span><span class="sxs-lookup"><span data-stu-id="3f995-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="3f995-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="3f995-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="3f995-172">Die Ressourcen-ID des Wiederherstellungs-Clouddiensts für den Failover dieses virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="3f995-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="3f995-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f995-173">-RecoveryPlan</span></span>
<span data-ttu-id="3f995-174">Gibt ein ASR-Wiederherstellungsplanobjekt an.</span><span class="sxs-lookup"><span data-stu-id="3f995-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="3f995-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="3f995-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="3f995-176">Die Ressourcen-ID der Näherungsplatzierungsgruppe für die Wiederherstellung zum Failover dieses virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="3f995-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="3f995-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="3f995-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="3f995-178">Recovery resourceGroup-ID für geschützte Vm.</span><span class="sxs-lookup"><span data-stu-id="3f995-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="3f995-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f995-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3f995-180">Gibt ein asR-replikationsgeschütztes Element an.</span><span class="sxs-lookup"><span data-stu-id="3f995-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="3f995-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="3f995-181">-RetentionVolume</span></span>
<span data-ttu-id="3f995-182">Aufbewahrungsvolumen auf dem zu verwendende Masterzielserver.</span><span class="sxs-lookup"><span data-stu-id="3f995-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="3f995-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="3f995-183">-VmmToVmm</span></span>
<span data-ttu-id="3f995-184">Aktualisieren Sie die Replikationsrichtung für einen Fehler auf einem virtuellen Hyper-V-Computer, der zwischen zwei von VMM verwalteten Hyper-V-Websites geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="3f995-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="3f995-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="3f995-185">-VMwareToAzure</span></span>
<span data-ttu-id="3f995-186">Aktualisieren Sie die Replikationsrichtung von VMware zu Azure.</span><span class="sxs-lookup"><span data-stu-id="3f995-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="3f995-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f995-187">-Confirm</span></span>
<span data-ttu-id="3f995-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f995-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f995-189">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3f995-189">-WhatIf</span></span>
<span data-ttu-id="3f995-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f995-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f995-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f995-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f995-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f995-192">CommonParameters</span></span>
<span data-ttu-id="3f995-193">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f995-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f995-194">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f995-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f995-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f995-195">INPUTS</span></span>

### <span data-ttu-id="3f995-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="3f995-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="3f995-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3f995-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3f995-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f995-198">OUTPUTS</span></span>

### <span data-ttu-id="3f995-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3f995-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3f995-200">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f995-200">NOTES</span></span>

## <span data-ttu-id="3f995-201">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f995-201">RELATED LINKS</span></span>
