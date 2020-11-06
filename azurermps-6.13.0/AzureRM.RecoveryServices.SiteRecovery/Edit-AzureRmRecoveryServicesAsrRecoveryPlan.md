---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499450"
---
# <span data-ttu-id="14099-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="14099-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="14099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14099-102">SYNOPSIS</span></span>
<span data-ttu-id="14099-103">Bearbeitet einen Website Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="14099-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14099-104">SYNTAX</span></span>

### <span data-ttu-id="14099-105">Appendgroup (Standard)</span><span class="sxs-lookup"><span data-stu-id="14099-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14099-106">Entfernen vongroup</span><span class="sxs-lookup"><span data-stu-id="14099-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14099-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="14099-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14099-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="14099-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14099-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14099-109">DESCRIPTION</span></span>
<span data-ttu-id="14099-110">Das Cmdlet " **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** " bearbeitet einen Azure Site Recovery-Plan.</span><span class="sxs-lookup"><span data-stu-id="14099-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="14099-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14099-111">EXAMPLES</span></span>

### <span data-ttu-id="14099-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14099-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="14099-113">Fügt eine Gruppe an den vorhandenen Azure Site Recovery-Wiederherstellungsplan an und gibt den im Arbeitsspeicher aktualisierten Wiederherstellungsplan zurück.</span><span class="sxs-lookup"><span data-stu-id="14099-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="14099-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="14099-114">PARAMETERS</span></span>

### <span data-ttu-id="14099-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="14099-115">-AddProtectedItem</span></span>
<span data-ttu-id="14099-116">Liste der geschützten Elemente der ASR-Replikation, die der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="14099-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="14099-117">-Appendgroup</span><span class="sxs-lookup"><span data-stu-id="14099-117">-AppendGroup</span></span>
<span data-ttu-id="14099-118">Parameter wechseln, um eine Wiederherstellungsplan Gruppe an das Wiederherstellungsplan Objekt anzufügen.</span><span class="sxs-lookup"><span data-stu-id="14099-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="14099-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14099-119">-DefaultProfile</span></span>
<span data-ttu-id="14099-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14099-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="14099-121">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="14099-121">-Group</span></span>
<span data-ttu-id="14099-122">Gibt eine Gruppe für den Wiederherstellungsplan an.</span><span class="sxs-lookup"><span data-stu-id="14099-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="14099-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="14099-123">-InputObject</span></span>
<span data-ttu-id="14099-124">Das zu bearbeitende ASR-Wiederherstellungsplan Objekt (im Arbeitsspeicher Vorgang)</span><span class="sxs-lookup"><span data-stu-id="14099-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="14099-125">So aktualisieren Sie den Wiederherstellungsplan, der Update-AzureRmASRRecoveryPlan mit dem geänderten Wiederherstellungsplan-Objekt ausgeführt wird.)</span><span class="sxs-lookup"><span data-stu-id="14099-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="14099-126">-Removegroup</span><span class="sxs-lookup"><span data-stu-id="14099-126">-RemoveGroup</span></span>
<span data-ttu-id="14099-127">Entfernt die angegebene Gruppe aus dem Wiederherstellungsplan-Objekt.</span><span class="sxs-lookup"><span data-stu-id="14099-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="14099-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="14099-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="14099-129">Liste der geschützten Elemente der ASR-Replikation, die aus der Gruppe "Wiederherstellungsplan" im Wiederherstellungsplan-Objekt entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="14099-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="14099-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14099-130">-Confirm</span></span>
<span data-ttu-id="14099-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14099-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14099-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14099-132">-WhatIf</span></span>
<span data-ttu-id="14099-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14099-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14099-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14099-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14099-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14099-135">CommonParameters</span></span>
<span data-ttu-id="14099-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14099-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14099-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14099-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14099-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14099-138">INPUTS</span></span>

### <span data-ttu-id="14099-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="14099-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="14099-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14099-140">OUTPUTS</span></span>

### <span data-ttu-id="14099-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="14099-141">System.Object</span></span>

## <span data-ttu-id="14099-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="14099-142">NOTES</span></span>

## <span data-ttu-id="14099-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14099-143">RELATED LINKS</span></span>

[<span data-ttu-id="14099-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="14099-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="14099-145">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="14099-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
