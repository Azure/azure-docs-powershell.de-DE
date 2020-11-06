---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501666"
---
# <span data-ttu-id="abb24-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="abb24-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="abb24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abb24-102">SYNOPSIS</span></span>
<span data-ttu-id="abb24-103">Aktualisiert eine Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="abb24-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb24-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb24-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb24-105">DESCRIPTION</span></span>
<span data-ttu-id="abb24-106">Das Cmdlet **Update-AzureRmRecoveryServicesAsrPolicy** aktualisiert die angegebene Azure Site Recovery-Replikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="abb24-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="abb24-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abb24-107">EXAMPLES</span></span>

### <span data-ttu-id="abb24-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abb24-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="abb24-109">Startet den Update-Replikationsrichtlinien Vorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abb24-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="abb24-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb24-110">PARAMETERS</span></span>

### <span data-ttu-id="abb24-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="abb24-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="abb24-112">Gibt die Häufigkeit (in Stunden) an, mit der anwendungskonsistente Wiederherstellungspunkte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="abb24-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="abb24-113">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="abb24-113">-Authentication</span></span>
<span data-ttu-id="abb24-114">Gibt den verwendeten Authentifizierungstyp an.</span><span class="sxs-lookup"><span data-stu-id="abb24-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="abb24-115">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="abb24-115">Valid values are:</span></span>

- <span data-ttu-id="abb24-116">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="abb24-116">Certificate</span></span>
-  <span data-ttu-id="abb24-117">Kerberos</span><span class="sxs-lookup"><span data-stu-id="abb24-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-118">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="abb24-118">-Compression</span></span>
<span data-ttu-id="abb24-119">Gibt an, ob die Komprimierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb24-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-120">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="abb24-120">-Encryption</span></span>
<span data-ttu-id="abb24-121">Gibt an, ob die Verschlüsselung aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb24-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="abb24-122">-InputObject</span></span>
<span data-ttu-id="abb24-123">Eingabeobjekt für das Cmdlet: gibt das ASR-Replikationsrichtlinien Objekt an, das der zu aktualisierden Replikationsrichtlinie entspricht.</span><span class="sxs-lookup"><span data-stu-id="abb24-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="abb24-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="abb24-125">Gibt die zu speichernden Nummern Wiederherstellungspunkte an.</span><span class="sxs-lookup"><span data-stu-id="abb24-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="abb24-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="abb24-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="abb24-127">Gibt die Azure-Speicherkonto-ID des Replikations Ziels an.</span><span class="sxs-lookup"><span data-stu-id="abb24-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="abb24-128">Wird als Zielspeicher Konto für die Replikation verwendet, wenn keine Alternative bereitgestellt wird, während die Replikation mithilfe des New-AzureRmRecoveryServicesASRReplicationProtectedItem-Cmdlets aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="abb24-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="abb24-129">-ReplicaDeletion</span></span>
<span data-ttu-id="abb24-130">Gibt an, ob der virtuelle replikatcomputer beim Deaktivieren der Replikation von einer VMM-verwalteten Website zu einem anderen gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="abb24-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="abb24-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="abb24-132">Gibt das Replikations Häufigkeitsintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="abb24-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="abb24-133">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="abb24-133">Valid values are:</span></span>

- <span data-ttu-id="abb24-134">30</span><span class="sxs-lookup"><span data-stu-id="abb24-134">30</span></span>
- <span data-ttu-id="abb24-135">300</span><span class="sxs-lookup"><span data-stu-id="abb24-135">300</span></span>
- <span data-ttu-id="abb24-136">900</span><span class="sxs-lookup"><span data-stu-id="abb24-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="abb24-137">-ReplicationMethod</span></span>
<span data-ttu-id="abb24-138">Gibt die Replikationsmethode an.</span><span class="sxs-lookup"><span data-stu-id="abb24-138">Specifies the replication method.</span></span>
<span data-ttu-id="abb24-139">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="abb24-139">Valid values are:</span></span>

- <span data-ttu-id="abb24-140">Online</span><span class="sxs-lookup"><span data-stu-id="abb24-140">Online</span></span>
- <span data-ttu-id="abb24-141">Offline</span><span class="sxs-lookup"><span data-stu-id="abb24-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="abb24-142">-ReplicationPort</span></span>
<span data-ttu-id="abb24-143">Gibt den Port an, der für die Replikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abb24-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb24-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="abb24-144">-ReplicationStartTime</span></span>
<span data-ttu-id="abb24-145">Gibt die Startzeit der Replikation an.</span><span class="sxs-lookup"><span data-stu-id="abb24-145">Specifies the replication start time.</span></span>
<span data-ttu-id="abb24-146">Sie darf nicht später als 24 Stunden nach dem Start des Auftrags erfolgen.</span><span class="sxs-lookup"><span data-stu-id="abb24-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="abb24-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abb24-147">-Confirm</span></span>
<span data-ttu-id="abb24-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abb24-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb24-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb24-149">-WhatIf</span></span>
<span data-ttu-id="abb24-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb24-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abb24-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abb24-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb24-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb24-152">CommonParameters</span></span>
<span data-ttu-id="abb24-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb24-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb24-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb24-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb24-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abb24-155">INPUTS</span></span>

### <span data-ttu-id="abb24-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="abb24-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="abb24-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abb24-157">OUTPUTS</span></span>

### <span data-ttu-id="abb24-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="abb24-158">System.Object</span></span>

## <span data-ttu-id="abb24-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="abb24-159">NOTES</span></span>

## <span data-ttu-id="abb24-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abb24-160">RELATED LINKS</span></span>

