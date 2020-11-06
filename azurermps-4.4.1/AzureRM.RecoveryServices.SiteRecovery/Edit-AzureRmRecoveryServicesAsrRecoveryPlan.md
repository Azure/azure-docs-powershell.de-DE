---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503221"
---
# <span data-ttu-id="f6263-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6263-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f6263-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6263-102">SYNOPSIS</span></span>
<span data-ttu-id="f6263-103">Bearbeitet einen Website Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="f6263-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6263-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6263-104">SYNTAX</span></span>

### <span data-ttu-id="f6263-105">Appendgroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6263-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6263-106">Entfernen vongroup</span><span class="sxs-lookup"><span data-stu-id="f6263-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6263-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f6263-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6263-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f6263-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6263-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6263-109">DESCRIPTION</span></span>
<span data-ttu-id="f6263-110">Das Cmdlet " **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** " bearbeitet einen Azure Site Recovery-Plan.</span><span class="sxs-lookup"><span data-stu-id="f6263-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="f6263-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6263-111">EXAMPLES</span></span>

### <span data-ttu-id="f6263-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6263-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="f6263-113">Fügt eine Gruppe an den vorhandenen Azure Site Recovery-Wiederherstellungsplan an und gibt den im Arbeitsspeicher aktualisierten Wiederherstellungsplan zurück.</span><span class="sxs-lookup"><span data-stu-id="f6263-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="f6263-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6263-114">PARAMETERS</span></span>

### <span data-ttu-id="f6263-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f6263-115">-AddProtectedItem</span></span>
<span data-ttu-id="f6263-116">Liste der geschützten Elemente der ASR-Replikation, die der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6263-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-117">-Appendgroup</span><span class="sxs-lookup"><span data-stu-id="f6263-117">-AppendGroup</span></span>
<span data-ttu-id="f6263-118">Parameter wechseln, um eine Wiederherstellungsplan Gruppe an das Wiederherstellungsplan Objekt anzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6263-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-119">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="f6263-119">-Group</span></span>
<span data-ttu-id="f6263-120">Gibt eine Gruppe für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="f6263-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6263-121">-InputObject</span></span>
<span data-ttu-id="f6263-122">Das zu bearbeitende ASR-Wiederherstellungsplan Objekt (im Arbeitsspeicher Vorgang)</span><span class="sxs-lookup"><span data-stu-id="f6263-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="f6263-123">So aktualisieren Sie den Wiederherstellungsplan, der Update-AzureRmASRRecoveryPlan mit dem geänderten Wiederherstellungsplan-Objekt ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="f6263-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-124">-Removegroup</span><span class="sxs-lookup"><span data-stu-id="f6263-124">-RemoveGroup</span></span>
<span data-ttu-id="f6263-125">Entfernt die angegebene Gruppe aus dem Wiederherstellungsplan-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6263-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f6263-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="f6263-127">Liste der geschützten Elemente der ASR-Replikation, die aus der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6263-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6263-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6263-128">-Confirm</span></span>
<span data-ttu-id="f6263-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6263-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6263-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6263-130">-WhatIf</span></span>
<span data-ttu-id="f6263-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6263-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6263-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6263-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6263-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6263-133">CommonParameters</span></span>
<span data-ttu-id="f6263-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6263-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6263-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6263-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6263-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6263-136">INPUTS</span></span>

### <span data-ttu-id="f6263-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6263-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f6263-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6263-138">OUTPUTS</span></span>

### <span data-ttu-id="f6263-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="f6263-139">System.Object</span></span>

## <span data-ttu-id="f6263-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6263-140">NOTES</span></span>

## <span data-ttu-id="f6263-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6263-141">RELATED LINKS</span></span>

[<span data-ttu-id="f6263-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6263-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f6263-143">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6263-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
