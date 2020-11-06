---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475962"
---
# <span data-ttu-id="4c369-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c369-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="4c369-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c369-102">SYNOPSIS</span></span>
<span data-ttu-id="4c369-103">Aktiviert die Replikation für ein ASR-geschütztes Element, indem ein geschütztes Replikat Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c369-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c369-104">SYNTAX</span></span>

### <span data-ttu-id="4c369-105">EnterpriseToEnterprise (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c369-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c369-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c369-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c369-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c369-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c369-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="4c369-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c369-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c369-111">DESCRIPTION</span></span>
<span data-ttu-id="4c369-112">Mit dem Cmdlet **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** wird ein neues geschütztes Replikat Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="4c369-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="4c369-113">Verwenden Sie dieses Cmdlet, um die Replikation für ein ASR-geschütztes Element zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4c369-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="4c369-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c369-114">EXAMPLES</span></span>

### <span data-ttu-id="4c369-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c369-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="4c369-116">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="4c369-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4c369-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="4c369-118">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Szenario "vmWare in Azure").</span><span class="sxs-lookup"><span data-stu-id="4c369-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="4c369-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4c369-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="4c369-120">Startet den Replikations geschützten Element Erstellungsvorgang für das angegebene ASR-Schutzelement und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="4c369-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="4c369-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="4c369-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="4c369-122">Startet den Replikations geschützten Element Erstellungsvorgang für den angegebenen VmId und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird (Azure to Azure-Szenario).</span><span class="sxs-lookup"><span data-stu-id="4c369-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="4c369-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c369-123">PARAMETERS</span></span>

### <span data-ttu-id="4c369-124">-Konto</span><span class="sxs-lookup"><span data-stu-id="4c369-124">-Account</span></span>
<span data-ttu-id="4c369-125">Das ausführende Konto, das für die Push-Installation des mobilitätsdiensts verwendet werden soll, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4c369-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="4c369-126">Muss eine aus der Liste der ausführende Konten in der ASR-Fabric sein.</span><span class="sxs-lookup"><span data-stu-id="4c369-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="4c369-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-127">-AzureToAzure</span></span>
<span data-ttu-id="4c369-128">Parameter wechseln, um anzugeben, dass es sich bei dem replizierten Element um eine Azure Virtual Machine handelt, die in einen Azure-Recovery-Bereich repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="4c369-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c369-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="4c369-130">Gibt die Liste der zu replizierenden virtuellen Computer Datenträger sowie das Cache-Speicherkonto und das Wiederherstellungs Speicherkonto an, das zum Replizieren des Datenträgers verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="4c369-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="4c369-131">-AzureVmId</span></span>
<span data-ttu-id="4c369-132">Gibt die zu replizierende Azure VM-ID an.</span><span class="sxs-lookup"><span data-stu-id="4c369-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="4c369-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c369-133">-DefaultProfile</span></span>
<span data-ttu-id="4c369-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c369-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-135">-HyperVToAzure</span></span>
<span data-ttu-id="4c369-136">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen Hyper-V-Computer, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="4c369-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="4c369-137">-IncludeDiskId</span></span>
<span data-ttu-id="4c369-138">Die Liste der Datenträger, die für die Replikation einzubeziehen sind.</span><span class="sxs-lookup"><span data-stu-id="4c369-138">The list of disks to include for replication.</span></span> <span data-ttu-id="4c369-139">Standardmäßig sind alle Datenträger enthalten.</span><span class="sxs-lookup"><span data-stu-id="4c369-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4c369-140">-LogStorageAccountId</span></span>
<span data-ttu-id="4c369-141">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="4c369-142">-Name</span><span class="sxs-lookup"><span data-stu-id="4c369-142">-Name</span></span>
<span data-ttu-id="4c369-143">Gibt einen Namen für das geschützte ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="4c369-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="4c369-144">Der Name muss innerhalb des Tresors eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4c369-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="4c369-145">-OS</span><span class="sxs-lookup"><span data-stu-id="4c369-145">-OS</span></span>
<span data-ttu-id="4c369-146">Gibt die Betriebssystemfamilie an.</span><span class="sxs-lookup"><span data-stu-id="4c369-146">Specifies the operating system family.</span></span>
<span data-ttu-id="4c369-147">Die akzeptablen Werte für diesen Parameter sind: Windows oder Linux.</span><span class="sxs-lookup"><span data-stu-id="4c369-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="4c369-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="4c369-148">-OSDiskName</span></span>
<span data-ttu-id="4c369-149">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4c369-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="4c369-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="4c369-150">-ProcessServer</span></span>
<span data-ttu-id="4c369-151">Der Prozess Server, mit dem dieser Computer repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="4c369-152">Verwenden Sie die Liste der Prozess Server im ASR-Fabric, die dem Konfigurationsserver entspricht, um eine anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4c369-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4c369-153">-ProtectableItem</span></span>
<span data-ttu-id="4c369-154">Gibt das zu schützende ASR-Element Objekt an, für das die Replikation aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4c369-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="4c369-156">Gibt das Container Zuordnungsobjekt für ASR-Schutz an, das der für die Replikation zu verwendenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="4c369-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="4c369-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="4c369-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="4c369-158">Die ID des Verfügbarkeits Verzeichnisses, in dem der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="4c369-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="4c369-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="4c369-160">Die ID des virtuellen Azure-Netzwerks, in dem der Computer im Fall eines Failovers wiederhergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4c369-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="4c369-162">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="4c369-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="4c369-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="4c369-164">Das Subnetz im virtuellen Recovery Azure-Netzwerk, in das der fehlerhafte virtuelle Computer im Fall eines Failovers angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c369-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4c369-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="4c369-166">Gibt das Speicherkonto für die Start Diagnose für die Azure-Wiederherstellungs-VM an.</span><span class="sxs-lookup"><span data-stu-id="4c369-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="4c369-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="4c369-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="4c369-168">Gibt die Ressourcen-ID des Wiederherstellungs-Cloud-Diensts an, auf den ein Failover für diesen virtuellen Computer durch die Ressource durch</span><span class="sxs-lookup"><span data-stu-id="4c369-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="4c369-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4c369-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="4c369-170">Gibt den Arm-Bezeichner der Ressourcengruppe an, in der der virtuelle Computer im Fall eines Failovers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="4c369-171">-RecoveryVmName</span></span>
<span data-ttu-id="4c369-172">Der Name des nach dem Failover erstellten Wiederherstellungs-VM.</span><span class="sxs-lookup"><span data-stu-id="4c369-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="4c369-173">-ReplicationGroupName</span></span>
<span data-ttu-id="4c369-174">Gibt den Namen der Replikationsgruppe an, der zum Erstellen von konsistenten Multi-VM-Wiederherstellungspunkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="4c369-175">Standardmäßig wird jedes geschützte Replikat Element in einer eigenen Gruppe erstellt, und es werden keine konsistenten Wiederherstellungspunkte mit mehreren virtuellen Computern generiert.</span><span class="sxs-lookup"><span data-stu-id="4c369-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="4c369-176">Verwenden Sie diese Option nur, wenn Sie mehrere VM-konsistente Wiederherstellungspunkte auf einer Gruppe von Computern erstellen müssen, indem Sie alle Computer auf die gleiche Replikationsgruppe schützen.</span><span class="sxs-lookup"><span data-stu-id="4c369-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c369-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="4c369-177">-VmmToVmm</span></span>
<span data-ttu-id="4c369-178">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen Hyper-v-Computer, der zwischen VMM-verwalteten Hyper-v-Websites repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="4c369-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4c369-179">-VMwareToAzure</span></span>
<span data-ttu-id="4c369-180">Switch-Parameter um das replizierte Element anzugeben, handelt es sich um einen virtuellen VMware-Computer oder physikalischen Server, der in Azure repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="4c369-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4c369-181">-WaitForCompletion</span></span>
<span data-ttu-id="4c369-182">Gibt an, dass das Cmdlet auf den Abschluss des Vorgangs warten soll, bevor er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="4c369-183">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c369-183">-Confirm</span></span>
<span data-ttu-id="4c369-184">Fordert zur Bestätigung auf, bevor der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="4c369-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c369-185">-WhatIf</span></span>
<span data-ttu-id="4c369-186">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c369-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c369-187">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c369-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c369-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c369-188">CommonParameters</span></span>
<span data-ttu-id="4c369-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c369-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c369-190">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c369-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c369-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c369-191">INPUTS</span></span>

### <span data-ttu-id="4c369-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4c369-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="4c369-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c369-193">OUTPUTS</span></span>

### <span data-ttu-id="4c369-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4c369-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4c369-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c369-195">NOTES</span></span>

## <span data-ttu-id="4c369-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c369-196">RELATED LINKS</span></span>

[<span data-ttu-id="4c369-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c369-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4c369-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c369-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="4c369-199">Satz-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c369-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
