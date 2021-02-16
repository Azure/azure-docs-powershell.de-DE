---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158601"
---
# <span data-ttu-id="7ea35-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea35-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7ea35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea35-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea35-103">Erstellt eine Azure-Websitewiederherstellungsreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ea35-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="7ea35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ea35-104">SYNTAX</span></span>

### <span data-ttu-id="7ea35-105">HyperVToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ea35-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea35-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7ea35-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea35-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="7ea35-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ea35-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ea35-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ea35-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7ea35-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea35-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ea35-110">DESCRIPTION</span></span>
<span data-ttu-id="7ea35-111">Das **Cmdlet "New-AzRecoveryServicesAsrPolicy"** erstellt eine Azure-Websitewiederherstellungsreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ea35-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="7ea35-112">Die Replikationsrichtlinie wird verwendet, um Replikationseinstellungen anzugeben, z. B. die Replikationshäufigkeit und die Anzahl der Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="7ea35-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="7ea35-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ea35-113">EXAMPLES</span></span>

### <span data-ttu-id="7ea35-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ea35-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="7ea35-115">Startet den Vorgang zum Erstellen einer Replikationsrichtlinie mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea35-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7ea35-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7ea35-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="7ea35-117">Startet den Vorgang zum Erstellen einer Replikationsrichtlinie mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea35-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="7ea35-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7ea35-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="7ea35-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7ea35-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="7ea35-120">Startet den Vorgang zum Erstellen einer Replikationsrichtlinie mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea35-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7ea35-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ea35-121">PARAMETERS</span></span>

### <span data-ttu-id="7ea35-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="7ea35-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="7ea35-123">Gibt die Häufigkeit (in Stunden) an, mit der in der Anwendung konsistente Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7ea35-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-124">-Authentication</span><span class="sxs-lookup"><span data-stu-id="7ea35-124">-Authentication</span></span>
<span data-ttu-id="7ea35-125">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="7ea35-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7ea35-126">Valid values are:</span></span>

- <span data-ttu-id="7ea35-127">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="7ea35-127">Certificate</span></span>
-  <span data-ttu-id="7ea35-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="7ea35-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ea35-129">-AzureToAzure</span></span>
<span data-ttu-id="7ea35-130">"Parameter wechseln" gibt das Szenario für die Erstellung von Azure-zu-Azure-Richtlinien an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="7ea35-131">-AzureToVMware</span></span>
<span data-ttu-id="7ea35-132">"Switch"-Parameter gibt das Szenario für die Erstellung von Richtlinien "azure zu vMWare" an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="7ea35-133">-Compression</span><span class="sxs-lookup"><span data-stu-id="7ea35-133">-Compression</span></span>
<span data-ttu-id="7ea35-134">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ea35-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea35-135">-DefaultProfile</span></span>
<span data-ttu-id="7ea35-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea35-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ea35-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="7ea35-137">-HyperVToAzure</span></span>
<span data-ttu-id="7ea35-138">Parameter zum Angeben der Richtlinie zum Replizieren virtueller Hyper-V-Computer auf Azure verwenden</span><span class="sxs-lookup"><span data-stu-id="7ea35-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="7ea35-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="7ea35-140">Gibt den Synchronisierungsstatus für mehrereVm für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-141">-Name</span><span class="sxs-lookup"><span data-stu-id="7ea35-141">-Name</span></span>
<span data-ttu-id="7ea35-142">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="7ea35-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="7ea35-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="7ea35-144">Gibt die Anzahl der zu behaltenden Wiederherstellungspunkte an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7ea35-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7ea35-146">Gibt die ID des Azure -Speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ea35-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="7ea35-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="7ea35-148">Bewahren Sie die Wiederherstellungspunkte für einen bestimmten Zeitraum in Stunden auf.</span><span class="sxs-lookup"><span data-stu-id="7ea35-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="7ea35-149">-ReplicaDeletion</span></span>
<span data-ttu-id="7ea35-150">Gibt an, ob der virtuelle Replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website auf eine andere gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ea35-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="7ea35-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="7ea35-152">Gibt das Intervall für die Replikationshäufigkeit in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="7ea35-153">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7ea35-153">Valid values are:</span></span>

- <span data-ttu-id="7ea35-154">30</span><span class="sxs-lookup"><span data-stu-id="7ea35-154">30</span></span>
- <span data-ttu-id="7ea35-155">300</span><span class="sxs-lookup"><span data-stu-id="7ea35-155">300</span></span>
- <span data-ttu-id="7ea35-156">900</span><span class="sxs-lookup"><span data-stu-id="7ea35-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="7ea35-157">-ReplicationMethod</span></span>
<span data-ttu-id="7ea35-158">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-158">Specifies the replication method.</span></span>
<span data-ttu-id="7ea35-159">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7ea35-159">Valid values are:</span></span>

- <span data-ttu-id="7ea35-160">Online</span><span class="sxs-lookup"><span data-stu-id="7ea35-160">Online</span></span>
- <span data-ttu-id="7ea35-161">Offline</span><span class="sxs-lookup"><span data-stu-id="7ea35-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="7ea35-162">-ReplicationPort</span></span>
<span data-ttu-id="7ea35-163">Gibt den port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7ea35-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="7ea35-164">-ReplicationProvider</span></span>
<span data-ttu-id="7ea35-165">Gibt den Replikationsanbieter für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="7ea35-166">-ReplicationStartTime</span></span>
<span data-ttu-id="7ea35-167">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="7ea35-167">Specifies the replication start time.</span></span>
<span data-ttu-id="7ea35-168">Er darf nicht später als 24 Stunden ab Dem Beginn des Auftrags sein.</span><span class="sxs-lookup"><span data-stu-id="7ea35-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="7ea35-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="7ea35-170">Der RPO-Schwellenwert in Minuten, zu der eine Warn vor dem RPO festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="7ea35-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ea35-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="7ea35-171">-VmmToVmm</span></span>
<span data-ttu-id="7ea35-172">Der Parameter zum Angeben der Richtlinie soll verwendet werden, um zwischen Hyper-V-Websites zu replizieren, die von einem VMM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea35-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="7ea35-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="7ea35-173">-VMwareToAzure</span></span>
<span data-ttu-id="7ea35-174">Parameter zum Angeben, dass die erstellte Replikationsrichtlinie verwendet wird, um virtuelle VMware-Computer und/oder physische Server in Azure zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="7ea35-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="7ea35-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ea35-175">-Confirm</span></span>
<span data-ttu-id="7ea35-176">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ea35-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea35-177">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7ea35-177">-WhatIf</span></span>
<span data-ttu-id="7ea35-178">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ea35-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ea35-179">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ea35-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea35-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea35-180">CommonParameters</span></span>
<span data-ttu-id="7ea35-181">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea35-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea35-182">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ea35-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea35-183">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ea35-183">INPUTS</span></span>

### <span data-ttu-id="7ea35-184">Keine</span><span class="sxs-lookup"><span data-stu-id="7ea35-184">None</span></span>

## <span data-ttu-id="7ea35-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ea35-185">OUTPUTS</span></span>

### <span data-ttu-id="7ea35-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ea35-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ea35-187">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ea35-187">NOTES</span></span>

## <span data-ttu-id="7ea35-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ea35-188">RELATED LINKS</span></span>

[<span data-ttu-id="7ea35-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea35-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7ea35-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7ea35-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
