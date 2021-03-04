---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: 78aa310d6fd3cdb7a27de066e234744b3e450520
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943948"
---
# <span data-ttu-id="f2345-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f2345-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="f2345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2345-102">SYNOPSIS</span></span>
<span data-ttu-id="f2345-103">Startet einen geplanten Failovervorgang.</span><span class="sxs-lookup"><span data-stu-id="f2345-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="f2345-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2345-104">SYNTAX</span></span>

### <span data-ttu-id="f2345-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2345-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2345-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f2345-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2345-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2345-107">DESCRIPTION</span></span>
<span data-ttu-id="f2345-108">Das **Cmdlet "Start-AzRecoveryServicesAsrPlannedFailoverJob"** startet ein geplantes Failover für ein geschütztes Element oder einen Wiederherstellungsplan für azuree Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="f2345-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f2345-109">Sie können überprüfen, ob der Auftrag erfolgreich ist, indem Sie das cmdlet Get-AzRecoveryServicesAsrJob verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2345-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f2345-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2345-110">EXAMPLES</span></span>

### <span data-ttu-id="f2345-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2345-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="f2345-112">Startet das geplante Failover für den angegebenen ASR-Wiederherstellungsplan und gibt den ZUM Nachverfolgen des Vorgangs verwendeten ASR-Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="f2345-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f2345-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f2345-113">PARAMETERS</span></span>

### <span data-ttu-id="f2345-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="f2345-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="f2345-115">Erstellen Sie den virtuellen Computer, wenn er nicht gefunden wird, während der Fehler wieder zum primären Bereich zurückfehlt (wird in der Wiederherstellung alternativer Speicherorte verwendet).) Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f2345-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2345-116">Ja</span><span class="sxs-lookup"><span data-stu-id="f2345-116">Yes</span></span>
- <span data-ttu-id="f2345-117">Nein</span><span class="sxs-lookup"><span data-stu-id="f2345-117">No</span></span>

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

### <span data-ttu-id="f2345-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f2345-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f2345-119">Gibt die primäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="f2345-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f2345-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f2345-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f2345-121">Gibt die sekundäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="f2345-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f2345-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2345-122">-DefaultProfile</span></span>
<span data-ttu-id="f2345-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2345-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f2345-124">-Richtung</span><span class="sxs-lookup"><span data-stu-id="f2345-124">-Direction</span></span>
<span data-ttu-id="f2345-125">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="f2345-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f2345-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="f2345-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2345-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f2345-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="f2345-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f2345-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f2345-129">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="f2345-129">-Optimize</span></span>
<span data-ttu-id="f2345-130">Gibt an, wofür optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2345-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="f2345-131">Dieser Parameter gilt, wenn ein Failover von einer Azure-Website auf eine lokale Website erfolgt, die eine umfangreiche Datensynchronisierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="f2345-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="f2345-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f2345-132">Valid values are:</span></span>

- <span data-ttu-id="f2345-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="f2345-133">ForDowntime</span></span>
- <span data-ttu-id="f2345-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="f2345-134">ForSynchronization</span></span>

<span data-ttu-id="f2345-135">Wenn **ForDowntime** angegeben wird, gibt dies an, dass Daten vor dem Failover synchronisiert werden, um Ausfallzeiten zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="f2345-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="f2345-136">Die Synchronisierung wird ohne Herunterfahren des virtuellen Computers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2345-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="f2345-137">Nach Abschluss der Synchronisierung wird der Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="f2345-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="f2345-138">Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang zum Herunterfahren des virtuellen Computers zu durchführen.</span><span class="sxs-lookup"><span data-stu-id="f2345-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="f2345-139">Wenn **ForSynchronization** angegeben wird, gibt dies an, dass Daten nur während des Failovers synchronisiert werden, damit die Datensynchronisierung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2345-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="f2345-140">Wenn diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="f2345-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="f2345-141">Die Synchronisierung wird nach dem Herunterfahren gestartet, um den Failovervorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f2345-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="f2345-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2345-142">-RecoveryPlan</span></span>
<span data-ttu-id="f2345-143">Gibt das ASR-Wiederherstellungsplanobjekt an, das dem Wiederherstellungsplan entspricht, für den ein Fehler vorprogrammiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2345-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="f2345-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f2345-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f2345-145">Gibt das asr-replikationsgeschützte Elementobjekt an, das dem replikationsgeschützten Element entspricht, das fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="f2345-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="f2345-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f2345-146">-ServicesProvider</span></span>
<span data-ttu-id="f2345-147">Gibt den Host an, auf dem der virtuelle Computer erstellt werden soll, während ein Fehler an einem alternativen Speicherort ausgeführt wird, indem das ASR-Anbieterobjekt angegeben wird, das dem auf dem Host ausgeführten ASR-Dienstanbieter entspricht.</span><span class="sxs-lookup"><span data-stu-id="f2345-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="f2345-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2345-148">-Confirm</span></span>
<span data-ttu-id="f2345-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2345-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2345-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2345-150">-WhatIf</span></span>
<span data-ttu-id="f2345-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2345-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2345-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2345-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2345-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2345-153">CommonParameters</span></span>
<span data-ttu-id="f2345-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2345-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2345-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2345-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2345-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2345-156">INPUTS</span></span>

### <span data-ttu-id="f2345-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2345-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f2345-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f2345-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f2345-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2345-159">OUTPUTS</span></span>

### <span data-ttu-id="f2345-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f2345-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f2345-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f2345-161">NOTES</span></span>

## <span data-ttu-id="f2345-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f2345-162">RELATED LINKS</span></span>
