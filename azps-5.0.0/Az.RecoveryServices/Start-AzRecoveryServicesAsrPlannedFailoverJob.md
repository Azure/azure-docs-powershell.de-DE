---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180049"
---
# <span data-ttu-id="26b20-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="26b20-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="26b20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26b20-102">SYNOPSIS</span></span>
<span data-ttu-id="26b20-103">Startet einen geplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="26b20-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="26b20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26b20-104">SYNTAX</span></span>

### <span data-ttu-id="26b20-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="26b20-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26b20-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="26b20-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26b20-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26b20-107">DESCRIPTION</span></span>
<span data-ttu-id="26b20-108">Das Cmdlet **Start-AzRecoveryServicesAsrPlannedFailoverJob** startet ein Geplantes Failover für ein geschütztes Element oder einen Wiederherstellungsplan für eine Azure-Site-Wiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="26b20-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="26b20-109">Mithilfe des Get-AzRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="26b20-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="26b20-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26b20-110">EXAMPLES</span></span>

### <span data-ttu-id="26b20-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26b20-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="26b20-112">Startet das geplante Failover für den angegebenen ASR-Wiederherstellungsplan und gibt den zum Nachvollziehen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="26b20-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="26b20-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="26b20-113">PARAMETERS</span></span>

### <span data-ttu-id="26b20-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="26b20-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="26b20-115">Erstellen Sie den virtuellen Computer, wenn er nicht gefunden wird, während der Fehler zurück in den primären Bereich fällt (wird bei der alternativen Standortwiederherstellung verwendet). Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="26b20-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26b20-116">Ja</span><span class="sxs-lookup"><span data-stu-id="26b20-116">Yes</span></span>
- <span data-ttu-id="26b20-117">Nein</span><span class="sxs-lookup"><span data-stu-id="26b20-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="26b20-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="26b20-119">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="26b20-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="26b20-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="26b20-121">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="26b20-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b20-122">-DefaultProfile</span></span>
<span data-ttu-id="26b20-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26b20-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="26b20-124">-Richtung</span><span class="sxs-lookup"><span data-stu-id="26b20-124">-Direction</span></span>
<span data-ttu-id="26b20-125">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="26b20-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="26b20-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="26b20-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26b20-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="26b20-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="26b20-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="26b20-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-129">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="26b20-129">-Optimize</span></span>
<span data-ttu-id="26b20-130">Gibt an, was optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26b20-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="26b20-131">Dieser Parameter gilt, wenn ein Failover von einer Azure-Website zu einer lokalen Website durchgeführt wird, für die eine beträchtliche Datensynchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="26b20-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="26b20-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="26b20-132">Valid values are:</span></span>

- <span data-ttu-id="26b20-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="26b20-133">ForDowntime</span></span>
- <span data-ttu-id="26b20-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="26b20-134">ForSynchronization</span></span>

<span data-ttu-id="26b20-135">Wenn **ForDowntime** angegeben wird, bedeutet dies, dass Daten vor dem Failover synchronisiert werden, um die Ausfallzeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="26b20-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="26b20-136">Die Synchronisierung wird ausgeführt, ohne den virtuellen Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="26b20-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="26b20-137">Nach Abschluss der Synchronisierung wird der Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="26b20-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="26b20-138">Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang auszuführen, der den virtuellen Computer herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="26b20-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="26b20-139">Wenn **ForSynchronization** angegeben wird, bedeutet dies, dass Daten während des Failovers nur synchronisiert werden, damit die Datensynchronisierung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="26b20-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="26b20-140">Wenn diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="26b20-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="26b20-141">Die Synchronisierung beginnt nach dem Herunterfahren, um den Failovervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="26b20-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26b20-142">-RecoveryPlan</span></span>
<span data-ttu-id="26b20-143">Gibt das ASR-Wiederherstellungsplan Objekt entsprechend dem Wiederherstellungsplan für einen Failover an.</span><span class="sxs-lookup"><span data-stu-id="26b20-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="26b20-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26b20-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="26b20-145">Gibt das Objekt der ASR-Replikations geschützten Elemente an, das dem zu überprüfenden Replikat geschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="26b20-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="26b20-146">-ServicesProvider</span></span>
<span data-ttu-id="26b20-147">Identifiziert den Host, auf dem der virtuelle Computer erstellt werden soll, während ein Failover an einem anderen Speicherort durchführen wird, indem das ASR-Dienstanbieterobjekt angegeben wird, das dem auf dem Host ausgeführten ASR-Dienstanbieter entspricht.</span><span class="sxs-lookup"><span data-stu-id="26b20-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b20-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26b20-148">-Confirm</span></span>
<span data-ttu-id="26b20-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26b20-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b20-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b20-150">-WhatIf</span></span>
<span data-ttu-id="26b20-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26b20-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26b20-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26b20-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b20-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b20-153">CommonParameters</span></span>
<span data-ttu-id="26b20-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b20-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b20-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26b20-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b20-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26b20-156">INPUTS</span></span>

### <span data-ttu-id="26b20-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="26b20-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="26b20-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="26b20-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="26b20-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26b20-159">OUTPUTS</span></span>

### <span data-ttu-id="26b20-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="26b20-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="26b20-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="26b20-161">NOTES</span></span>

## <span data-ttu-id="26b20-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26b20-162">RELATED LINKS</span></span>
