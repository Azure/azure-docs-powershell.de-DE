---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663858"
---
# <span data-ttu-id="b2c63-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b2c63-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="b2c63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2c63-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c63-103">Startet einen ungeplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b2c63-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2c63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2c63-104">SYNTAX</span></span>

### <span data-ttu-id="b2c63-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2c63-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2c63-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b2c63-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c63-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2c63-107">DESCRIPTION</span></span>
<span data-ttu-id="b2c63-108">Mit dem Cmdlet **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** wird das ungeplante Failover eines geschützten Elements oder Wiederherstellungsplans für die Azure Site Recovery-Replikation gestartet.</span><span class="sxs-lookup"><span data-stu-id="b2c63-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="b2c63-109">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="b2c63-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="b2c63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2c63-110">EXAMPLES</span></span>

### <span data-ttu-id="b2c63-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2c63-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="b2c63-112">Startet den ungeplanten Failover-Vorgang für den angegebenen Wiederherstellungsplan unter Verwendung der angegebenen Parameter und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2c63-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b2c63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c63-113">PARAMETERS</span></span>

### <span data-ttu-id="b2c63-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b2c63-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b2c63-115">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="b2c63-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="b2c63-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b2c63-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b2c63-117">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="b2c63-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="b2c63-118">-Richtung</span><span class="sxs-lookup"><span data-stu-id="b2c63-118">-Direction</span></span>
<span data-ttu-id="b2c63-119">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="b2c63-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="b2c63-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2c63-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2c63-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b2c63-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="b2c63-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b2c63-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b2c63-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="b2c63-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="b2c63-124">Gibt an, dass alle im Wiederherstellungsplan angegebenen Quellwebsite Vorgänge als Teil des Failovers ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b2c63-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2c63-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c63-125">-RecoveryPlan</span></span>
<span data-ttu-id="b2c63-126">Gibt ein ASR-Wiederherstellungsplan Objekt an, das dem Wiederherstellungsplan entspricht, für den der Failovervorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2c63-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="b2c63-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b2c63-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b2c63-128">Gibt das Objekt der ASR-Replikations geschützten Elemente an, das dem Replikations geschützten Element entspricht, für das der Failovervorgang durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2c63-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="b2c63-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2c63-129">-Confirm</span></span>
<span data-ttu-id="b2c63-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2c63-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c63-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c63-131">-WhatIf</span></span>
<span data-ttu-id="b2c63-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c63-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2c63-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2c63-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c63-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c63-134">CommonParameters</span></span>
<span data-ttu-id="b2c63-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c63-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c63-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c63-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c63-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2c63-137">INPUTS</span></span>

### <span data-ttu-id="b2c63-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b2c63-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="b2c63-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b2c63-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b2c63-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2c63-140">OUTPUTS</span></span>

### <span data-ttu-id="b2c63-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b2c63-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b2c63-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2c63-142">NOTES</span></span>

## <span data-ttu-id="b2c63-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2c63-143">RELATED LINKS</span></span>

[<span data-ttu-id="b2c63-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b2c63-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


