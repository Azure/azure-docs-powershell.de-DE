---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 7356f6f0235f73207582303b46459d28dffbe6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925056"
---
# <span data-ttu-id="dc7d2-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="dc7d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7d2-103">Beendet einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="dc7d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc7d2-104">SYNTAX</span></span>

### <span data-ttu-id="dc7d2-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc7d2-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc7d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc7d2-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc7d2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc7d2-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc7d2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc7d2-108">DESCRIPTION</span></span>
<span data-ttu-id="dc7d2-109">Das **Cmdlet Stop-AzDataFactoryV2Trigger** beendet einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="dc7d2-110">Wenn sich der Trigger im Zustand "Gestartet" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="dc7d2-111">Wenn sich der Trigger bereits im Zustand "Beendet" befindet, hat dieses Cmdlet keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="dc7d2-112">Wenn der Parameter Erzwingen angegeben ist, wird das Cmdlet vor dem Beenden des Triggers nicht aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="dc7d2-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc7d2-113">EXAMPLES</span></span>

### <span data-ttu-id="dc7d2-114">Beispiel 1: Beenden eines Triggers</span><span class="sxs-lookup"><span data-stu-id="dc7d2-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="dc7d2-115">Beendet einen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="dc7d2-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="dc7d2-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc7d2-116">PARAMETERS</span></span>

### <span data-ttu-id="dc7d2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dc7d2-117">-DataFactoryName</span></span>
<span data-ttu-id="dc7d2-118">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7d2-119">-DefaultProfile</span></span>
<span data-ttu-id="dc7d2-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc7d2-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="dc7d2-121">-Force</span></span>
<span data-ttu-id="dc7d2-122">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc7d2-123">-InputObject</span></span>
<span data-ttu-id="dc7d2-124">Start des Triggerobjekts</span><span class="sxs-lookup"><span data-stu-id="dc7d2-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dc7d2-125">-Name</span></span>
<span data-ttu-id="dc7d2-126">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc7d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc7d2-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc7d2-129">-ResourceId</span></span>
<span data-ttu-id="dc7d2-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7d2-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dc7d2-131">-Confirm</span></span>
<span data-ttu-id="dc7d2-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc7d2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc7d2-133">-WhatIf</span></span>
<span data-ttu-id="dc7d2-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="dc7d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7d2-135">CommonParameters</span></span>
<span data-ttu-id="dc7d2-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc7d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7d2-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc7d2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7d2-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc7d2-138">INPUTS</span></span>

### <span data-ttu-id="dc7d2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dc7d2-139">System.String</span></span>

### <span data-ttu-id="dc7d2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="dc7d2-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc7d2-141">OUTPUTS</span></span>

### <span data-ttu-id="dc7d2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="dc7d2-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc7d2-143">NOTES</span></span>

## <span data-ttu-id="dc7d2-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc7d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc7d2-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="dc7d2-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="dc7d2-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="dc7d2-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="dc7d2-148">Remove-AzDataFactoryV2Trigger</span></span>]()
