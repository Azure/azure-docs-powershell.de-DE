---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945767"
---
# <span data-ttu-id="bb132-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bb132-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="bb132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb132-102">SYNOPSIS</span></span>
<span data-ttu-id="bb132-103">Aktualisiert eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bb132-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="bb132-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb132-104">SYNTAX</span></span>

### <span data-ttu-id="bb132-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb132-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb132-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb132-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb132-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="bb132-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb132-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb132-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="bb132-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb132-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb132-111">DESCRIPTION</span></span>
<span data-ttu-id="bb132-112">Das **Cmdlet Update-AzRecoveryServicesAsrPolicy** aktualisiert die angegebene Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bb132-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="bb132-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb132-113">EXAMPLES</span></span>

### <span data-ttu-id="bb132-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb132-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="bb132-115">Startet den Updatereplikationsrichtlinienvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bb132-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bb132-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="bb132-117">Startet den Azure-auf-Azure-Replikationsrichtlinienvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="bb132-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="bb132-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="bb132-119">Startet die Azure-auf-Azure-Replikationsrichtlinie mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bb132-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bb132-120">PARAMETERS</span></span>

### <span data-ttu-id="bb132-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="bb132-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="bb132-122">Gibt die Häufigkeit (in Stunden) an, mit der anwendungsbeständige Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bb132-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="bb132-123">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="bb132-123">-Authentication</span></span>
<span data-ttu-id="bb132-124">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="bb132-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-125">-AzureToAzure</span></span>
<span data-ttu-id="bb132-126">Gibt die Notfallwiederherstellung von Azure zu Azure an.</span><span class="sxs-lookup"><span data-stu-id="bb132-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="bb132-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="bb132-127">-AzureToVMware</span></span>
<span data-ttu-id="bb132-128">Gibt die Azure to vMWare-Notfallwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="bb132-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="bb132-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="bb132-129">-Compression</span></span>
<span data-ttu-id="bb132-130">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb132-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb132-131">-DefaultProfile</span></span>
<span data-ttu-id="bb132-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb132-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bb132-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-133">-HyperVToAzure</span></span>
<span data-ttu-id="bb132-134">Parameter wechseln, der angibt, dass die angegebene Richtlinie zum Replizieren virtueller Hyper-V-Computer in Azure verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="bb132-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb132-135">-InputObject</span></span>
<span data-ttu-id="bb132-136">Eingabeobjekt für das Cmdlet: Gibt das ASR-Replikationsrichtlinienobjekt an, das der zu aktualisierenden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="bb132-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="bb132-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="bb132-138">Gibt den MultiVm-Synchronisierungsstatus für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="bb132-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="bb132-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="bb132-140">Gibt die Anzahl der Wiederherstellungspunkte an, die beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bb132-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bb132-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bb132-142">Gibt die Azure-Speicherkonto-ID des Replikationsziels an.</span><span class="sxs-lookup"><span data-stu-id="bb132-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="bb132-143">Wird als Zielspeicherkonto für die Replikation verwendet, wenn keine Alternative bereitgestellt wird, während die Replikation mithilfe des New-AzRecoveryServicesASRReplicationProtectedItem aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="bb132-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="bb132-145">Zeit in Stunden zum Beibehalten von Wiederherstellungspunkten nach der Erstellung.</span><span class="sxs-lookup"><span data-stu-id="bb132-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="bb132-146">-ReplicaDeletion</span></span>
<span data-ttu-id="bb132-147">Gibt an, ob der virtuelle Replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website auf eine andere gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb132-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="bb132-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="bb132-149">Gibt das Intervall für die Replikationshäufigkeit in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="bb132-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="bb132-150">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bb132-150">Valid values are:</span></span>

- <span data-ttu-id="bb132-151">30</span><span class="sxs-lookup"><span data-stu-id="bb132-151">30</span></span>
- <span data-ttu-id="bb132-152">300</span><span class="sxs-lookup"><span data-stu-id="bb132-152">300</span></span>
- <span data-ttu-id="bb132-153">900</span><span class="sxs-lookup"><span data-stu-id="bb132-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="bb132-154">-ReplicationMethod</span></span>
<span data-ttu-id="bb132-155">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="bb132-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="bb132-156">-ReplicationPort</span></span>
<span data-ttu-id="bb132-157">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="bb132-158">-ReplicationStartTime</span></span>
<span data-ttu-id="bb132-159">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="bb132-159">Specifies the replication start time.</span></span>
<span data-ttu-id="bb132-160">Sie darf nicht später als 24 Stunden nach Dem Beginn des Auftrags sein.</span><span class="sxs-lookup"><span data-stu-id="bb132-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="bb132-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="bb132-162">Der RPO-Schwellenwert in Minuten zum Warnen.</span><span class="sxs-lookup"><span data-stu-id="bb132-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb132-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="bb132-163">-VmmToVmm</span></span>
<span data-ttu-id="bb132-164">Parameter wechseln, der angibt, dass die angegebene Richtlinie verwendet wird, um virtuelle VMM-verwaltete Hyper-V-Computer zwischen zwei Hyper-V-Websites zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="bb132-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="bb132-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bb132-165">-VMwareToAzure</span></span>
<span data-ttu-id="bb132-166">Parameter wechseln, der angibt, dass die angegebene Richtlinie zum Replizieren virtueller VMware-Computer in Azure verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="bb132-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bb132-167">-Confirm</span></span>
<span data-ttu-id="bb132-168">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb132-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb132-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb132-169">-WhatIf</span></span>
<span data-ttu-id="bb132-170">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb132-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb132-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb132-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb132-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb132-172">CommonParameters</span></span>
<span data-ttu-id="bb132-173">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb132-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb132-174">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb132-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb132-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb132-175">INPUTS</span></span>

### <span data-ttu-id="bb132-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="bb132-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="bb132-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb132-177">OUTPUTS</span></span>

### <span data-ttu-id="bb132-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bb132-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bb132-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bb132-179">NOTES</span></span>

## <span data-ttu-id="bb132-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bb132-180">RELATED LINKS</span></span>
