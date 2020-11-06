---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e6145ee1773a0ecee3ebb1f8c9b5b9e2386cf229
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475970"
---
# <span data-ttu-id="d4a90-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d4a90-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d4a90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a90-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a90-103">Erstellt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d4a90-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a90-104">SYNTAX</span></span>

### <span data-ttu-id="d4a90-105">HyperVToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4a90-105">HyperVToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a90-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d4a90-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4a90-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d4a90-107">AzureToVMware</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4a90-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d4a90-108">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4a90-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d4a90-109">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a90-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a90-110">DESCRIPTION</span></span>
<span data-ttu-id="d4a90-111">Das Cmdlet **New-AzureRmRecoveryServicesAsrPolicy** erstellt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d4a90-111">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="d4a90-112">Die Replikationsrichtlinie wird verwendet, um Replikationseinstellungen wie die Replikationshäufigkeit und die Anzahl der Wiederherstellungspunkte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4a90-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="d4a90-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a90-113">EXAMPLES</span></span>

### <span data-ttu-id="d4a90-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4a90-114">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="d4a90-115">Startet den Replikationsrichtlinien Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4a90-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4a90-116">Example 2</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

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

<span data-ttu-id="d4a90-117">Startet den Replikationsrichtlinien Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d4a90-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d4a90-118">Example 3</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
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

### <span data-ttu-id="d4a90-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d4a90-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzureRmRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="d4a90-120">Startet den Replikationsrichtlinien Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d4a90-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a90-121">PARAMETERS</span></span>

### <span data-ttu-id="d4a90-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d4a90-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="d4a90-123">Gibt die Häufigkeit (in Stunden) an, mit der anwendungskonsistente Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4a90-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="d4a90-124">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d4a90-124">-Authentication</span></span>
<span data-ttu-id="d4a90-125">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="d4a90-126">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d4a90-126">Valid values are:</span></span>

- <span data-ttu-id="d4a90-127">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="d4a90-127">Certificate</span></span>
-  <span data-ttu-id="d4a90-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="d4a90-128">Kerberos</span></span>

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

### <span data-ttu-id="d4a90-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d4a90-129">-AzureToAzure</span></span>
<span data-ttu-id="d4a90-130">Parameter Switch gibt an, dass die erstellte Replikationsrichtlinie zum Replizieren von Azure Virtual Machines zwischen zwei Azure-Regionen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-130">Switch parameter specifying that the replication policy being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="d4a90-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d4a90-131">-AzureToVMware</span></span>
<span data-ttu-id="d4a90-132">Parameter "Switch" gibt an, dass die erstellte Replikationsrichtlinie verwendet wird, um den Replikat Fehler über virtuelle VMware-Maschinen und physische Server, die in Azure ausgeführt werden, zurück zu einer lokalen VMware-Website zu vertauschen.</span><span class="sxs-lookup"><span data-stu-id="d4a90-132">Switch parameter specifying that the replication policy being created will be used to reverse replicate failed over VMware virtual machines and Physical servers running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="d4a90-133">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="d4a90-133">-Compression</span></span>
<span data-ttu-id="d4a90-134">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4a90-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="d4a90-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a90-135">-DefaultProfile</span></span>
<span data-ttu-id="d4a90-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4a90-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d4a90-137">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d4a90-137">-Encryption</span></span>
<span data-ttu-id="d4a90-138">{{Fill Encryption Description}}</span><span class="sxs-lookup"><span data-stu-id="d4a90-138">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a90-139">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d4a90-139">-HyperVToAzure</span></span>
<span data-ttu-id="d4a90-140">Switch-Parameter zum Angeben der Richtlinie wird verwendet, um virtuelle Hyper-V-Computer auf Azure zu replizieren</span><span class="sxs-lookup"><span data-stu-id="d4a90-140">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="d4a90-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="d4a90-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="d4a90-142">Gibt den multiVm-Synchronisierungsstatus für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-142">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="d4a90-143">-Name</span><span class="sxs-lookup"><span data-stu-id="d4a90-143">-Name</span></span>
<span data-ttu-id="d4a90-144">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-144">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="d4a90-145">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="d4a90-145">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="d4a90-146">Gibt die zu speichernden Nummern Wiederherstellungspunkte an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-146">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="d4a90-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4a90-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d4a90-148">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4a90-148">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="d4a90-149">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="d4a90-149">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="d4a90-150">Behalten Sie die Wiederherstellungspunkte für die angegebene Zeit in Stunden bei.</span><span class="sxs-lookup"><span data-stu-id="d4a90-150">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="d4a90-151">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="d4a90-151">-ReplicaDeletion</span></span>
<span data-ttu-id="d4a90-152">Gibt an, ob der virtuelle replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website zu einem anderen gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4a90-152">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="d4a90-153">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="d4a90-153">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="d4a90-154">Gibt das Replikations Häufigkeitsintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-154">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="d4a90-155">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d4a90-155">Valid values are:</span></span>

- <span data-ttu-id="d4a90-156">30</span><span class="sxs-lookup"><span data-stu-id="d4a90-156">30</span></span>
- <span data-ttu-id="d4a90-157">300</span><span class="sxs-lookup"><span data-stu-id="d4a90-157">300</span></span>
- <span data-ttu-id="d4a90-158">900</span><span class="sxs-lookup"><span data-stu-id="d4a90-158">900</span></span>

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

### <span data-ttu-id="d4a90-159">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="d4a90-159">-ReplicationMethod</span></span>
<span data-ttu-id="d4a90-160">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-160">Specifies the replication method.</span></span>
<span data-ttu-id="d4a90-161">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d4a90-161">Valid values are:</span></span>

- <span data-ttu-id="d4a90-162">Online</span><span class="sxs-lookup"><span data-stu-id="d4a90-162">Online</span></span>
- <span data-ttu-id="d4a90-163">Offline</span><span class="sxs-lookup"><span data-stu-id="d4a90-163">Offline</span></span>

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

### <span data-ttu-id="d4a90-164">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="d4a90-164">-ReplicationPort</span></span>
<span data-ttu-id="d4a90-165">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-165">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="d4a90-166">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="d4a90-166">-ReplicationProvider</span></span>
<span data-ttu-id="d4a90-167">Gibt den Replikationsanbieter für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-167">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="d4a90-168">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="d4a90-168">-ReplicationStartTime</span></span>
<span data-ttu-id="d4a90-169">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="d4a90-169">Specifies the replication start time.</span></span>
<span data-ttu-id="d4a90-170">Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d4a90-170">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="d4a90-171">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4a90-171">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="d4a90-172">Der RPO-Schwellenwert in Minuten, an dem gewarnt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4a90-172">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="d4a90-173">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="d4a90-173">-VmmToVmm</span></span>
<span data-ttu-id="d4a90-174">Switch-Parameter zum Angeben der Richtlinie wird verwendet, um zwischen Hyper-V-Websites zu replizieren, die von einem VMM-Server verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="d4a90-174">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="d4a90-175">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d4a90-175">-VMwareToAzure</span></span>
<span data-ttu-id="d4a90-176">Parameter Switch gibt an, dass die erstellte Replikationsrichtlinie verwendet wird, um virtuelle VMware-Maschinen und/oder physikalische Server auf Azure zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="d4a90-176">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="d4a90-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4a90-177">-Confirm</span></span>
<span data-ttu-id="d4a90-178">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4a90-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a90-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a90-179">-WhatIf</span></span>
<span data-ttu-id="d4a90-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a90-180">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4a90-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a90-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a90-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a90-182">CommonParameters</span></span>
<span data-ttu-id="d4a90-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a90-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a90-184">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a90-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a90-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a90-185">INPUTS</span></span>

### <span data-ttu-id="d4a90-186">Keine</span><span class="sxs-lookup"><span data-stu-id="d4a90-186">None</span></span>

## <span data-ttu-id="d4a90-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a90-187">OUTPUTS</span></span>

### <span data-ttu-id="d4a90-188">System. Object</span><span class="sxs-lookup"><span data-stu-id="d4a90-188">System.Object</span></span>

## <span data-ttu-id="d4a90-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a90-189">NOTES</span></span>

## <span data-ttu-id="d4a90-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a90-190">RELATED LINKS</span></span>

[<span data-ttu-id="d4a90-191">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d4a90-191">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="d4a90-192">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d4a90-192">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
