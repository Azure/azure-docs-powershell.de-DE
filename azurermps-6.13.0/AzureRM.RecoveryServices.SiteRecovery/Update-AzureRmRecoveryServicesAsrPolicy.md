---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 805e421aedbb06b6f9a821b3f575b8a5035c86d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477754"
---
# <span data-ttu-id="d25f5-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="d25f5-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="d25f5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d25f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d25f5-103">Aktualisiert eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d25f5-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d25f5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d25f5-104">SYNTAX</span></span>

### <span data-ttu-id="d25f5-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="d25f5-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25f5-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25f5-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d25f5-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d25f5-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25f5-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25f5-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d25f5-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25f5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d25f5-111">DESCRIPTION</span></span>
<span data-ttu-id="d25f5-112">Das Cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aktualisiert die angegebene Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="d25f5-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="d25f5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d25f5-113">EXAMPLES</span></span>

### <span data-ttu-id="d25f5-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d25f5-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="d25f5-115">Startet den Update-Replikationsrichtlinien Vorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d25f5-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d25f5-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="d25f5-117">Startet den Update Azure to Azure-Replikationsrichtlinien Vorgang unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d25f5-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d25f5-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="d25f5-119">Startet die Update Azure to Azure-Replikationsrichtlinie unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d25f5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d25f5-120">PARAMETERS</span></span>

### <span data-ttu-id="d25f5-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d25f5-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="d25f5-122">Gibt die Häufigkeit (in Stunden) an, mit der anwendungskonsistente Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d25f5-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="d25f5-123">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="d25f5-123">-Authentication</span></span>
<span data-ttu-id="d25f5-124">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="d25f5-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-125">-AzureToAzure</span></span>
<span data-ttu-id="d25f5-126">Parameter Switch gibt an, dass die Replikationsrichtlinie, die zum Replizieren von Azure Virtual Machines zwischen zwei Azure-Bereichen verwendet wird, aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

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

### <span data-ttu-id="d25f5-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d25f5-127">-AzureToVMware</span></span>
<span data-ttu-id="d25f5-128">Switch-Parameter, der angibt, dass die angegebene-Richtlinie zum Replizieren einer fehlgeschlagenen virtuellen Maschine in Azure zurück zu einer lokalen VMware-Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="d25f5-129">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="d25f5-129">-Compression</span></span>
<span data-ttu-id="d25f5-130">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d25f5-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="d25f5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25f5-131">-DefaultProfile</span></span>
<span data-ttu-id="d25f5-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d25f5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d25f5-133">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d25f5-133">-Encryption</span></span>
<span data-ttu-id="d25f5-134">{{Fill Encryption Description}}</span><span class="sxs-lookup"><span data-stu-id="d25f5-134">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25f5-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-135">-HyperVToAzure</span></span>
<span data-ttu-id="d25f5-136">Switch-Parameter, der angibt, dass die angegebene-Richtlinie verwendet wird, um virtuelle Hyper-V-Computer auf Azure zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="d25f5-136">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="d25f5-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d25f5-137">-InputObject</span></span>
<span data-ttu-id="d25f5-138">Eingabeobjekt für das Cmdlet: gibt das ASR-Replikationsrichtlinien Objekt an, das der zu aktualisierden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="d25f5-138">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="d25f5-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="d25f5-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="d25f5-140">Gibt den multiVm-Synchronisierungsstatus für die Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="d25f5-141">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="d25f5-141">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="d25f5-142">Gibt die zu speichernden Nummern Wiederherstellungspunkte an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-142">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="d25f5-143">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d25f5-143">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d25f5-144">Gibt die Azure-Speicherkonto-ID des Replikations Ziels an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-144">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="d25f5-145">Wird als Zielspeicher Konto für die Replikation verwendet, wenn keine Alternative bereitgestellt wird, während die Replikation mithilfe des New-AzureRmRecoveryServicesASRReplicationProtectedItem-Cmdlets aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-145">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="d25f5-146">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="d25f5-146">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="d25f5-147">Zeit in Stunden, um Wiederherstellungspunkte nach der Erstellung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="d25f5-147">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="d25f5-148">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="d25f5-148">-ReplicaDeletion</span></span>
<span data-ttu-id="d25f5-149">Gibt an, ob der virtuelle replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website zu einem anderen gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d25f5-149">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="d25f5-150">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="d25f5-150">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="d25f5-151">Gibt das Replikations Häufigkeitsintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-151">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="d25f5-152">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d25f5-152">Valid values are:</span></span>

- <span data-ttu-id="d25f5-153">30</span><span class="sxs-lookup"><span data-stu-id="d25f5-153">30</span></span>
- <span data-ttu-id="d25f5-154">300</span><span class="sxs-lookup"><span data-stu-id="d25f5-154">300</span></span>
- <span data-ttu-id="d25f5-155">900</span><span class="sxs-lookup"><span data-stu-id="d25f5-155">900</span></span>

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

### <span data-ttu-id="d25f5-156">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="d25f5-156">-ReplicationMethod</span></span>
<span data-ttu-id="d25f5-157">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-157">Specifies the replication method.</span></span>

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

### <span data-ttu-id="d25f5-158">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="d25f5-158">-ReplicationPort</span></span>
<span data-ttu-id="d25f5-159">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-159">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="d25f5-160">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="d25f5-160">-ReplicationStartTime</span></span>
<span data-ttu-id="d25f5-161">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="d25f5-161">Specifies the replication start time.</span></span>
<span data-ttu-id="d25f5-162">Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d25f5-162">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="d25f5-163">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="d25f5-163">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="d25f5-164">Der RPO-Schwellenwert in Minuten, an dem gewarnt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d25f5-164">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="d25f5-165">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="d25f5-165">-VmmToVmm</span></span>
<span data-ttu-id="d25f5-166">Switch-Parameter, der angibt, dass die angegebene-Richtlinie zum Replizieren von VMM-verwalteten Hyper-v-virtuellen Computern zwischen zwei Hyper-v-Websites verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-166">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="d25f5-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d25f5-167">-VMwareToAzure</span></span>
<span data-ttu-id="d25f5-168">Switch-Parameter, der angibt, dass die angegebene-Richtlinie verwendet wird, um virtuelle VMware-Computer auf Azure zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="d25f5-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="d25f5-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d25f5-169">-Confirm</span></span>
<span data-ttu-id="d25f5-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d25f5-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25f5-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25f5-171">-WhatIf</span></span>
<span data-ttu-id="d25f5-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d25f5-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d25f5-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d25f5-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25f5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25f5-174">CommonParameters</span></span>
<span data-ttu-id="d25f5-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25f5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25f5-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d25f5-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25f5-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d25f5-177">INPUTS</span></span>

### <span data-ttu-id="d25f5-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d25f5-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d25f5-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d25f5-179">OUTPUTS</span></span>

### <span data-ttu-id="d25f5-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="d25f5-180">System.Object</span></span>

## <span data-ttu-id="d25f5-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="d25f5-181">NOTES</span></span>

## <span data-ttu-id="d25f5-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d25f5-182">RELATED LINKS</span></span>
