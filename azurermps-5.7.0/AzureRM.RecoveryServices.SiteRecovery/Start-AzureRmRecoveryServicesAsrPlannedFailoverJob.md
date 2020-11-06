---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478293"
---
# <span data-ttu-id="e7f3d-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e7f3d-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="e7f3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f3d-103">Startet einen geplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7f3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7f3d-104">SYNTAX</span></span>

### <span data-ttu-id="e7f3d-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="e7f3d-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7f3d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e7f3d-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f3d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7f3d-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f3d-108">Das Cmdlet **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** startet ein Geplantes Failover für ein geschütztes Element oder einen Wiederherstellungsplan für eine Azure-Site-Wiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e7f3d-109">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e7f3d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7f3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f3d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7f3d-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="e7f3d-112">Startet das geplante Failover für den angegebenen ASR-Wiederherstellungsplan und gibt den zum Nachvollziehen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e7f3d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7f3d-113">PARAMETERS</span></span>

### <span data-ttu-id="e7f3d-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7f3d-114">-Confirm</span></span>
<span data-ttu-id="e7f3d-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f3d-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="e7f3d-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="e7f3d-117">Erstellen Sie den virtuellen Computer, wenn er nicht gefunden wird, während der Fehler zurück in den primären Bereich fällt (wird bei der alternativen Standortwiederherstellung verwendet). Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e7f3d-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7f3d-118">Ja</span><span class="sxs-lookup"><span data-stu-id="e7f3d-118">Yes</span></span>
- <span data-ttu-id="e7f3d-119">Nein</span><span class="sxs-lookup"><span data-stu-id="e7f3d-119">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e7f3d-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e7f3d-121">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="e7f3d-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e7f3d-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e7f3d-123">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="e7f3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f3d-124">-DefaultProfile</span></span>
<span data-ttu-id="e7f3d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-126">-Richtung</span><span class="sxs-lookup"><span data-stu-id="e7f3d-126">-Direction</span></span>
<span data-ttu-id="e7f3d-127">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="e7f3d-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e7f3d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7f3d-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e7f3d-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="e7f3d-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e7f3d-130">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-131">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="e7f3d-131">-Optimize</span></span>
<span data-ttu-id="e7f3d-132">Gibt an, was optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="e7f3d-133">Dieser Parameter gilt, wenn ein Failover von einer Azure-Website zu einer lokalen Website durchgeführt wird, für die eine beträchtliche Datensynchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="e7f3d-134">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="e7f3d-134">Valid values are:</span></span>

- <span data-ttu-id="e7f3d-135">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="e7f3d-135">ForDowntime</span></span>
- <span data-ttu-id="e7f3d-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="e7f3d-136">ForSynchronization</span></span>

<span data-ttu-id="e7f3d-137">Wenn **ForDowntime** angegeben wird, bedeutet dies, dass Daten vor dem Failover synchronisiert werden, um die Ausfallzeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="e7f3d-138">Die Synchronisierung wird ausgeführt, ohne den virtuellen Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="e7f3d-139">Nach Abschluss der Synchronisierung wird der Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="e7f3d-140">Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang auszuführen, der den virtuellen Computer herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="e7f3d-141">Wenn **ForSynchronization** angegeben wird, bedeutet dies, dass Daten während des Failovers nur synchronisiert werden, damit die Datensynchronisierung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="e7f3d-142">Wenn diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="e7f3d-143">Die Synchronisierung beginnt nach dem Herunterfahren, um den Failovervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7f3d-144">-RecoveryPlan</span></span>
<span data-ttu-id="e7f3d-145">Gibt das ASR-Wiederherstellungsplan Objekt entsprechend dem Wiederherstellungsplan für einen Failover an.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-146">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e7f3d-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e7f3d-147">Gibt das Objekt der ASR-Replikations geschützten Elemente an, das dem zu überprüfenden Replikat geschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e7f3d-148">-ServicesProvider</span></span>
<span data-ttu-id="e7f3d-149">Identifiziert den Host, auf dem der virtuelle Computer erstellt werden soll, während ein Failover an einem anderen Speicherort durchführen wird, indem das ASR-Dienstanbieterobjekt angegeben wird, das dem auf dem Host ausgeführten ASR-Dienstanbieter entspricht.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f3d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f3d-150">-WhatIf</span></span>
<span data-ttu-id="e7f3d-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f3d-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f3d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f3d-153">CommonParameters</span></span>
<span data-ttu-id="e7f3d-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f3d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f3d-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f3d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f3d-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7f3d-156">INPUTS</span></span>

### <span data-ttu-id="e7f3d-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e7f3d-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e7f3d-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e7f3d-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e7f3d-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7f3d-159">OUTPUTS</span></span>

### <span data-ttu-id="e7f3d-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e7f3d-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e7f3d-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7f3d-161">NOTES</span></span>

## <span data-ttu-id="e7f3d-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7f3d-162">RELATED LINKS</span></span>
