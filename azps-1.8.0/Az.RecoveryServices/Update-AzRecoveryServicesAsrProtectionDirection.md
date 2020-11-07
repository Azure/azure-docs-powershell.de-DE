---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659781"
---
# <span data-ttu-id="a20a8-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="a20a8-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="a20a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a20a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a20a8-103">Aktualisiert die Replikationsrichtung für das angegebene Replikations geschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="a20a8-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="a20a8-104">Wird verwendet, um einen fehlerhaften über replizierten Artikel oder Wiederherstellungsplan wieder zu replizieren/zurück zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="a20a8-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="a20a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20a8-105">SYNTAX</span></span>

### <span data-ttu-id="a20a8-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a20a8-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a8-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a20a8-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a20a8-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a8-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a8-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a20a8-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a8-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a20a8-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a20a8-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a20a8-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a20a8-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a20a8-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="a20a8-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20a8-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a20a8-115">DESCRIPTION</span></span>
<span data-ttu-id="a20a8-116">Das Cmdlet **Update-AzRecoveryServicesAsrProtectionDirection** aktualisiert die Replikationsrichtung für das angegebene Azure Site Recovery-Objekt nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a20a8-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="a20a8-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a20a8-117">EXAMPLES</span></span>

### <span data-ttu-id="a20a8-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a20a8-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="a20a8-119">Starten Sie den Vorgang Richtung aktualisieren für den angegebenen Wiederherstellungsplan, und geben Sie das ASR-Auftragsobjekt zurück, das zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a20a8-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="a20a8-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a20a8-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="a20a8-121">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Verwendung des Cachespeichers (im gleichen Bereich wie VM) definierte Replikations geschützte Element im Ziel Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="a20a8-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="a20a8-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a20a8-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="a20a8-123">Starten Sie den Vorgang "Richtung aktualisieren" für das angegebene, durch die Schutzcontainer Zuordnung und die Bereitstellung der Datenträger Replikation festgelegte, in Ziel Azure Region definierte, geschützte Element</span><span class="sxs-lookup"><span data-stu-id="a20a8-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="a20a8-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="a20a8-124">PARAMETERS</span></span>

### <span data-ttu-id="a20a8-125">-Konto</span><span class="sxs-lookup"><span data-stu-id="a20a8-125">-Account</span></span>
<span data-ttu-id="a20a8-126">Das ausführende Konto, das für die Push-Installation des mobilitätsdiensts verwendet werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a20a8-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="a20a8-127">Muss eine aus der Liste der ausführende Konten in der ASR-Fabric sein.</span><span class="sxs-lookup"><span data-stu-id="a20a8-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="a20a8-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-128">-AzureToAzure</span></span>
<span data-ttu-id="a20a8-129">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="a20a8-129">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="a20a8-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a20a8-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="a20a8-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="a20a8-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

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

### <span data-ttu-id="a20a8-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a20a8-132">-AzureToVMware</span></span>
<span data-ttu-id="a20a8-133">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="a20a8-133">{{Fill AzureToVMware Description}}</span></span>

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

### <span data-ttu-id="a20a8-134">-Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="a20a8-134">-DataStore</span></span>
<span data-ttu-id="a20a8-135">Der VMware-Datenspeicher, der für die vmdisk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a20a8-135">The VMware datastore to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="a20a8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20a8-136">-DefaultProfile</span></span>
<span data-ttu-id="a20a8-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a20a8-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a20a8-138">-Richtung</span><span class="sxs-lookup"><span data-stu-id="a20a8-138">-Direction</span></span>
<span data-ttu-id="a20a8-139">Gibt die Richtung an, die für den Aktualisierungsvorgang verwendet werden soll, um einen Failover zu senden.</span><span class="sxs-lookup"><span data-stu-id="a20a8-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="a20a8-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a20a8-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a20a8-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a20a8-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="a20a8-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a20a8-142">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a20a8-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-143">-HyperVToAzure</span></span>
<span data-ttu-id="a20a8-144">Schützen Sie einen virtuellen Hyper-V-Computer nach dem Failback.</span><span class="sxs-lookup"><span data-stu-id="a20a8-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="a20a8-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a20a8-145">-LogStorageAccountId</span></span>
<span data-ttu-id="a20a8-146">Gibt die Speicherkonto-ID an, auf der das Replikationsprotokoll von VMS gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a20a8-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="a20a8-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="a20a8-147">-MasterTarget</span></span>
<span data-ttu-id="a20a8-148">Master-Ziel Server Details.</span><span class="sxs-lookup"><span data-stu-id="a20a8-148">Master Target Server Details.</span></span>

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

### <span data-ttu-id="a20a8-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="a20a8-149">-ProcessServer</span></span>
<span data-ttu-id="a20a8-150">Der für die Replikation zu verwendende Prozess Server.</span><span class="sxs-lookup"><span data-stu-id="a20a8-150">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="a20a8-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a20a8-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="a20a8-152">Der für die Replikation zu verwendende Schutz containerMapping.</span><span class="sxs-lookup"><span data-stu-id="a20a8-152">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="a20a8-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="a20a8-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="a20a8-154">Der Verfügbarkeits Satz, in dem der virtuelle Computer beim Failover erstellt werden soll</span><span class="sxs-lookup"><span data-stu-id="a20a8-154">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="a20a8-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a20a8-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a20a8-156">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a20a8-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="a20a8-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a20a8-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="a20a8-158">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="a20a8-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="a20a8-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="a20a8-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="a20a8-160">Die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts, auf den dieser virtuelle Computer Failover durch ein Failover durch.</span><span class="sxs-lookup"><span data-stu-id="a20a8-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="a20a8-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a20a8-161">-RecoveryPlan</span></span>
<span data-ttu-id="a20a8-162">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a20a8-162">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="a20a8-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a20a8-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a20a8-164">Wiederherstellungs-Wiederbeschaffungs-ID für geschützte VM.</span><span class="sxs-lookup"><span data-stu-id="a20a8-164">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="a20a8-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a20a8-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a20a8-166">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="a20a8-166">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="a20a8-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="a20a8-167">-RetentionVolume</span></span>
<span data-ttu-id="a20a8-168">Das Aufbewahrungs Volumen auf dem zu verwendenden Master-Zielserver.</span><span class="sxs-lookup"><span data-stu-id="a20a8-168">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="a20a8-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a20a8-169">-VmmToVmm</span></span>
<span data-ttu-id="a20a8-170">Aktualisieren Sie die Replikationsrichtung für einen fehlerhaften Hyper-v-virtuellen Computer, der zwischen zwei VMM-verwalteten Hyper-v-Websites geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="a20a8-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="a20a8-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a20a8-171">-VMwareToAzure</span></span>
<span data-ttu-id="a20a8-172">Aktualisieren Sie die Replikationsrichtung von VMware auf Azure.</span><span class="sxs-lookup"><span data-stu-id="a20a8-172">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="a20a8-173">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a20a8-173">-Confirm</span></span>
<span data-ttu-id="a20a8-174">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a20a8-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20a8-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20a8-175">-WhatIf</span></span>
<span data-ttu-id="a20a8-176">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a20a8-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a20a8-177">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a20a8-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20a8-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20a8-178">CommonParameters</span></span>
<span data-ttu-id="a20a8-179">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20a8-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20a8-180">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a20a8-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20a8-181">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a20a8-181">INPUTS</span></span>

### <span data-ttu-id="a20a8-182">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a20a8-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="a20a8-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a20a8-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a20a8-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a20a8-184">OUTPUTS</span></span>

### <span data-ttu-id="a20a8-185">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a20a8-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a20a8-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="a20a8-186">NOTES</span></span>

## <span data-ttu-id="a20a8-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a20a8-187">RELATED LINKS</span></span>
