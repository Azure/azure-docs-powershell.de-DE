---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174449"
---
# <span data-ttu-id="c2f78-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="c2f78-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="c2f78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2f78-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f78-103">Aktualisiert die Replikationsrichtung für das angegebene Replikations geschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="c2f78-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="c2f78-104">Wird verwendet, um einen fehlerhaften über replizierten Artikel oder Wiederherstellungsplan wieder zu replizieren/zurück zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="c2f78-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="c2f78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2f78-105">SYNTAX</span></span>

### <span data-ttu-id="c2f78-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2f78-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f78-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c2f78-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2f78-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f78-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f78-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c2f78-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f78-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-111">AzureToAzure</span></span>
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

### <span data-ttu-id="c2f78-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2f78-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="c2f78-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c2f78-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f78-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="c2f78-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2f78-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2f78-115">DESCRIPTION</span></span>
<span data-ttu-id="c2f78-116">Das Cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aktualisiert die Replikationsrichtung für das angegebene Azure Site Recovery-Objekt nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c2f78-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="c2f78-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2f78-117">EXAMPLES</span></span>

### <span data-ttu-id="c2f78-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2f78-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="c2f78-119">Starten Sie den Vorgang Richtung aktualisieren für den angegebenen Wiederherstellungsplan, und geben Sie das ASR-Auftragsobjekt zurück, das zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f78-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="c2f78-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c2f78-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="c2f78-121">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Verwendung des Cachespeichers (im gleichen Bereich wie VM) definierte Replikations geschützte Element im Ziel Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="c2f78-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="c2f78-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c2f78-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="c2f78-123">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Bereitstellung der Datenträger Replikation festgelegte, in Ziel Azure Region definierte, geschützte Element</span><span class="sxs-lookup"><span data-stu-id="c2f78-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="c2f78-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="c2f78-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="c2f78-125">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, verschlüsselte Replikat geschützte Element in einem Azure-Zielbereich, das durch die Schutzcontainer Zuordnung definiert ist, und bereitgestellte Datenträger Replikationskonfiguration</span><span class="sxs-lookup"><span data-stu-id="c2f78-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="c2f78-126">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="c2f78-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="c2f78-127">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Verwendung des Cachespeichers (in der gleichen Region wie VM) und der Näherungs Platzierungs Gruppe definierte, geschützte Replikations Element in einem Ziel Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="c2f78-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="c2f78-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2f78-128">PARAMETERS</span></span>

### <span data-ttu-id="c2f78-129">-Konto</span><span class="sxs-lookup"><span data-stu-id="c2f78-129">-Account</span></span>
<span data-ttu-id="c2f78-130">Das ausführende Konto, das für die Push-Installation des mobilitätsdiensts verwendet werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2f78-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="c2f78-131">Muss eine aus der Liste der ausführende Konten in der ASR-Fabric sein.</span><span class="sxs-lookup"><span data-stu-id="c2f78-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="c2f78-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-132">-AzureToAzure</span></span>
<span data-ttu-id="c2f78-133">Gibt die Azure to Azure Disaster Recovery an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="c2f78-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2f78-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="c2f78-135">Gibt die Datenträgerkonfiguration für die Disaster Recovery an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="c2f78-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="c2f78-136">-AzureToVMware</span></span>
<span data-ttu-id="c2f78-137">Gibt das Umschalten von Azure zu vMWare-Szenario an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="c2f78-138">-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="c2f78-138">-DataStore</span></span>
<span data-ttu-id="c2f78-139">Der VMware-Datenspeicher, der für die vmdisk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f78-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="c2f78-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f78-140">-DefaultProfile</span></span>
<span data-ttu-id="c2f78-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2f78-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c2f78-142">-Richtung</span><span class="sxs-lookup"><span data-stu-id="c2f78-142">-Direction</span></span>
<span data-ttu-id="c2f78-143">Gibt die Richtung an, die für den Aktualisierungsvorgang verwendet werden soll, um einen Failover zu senden.</span><span class="sxs-lookup"><span data-stu-id="c2f78-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="c2f78-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2f78-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2f78-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c2f78-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="c2f78-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c2f78-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c2f78-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="c2f78-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="c2f78-148">Gibt die geheim-URL der Datenträgerverschlüsselung mit der Version (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c2f78-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="c2f78-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="c2f78-150">Gibt die Datenträgerverschlüsselung Secret Vault-ID (Azure Disk Encryption) an, die nach einem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c2f78-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-151">-HyperVToAzure</span></span>
<span data-ttu-id="c2f78-152">Schützen Sie einen virtuellen Hyper-V-Computer nach dem Failback.</span><span class="sxs-lookup"><span data-stu-id="c2f78-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="c2f78-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="c2f78-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="c2f78-154">Gibt die URL des Datenträger Verschlüsselungsschlüssels (Azure Disk Encryption) an, der nach einem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c2f78-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="c2f78-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="c2f78-156">Gibt den Datenträgerverschlüsselungsschlüssel keyvault-ID (Azure Disk Encryption) an, der als Wiederherstellungs-VM nach einem Failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="c2f78-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c2f78-157">-LogStorageAccountId</span></span>
<span data-ttu-id="c2f78-158">Gibt die Speicherkonto-ID an, auf der das Replikationsprotokoll von VMS gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="c2f78-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="c2f78-159">-MasterTarget</span></span>
<span data-ttu-id="c2f78-160">Master-Ziel Server Details.</span><span class="sxs-lookup"><span data-stu-id="c2f78-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="c2f78-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="c2f78-161">-ProcessServer</span></span>
<span data-ttu-id="c2f78-162">Der für die Replikation zu verwendende Prozess Server.</span><span class="sxs-lookup"><span data-stu-id="c2f78-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="c2f78-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c2f78-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="c2f78-164">Der für die Replikation zu verwendende Schutz containerMapping.</span><span class="sxs-lookup"><span data-stu-id="c2f78-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="c2f78-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="c2f78-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="c2f78-166">Der Verfügbarkeits Satz, in dem der virtuelle Computer beim Failover erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="c2f78-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="c2f78-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c2f78-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c2f78-168">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f78-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="c2f78-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c2f78-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="c2f78-170">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="c2f78-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="c2f78-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="c2f78-172">Die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts, auf den dieser virtuelle Computer Failover durch ein Failover durch.</span><span class="sxs-lookup"><span data-stu-id="c2f78-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="c2f78-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2f78-173">-RecoveryPlan</span></span>
<span data-ttu-id="c2f78-174">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="c2f78-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="c2f78-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="c2f78-176">Die Ressourcen-ID der Wiederherstellungs-Näherungs Gruppe, für die ein Failover für diesen virtuellen Computer durchgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f78-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="c2f78-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="c2f78-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="c2f78-178">Wiederherstellungs-Wiederbeschaffungs-ID für geschützte VM.</span><span class="sxs-lookup"><span data-stu-id="c2f78-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="c2f78-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2f78-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c2f78-180">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="c2f78-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="c2f78-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="c2f78-181">-RetentionVolume</span></span>
<span data-ttu-id="c2f78-182">Das Aufbewahrungs Volumen auf dem zu verwendenden Master-Zielserver.</span><span class="sxs-lookup"><span data-stu-id="c2f78-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="c2f78-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="c2f78-183">-VmmToVmm</span></span>
<span data-ttu-id="c2f78-184">Aktualisieren Sie die Replikationsrichtung für einen fehlerhaften Hyper-v-virtuellen Computer, der zwischen zwei VMM-verwalteten Hyper-v-Websites geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="c2f78-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="c2f78-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="c2f78-185">-VMwareToAzure</span></span>
<span data-ttu-id="c2f78-186">Aktualisieren Sie die Replikationsrichtung von VMware auf Azure.</span><span class="sxs-lookup"><span data-stu-id="c2f78-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="c2f78-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2f78-187">-Confirm</span></span>
<span data-ttu-id="c2f78-188">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2f78-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2f78-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f78-189">-WhatIf</span></span>
<span data-ttu-id="c2f78-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f78-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2f78-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2f78-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2f78-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f78-192">CommonParameters</span></span>
<span data-ttu-id="c2f78-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f78-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f78-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2f78-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f78-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2f78-195">INPUTS</span></span>

### <span data-ttu-id="c2f78-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c2f78-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="c2f78-197">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c2f78-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c2f78-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2f78-198">OUTPUTS</span></span>

### <span data-ttu-id="c2f78-199">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c2f78-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2f78-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2f78-200">NOTES</span></span>

## <span data-ttu-id="c2f78-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2f78-201">RELATED LINKS</span></span>
