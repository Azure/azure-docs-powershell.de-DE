---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505966"
---
# <span data-ttu-id="a1401-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a1401-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="a1401-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1401-102">SYNOPSIS</span></span>

<span data-ttu-id="a1401-103">Startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1401-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1401-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1401-104">SYNTAX</span></span>

### <span data-ttu-id="a1401-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1401-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1401-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1401-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a1401-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1401-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a1401-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1401-108">DESCRIPTION</span></span>

<span data-ttu-id="a1401-109">Das Cmdlet **Start-AzureRmDataFactoryV2Trigger** startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1401-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="a1401-110">Wenn sich der Trigger im Zustand "stopped" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="a1401-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="a1401-111">Wenn sich der Trigger bereits im Zustand "Started" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="a1401-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="a1401-112">Wenn der Parameter Force angegeben wird, wird das Cmdlet vor dem Starten des Triggers nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="a1401-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="a1401-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1401-113">EXAMPLES</span></span>

### <span data-ttu-id="a1401-114">Beispiel 1: Starten eines Triggers</span><span class="sxs-lookup"><span data-stu-id="a1401-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="a1401-115">Startet einen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="a1401-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="a1401-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1401-116">PARAMETERS</span></span>

### <span data-ttu-id="a1401-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1401-117">-Confirm</span></span>
<span data-ttu-id="a1401-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1401-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1401-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a1401-119">-DataFactoryName</span></span>
<span data-ttu-id="a1401-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a1401-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a1401-121">-Force</span></span>
<span data-ttu-id="a1401-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a1401-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a1401-123">-Name</span></span>
<span data-ttu-id="a1401-124">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="a1401-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1401-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1401-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1401-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1401-127">-ResourceId</span></span>
<span data-ttu-id="a1401-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a1401-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1401-129">-InputObject</span></span>
<span data-ttu-id="a1401-130">Trigger-Objekt, das gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1401-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1401-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1401-131">-WhatIf</span></span>
<span data-ttu-id="a1401-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1401-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="a1401-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1401-133">INPUTS</span></span>

### <span data-ttu-id="a1401-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a1401-134">System.String</span></span>
<span data-ttu-id="a1401-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a1401-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="a1401-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1401-136">OUTPUTS</span></span>

### <span data-ttu-id="a1401-137">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a1401-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="a1401-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a1401-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="a1401-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1401-139">NOTES</span></span>

## <span data-ttu-id="a1401-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1401-140">RELATED LINKS</span></span>
[<span data-ttu-id="a1401-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a1401-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a1401-142">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a1401-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a1401-143">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a1401-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a1401-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a1401-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
