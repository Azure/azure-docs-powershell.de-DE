---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 32218fdb966a17cedcb51a2838acae1ae79d9f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003722"
---
# <span data-ttu-id="21a52-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="21a52-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="21a52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21a52-102">SYNOPSIS</span></span>
<span data-ttu-id="21a52-103">Aktualisiert die Replikationsrichtung für das angegebene Replikations geschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="21a52-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="21a52-104">Wird verwendet, um einen fehlerhaften über replizierten Artikel oder Wiederherstellungsplan wieder zu replizieren/zurück zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="21a52-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="21a52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21a52-105">SYNTAX</span></span>

### <span data-ttu-id="21a52-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="21a52-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="21a52-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21a52-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="21a52-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="21a52-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="21a52-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a52-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="21a52-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a52-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21a52-115">DESCRIPTION</span></span>
<span data-ttu-id="21a52-116">Das Cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aktualisiert die Replikationsrichtung für das angegebene Azure Site Recovery-Objekt nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="21a52-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="21a52-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21a52-117">EXAMPLES</span></span>

### <span data-ttu-id="21a52-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21a52-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="21a52-119">Starten Sie den Vorgang Richtung aktualisieren für den angegebenen Wiederherstellungsplan, und geben Sie das ASR-Auftragsobjekt zurück, das zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21a52-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="21a52-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="21a52-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="21a52-121">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Verwendung des Cachespeichers (im gleichen Bereich wie VM) definierte Replikations geschützte Element im Ziel Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="21a52-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="21a52-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="21a52-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="21a52-123">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Bereitstellung der Datenträger Replikation festgelegte, in Ziel Azure Region definierte, geschützte Element</span><span class="sxs-lookup"><span data-stu-id="21a52-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="21a52-124">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="21a52-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="21a52-125">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, verschlüsselte Replikat geschützte Element in einem Azure-Zielbereich, das durch die Schutzcontainer Zuordnung definiert ist, und bereitgestellte Datenträger Replikationskonfiguration</span><span class="sxs-lookup"><span data-stu-id="21a52-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="21a52-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="21a52-126">PARAMETERS</span></span>

### <span data-ttu-id="21a52-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="21a52-127">-Account</span></span>
<span data-ttu-id="21a52-128">Das ausführende Konto, das für die Push-Installation des mobilitätsdiensts verwendet werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="21a52-128">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="21a52-129">Muss eine aus der Liste der ausführende Konten in der ASR-Fabric sein.</span><span class="sxs-lookup"><span data-stu-id="21a52-129">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="21a52-130">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-130">-AzureToAzure</span></span>
<span data-ttu-id="21a52-131">Gibt die Azure to Azure Disaster Recovery an.</span><span class="sxs-lookup"><span data-stu-id="21a52-131">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="21a52-132">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="21a52-132">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="21a52-133">Gibt die Datenträgerkonfiguration für die Disaster Recovery an.</span><span class="sxs-lookup"><span data-stu-id="21a52-133">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="21a52-134">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="21a52-134">-AzureToVMware</span></span>
<span data-ttu-id="21a52-135">Gibt das Umschalten von Azure zu vMWare-Szenario an.</span><span class="sxs-lookup"><span data-stu-id="21a52-135">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="21a52-136">-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="21a52-136">-DataStore</span></span>
<span data-ttu-id="21a52-137">Der VMware-Datenspeicher, der für die vmdisk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21a52-137">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="21a52-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a52-138">-DefaultProfile</span></span>
<span data-ttu-id="21a52-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21a52-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="21a52-140">-Richtung</span><span class="sxs-lookup"><span data-stu-id="21a52-140">-Direction</span></span>
<span data-ttu-id="21a52-141">Gibt die Richtung an, die für den Aktualisierungsvorgang verwendet werden soll, um einen Failover zu senden.</span><span class="sxs-lookup"><span data-stu-id="21a52-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="21a52-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="21a52-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21a52-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="21a52-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="21a52-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="21a52-144">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="21a52-145">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="21a52-145">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="21a52-146">Gibt die geheim-URL der Datenträgerverschlüsselung mit der Version (Azure Disk Encryption) an, die nach dem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-146">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="21a52-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="21a52-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="21a52-148">Gibt die Datenträgerverschlüsselung Secret Vault-ID (Azure Disk Encryption) an, die nach einem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="21a52-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-149">-HyperVToAzure</span></span>
<span data-ttu-id="21a52-150">Schützen Sie einen virtuellen Hyper-V-Computer nach dem Failback.</span><span class="sxs-lookup"><span data-stu-id="21a52-150">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="21a52-151">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="21a52-151">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="21a52-152">Gibt die URL des Datenträger Verschlüsselungsschlüssels (Azure Disk Encryption) an, der nach einem Failover als Wiederherstellungs-VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-152">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="21a52-153">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="21a52-153">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="21a52-154">Gibt den Datenträgerverschlüsselungsschlüssel keyvault-ID (Azure Disk Encryption) an, der als Wiederherstellungs-VM nach einem Failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-154">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="21a52-155">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21a52-155">-LogStorageAccountId</span></span>
<span data-ttu-id="21a52-156">Gibt die Speicherkonto-ID an, auf der das Replikationsprotokoll von VMS gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-156">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="21a52-157">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="21a52-157">-MasterTarget</span></span>
<span data-ttu-id="21a52-158">Master-Ziel Server Details.</span><span class="sxs-lookup"><span data-stu-id="21a52-158">Master Target Server Details.</span></span>

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

### <span data-ttu-id="21a52-159">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="21a52-159">-ProcessServer</span></span>
<span data-ttu-id="21a52-160">Der für die Replikation zu verwendende Prozess Server.</span><span class="sxs-lookup"><span data-stu-id="21a52-160">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="21a52-161">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="21a52-161">-ProtectionContainerMapping</span></span>
<span data-ttu-id="21a52-162">Der für die Replikation zu verwendende Schutz containerMapping.</span><span class="sxs-lookup"><span data-stu-id="21a52-162">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="21a52-163">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="21a52-163">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="21a52-164">Der Verfügbarkeits Satz, in dem der virtuelle Computer beim Failover erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="21a52-164">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="21a52-165">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21a52-165">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="21a52-166">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21a52-166">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="21a52-167">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="21a52-167">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="21a52-168">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="21a52-168">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="21a52-169">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="21a52-169">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="21a52-170">Die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts, auf den dieser virtuelle Computer Failover durch ein Failover durch.</span><span class="sxs-lookup"><span data-stu-id="21a52-170">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="21a52-171">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21a52-171">-RecoveryPlan</span></span>
<span data-ttu-id="21a52-172">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="21a52-172">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="21a52-173">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="21a52-173">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="21a52-174">Wiederherstellungs-Wiederbeschaffungs-ID für geschützte VM.</span><span class="sxs-lookup"><span data-stu-id="21a52-174">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="21a52-175">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21a52-175">-ReplicationProtectedItem</span></span>
<span data-ttu-id="21a52-176">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="21a52-176">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="21a52-177">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="21a52-177">-RetentionVolume</span></span>
<span data-ttu-id="21a52-178">Das Aufbewahrungs Volumen auf dem zu verwendenden Master-Zielserver.</span><span class="sxs-lookup"><span data-stu-id="21a52-178">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="21a52-179">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="21a52-179">-VmmToVmm</span></span>
<span data-ttu-id="21a52-180">Aktualisieren Sie die Replikationsrichtung für einen fehlerhaften Hyper-v-virtuellen Computer, der zwischen zwei VMM-verwalteten Hyper-v-Websites geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="21a52-180">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="21a52-181">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="21a52-181">-VMwareToAzure</span></span>
<span data-ttu-id="21a52-182">Aktualisieren Sie die Replikationsrichtung von VMware auf Azure.</span><span class="sxs-lookup"><span data-stu-id="21a52-182">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="21a52-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21a52-183">-Confirm</span></span>
<span data-ttu-id="21a52-184">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21a52-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a52-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a52-185">-WhatIf</span></span>
<span data-ttu-id="21a52-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21a52-186">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21a52-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21a52-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a52-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a52-188">CommonParameters</span></span>
<span data-ttu-id="21a52-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21a52-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a52-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21a52-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a52-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21a52-191">INPUTS</span></span>

### <span data-ttu-id="21a52-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="21a52-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="21a52-193">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="21a52-193">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="21a52-194">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21a52-194">OUTPUTS</span></span>

### <span data-ttu-id="21a52-195">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="21a52-195">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="21a52-196">Notizen</span><span class="sxs-lookup"><span data-stu-id="21a52-196">NOTES</span></span>

## <span data-ttu-id="21a52-197">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21a52-197">RELATED LINKS</span></span>
