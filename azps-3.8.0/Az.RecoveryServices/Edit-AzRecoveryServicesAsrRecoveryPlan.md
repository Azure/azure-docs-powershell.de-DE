---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: be66887225ee78b31497bbd8918faae9535731de
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846992"
---
# <span data-ttu-id="9e131-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e131-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9e131-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e131-102">SYNOPSIS</span></span>
<span data-ttu-id="9e131-103">Bearbeitet einen Website Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="9e131-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="9e131-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e131-104">SYNTAX</span></span>

### <span data-ttu-id="9e131-105">Appendgroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e131-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e131-106">Entfernen vongroup</span><span class="sxs-lookup"><span data-stu-id="9e131-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e131-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9e131-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e131-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9e131-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e131-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e131-109">DESCRIPTION</span></span>
<span data-ttu-id="9e131-110">Das Cmdlet " **Edit-AzRecoveryServicesAsrRecoveryPlan** " bearbeitet einen Azure Site Recovery-Plan.</span><span class="sxs-lookup"><span data-stu-id="9e131-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="9e131-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e131-111">EXAMPLES</span></span>

### <span data-ttu-id="9e131-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e131-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="9e131-113">Fügt eine Gruppe an den vorhandenen Azure Site Recovery-Plan an und gibt den im Arbeitsspeicher aktualisierten Wiederherstellungsplan zurück.</span><span class="sxs-lookup"><span data-stu-id="9e131-113">Appends a group to existing Azure Site Recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="9e131-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e131-114">PARAMETERS</span></span>

### <span data-ttu-id="9e131-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9e131-115">-AddProtectedItem</span></span>
<span data-ttu-id="9e131-116">Liste der geschützten Elemente der ASR-Replikation, die der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e131-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-117">-Appendgroup</span><span class="sxs-lookup"><span data-stu-id="9e131-117">-AppendGroup</span></span>
<span data-ttu-id="9e131-118">Parameter wechseln, um eine Wiederherstellungsplan Gruppe an das Wiederherstellungsplan Objekt anzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e131-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e131-119">-DefaultProfile</span></span>
<span data-ttu-id="9e131-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e131-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9e131-121">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="9e131-121">-Group</span></span>
<span data-ttu-id="9e131-122">Gibt eine Gruppe für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="9e131-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9e131-123">-InputObject</span></span>
<span data-ttu-id="9e131-124">Das zu bearbeitende ASR-Wiederherstellungsplan Objekt (im Arbeitsspeicher Vorgang)</span><span class="sxs-lookup"><span data-stu-id="9e131-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="9e131-125">So aktualisieren Sie den Wiederherstellungsplan, der Update-AzASRRecoveryPlan mit dem geänderten Wiederherstellungsplan-Objekt ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="9e131-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-126">-Removegroup</span><span class="sxs-lookup"><span data-stu-id="9e131-126">-RemoveGroup</span></span>
<span data-ttu-id="9e131-127">Entfernt die angegebene Gruppe aus dem Wiederherstellungsplan-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9e131-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9e131-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="9e131-129">Liste der geschützten Elemente der ASR-Replikation, die aus der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e131-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e131-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e131-130">-Confirm</span></span>
<span data-ttu-id="9e131-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e131-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e131-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e131-132">-WhatIf</span></span>
<span data-ttu-id="9e131-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e131-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e131-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e131-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e131-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e131-135">CommonParameters</span></span>
<span data-ttu-id="9e131-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e131-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e131-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e131-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e131-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e131-138">INPUTS</span></span>

### <span data-ttu-id="9e131-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e131-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9e131-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e131-140">OUTPUTS</span></span>

### <span data-ttu-id="9e131-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e131-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9e131-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e131-142">NOTES</span></span>

## <span data-ttu-id="9e131-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e131-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e131-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e131-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9e131-145">Neu – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9e131-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
