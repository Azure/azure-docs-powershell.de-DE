---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481705"
---
# <span data-ttu-id="7964d-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7964d-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7964d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7964d-102">SYNOPSIS</span></span>
<span data-ttu-id="7964d-103">Erstellt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7964d-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7964d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7964d-104">SYNTAX</span></span>

### <span data-ttu-id="7964d-105">EnterpriseToAzure (Standard)</span><span class="sxs-lookup"><span data-stu-id="7964d-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7964d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7964d-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7964d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7964d-107">DESCRIPTION</span></span>
<span data-ttu-id="7964d-108">Das Cmdlet **New-AzureRmRecoveryServicesAsrPolicy** erstellt eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="7964d-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="7964d-109">Die Replikationsrichtlinie wird verwendet, um Replikationseinstellungen wie die Replikationshäufigkeit und die Anzahl der Wiederherstellungspunkte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7964d-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="7964d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7964d-110">EXAMPLES</span></span>

### <span data-ttu-id="7964d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7964d-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="7964d-112">Startet den Replikationsrichtlinien Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7964d-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7964d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7964d-113">PARAMETERS</span></span>

### <span data-ttu-id="7964d-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="7964d-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="7964d-115">Gibt die Häufigkeit (in Stunden) an, mit der anwendungskonsistente Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7964d-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-116">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="7964d-116">-Authentication</span></span>
<span data-ttu-id="7964d-117">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="7964d-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="7964d-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7964d-118">Valid values are:</span></span>

- <span data-ttu-id="7964d-119">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="7964d-119">Certificate</span></span>
-  <span data-ttu-id="7964d-120">Kerberos</span><span class="sxs-lookup"><span data-stu-id="7964d-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-121">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="7964d-121">-Compression</span></span>
<span data-ttu-id="7964d-122">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7964d-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-123">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="7964d-123">-Encryption</span></span>
<span data-ttu-id="7964d-124">Gibt an, ob die Verschlüsselung aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7964d-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7964d-125">-Name</span></span>
<span data-ttu-id="7964d-126">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="7964d-126">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="7964d-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="7964d-128">Gibt die zu speichernden Nummern Wiederherstellungspunkte an.</span><span class="sxs-lookup"><span data-stu-id="7964d-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7964d-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7964d-130">Gibt die Azure-Speicherkonto-ID des Replikations Ziels an.</span><span class="sxs-lookup"><span data-stu-id="7964d-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="7964d-131">Wird als Zielspeicher Konto für die Replikation verwendet, wenn keine Alternative bereitgestellt wird, während die Replikation mithilfe des New-AzureRmRecoveryServicesASRReplicationProtectedItem-Cmdlets aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7964d-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="7964d-132">-ReplicaDeletion</span></span>
<span data-ttu-id="7964d-133">Gibt an, ob der virtuelle replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website zu einem anderen gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7964d-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="7964d-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="7964d-135">Gibt das Replikations Häufigkeitsintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7964d-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="7964d-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7964d-136">Valid values are:</span></span>

- <span data-ttu-id="7964d-137">30</span><span class="sxs-lookup"><span data-stu-id="7964d-137">30</span></span>
- <span data-ttu-id="7964d-138">300</span><span class="sxs-lookup"><span data-stu-id="7964d-138">300</span></span>
- <span data-ttu-id="7964d-139">900</span><span class="sxs-lookup"><span data-stu-id="7964d-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="7964d-140">-ReplicationMethod</span></span>
<span data-ttu-id="7964d-141">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="7964d-141">Specifies the replication method.</span></span>
<span data-ttu-id="7964d-142">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7964d-142">Valid values are:</span></span>

- <span data-ttu-id="7964d-143">Online</span><span class="sxs-lookup"><span data-stu-id="7964d-143">Online</span></span>
- <span data-ttu-id="7964d-144">Offline</span><span class="sxs-lookup"><span data-stu-id="7964d-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="7964d-145">-ReplicationPort</span></span>
<span data-ttu-id="7964d-146">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7964d-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="7964d-147">-ReplicationProvider</span></span>
<span data-ttu-id="7964d-148">Gibt den Replikationsanbieter an.</span><span class="sxs-lookup"><span data-stu-id="7964d-148">Specifies the replication provider.</span></span>
<span data-ttu-id="7964d-149">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7964d-149">Valid values are:</span></span>

- <span data-ttu-id="7964d-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="7964d-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="7964d-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="7964d-151">HyperVReplica2012</span></span>
- <span data-ttu-id="7964d-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="7964d-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="7964d-153">-ReplicationStartTime</span></span>
<span data-ttu-id="7964d-154">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="7964d-154">Specifies the replication start time.</span></span>
<span data-ttu-id="7964d-155">Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="7964d-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7964d-156">-Confirm</span></span>
<span data-ttu-id="7964d-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7964d-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7964d-158">-WhatIf</span></span>
<span data-ttu-id="7964d-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7964d-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7964d-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7964d-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7964d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7964d-161">CommonParameters</span></span>
<span data-ttu-id="7964d-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7964d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7964d-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7964d-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7964d-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7964d-164">INPUTS</span></span>

### <span data-ttu-id="7964d-165">Keine</span><span class="sxs-lookup"><span data-stu-id="7964d-165">None</span></span>

## <span data-ttu-id="7964d-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7964d-166">OUTPUTS</span></span>

### <span data-ttu-id="7964d-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="7964d-167">System.Object</span></span>

## <span data-ttu-id="7964d-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="7964d-168">NOTES</span></span>

## <span data-ttu-id="7964d-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7964d-169">RELATED LINKS</span></span>

[<span data-ttu-id="7964d-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7964d-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7964d-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7964d-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
