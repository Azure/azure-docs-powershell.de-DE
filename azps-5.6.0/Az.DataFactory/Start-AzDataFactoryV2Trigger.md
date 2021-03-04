---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d9ce325979a40315341a0e43049bd2c5bb512622
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925059"
---
# <span data-ttu-id="7d0e1-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="7d0e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0e1-103">Startet einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="7d0e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d0e1-104">SYNTAX</span></span>

### <span data-ttu-id="7d0e1-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d0e1-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7d0e1-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d0e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d0e1-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d0e1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d0e1-108">DESCRIPTION</span></span>
<span data-ttu-id="7d0e1-109">Das **Cmdlet Start-AzDataFactoryV2Trigger** startet einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="7d0e1-110">Wenn sich der Trigger im Zustand "Beendet" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="7d0e1-111">Wenn sich der Trigger bereits im Zustand "Gestartet" befindet, hat dieses Cmdlet keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="7d0e1-112">Wenn der Parameter Erzwingen angegeben ist, wird das Cmdlet vor dem Starten des Triggers nicht aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="7d0e1-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d0e1-113">EXAMPLES</span></span>

### <span data-ttu-id="7d0e1-114">Beispiel 1: Starten eines Triggers</span><span class="sxs-lookup"><span data-stu-id="7d0e1-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="7d0e1-115">Startet einen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="7d0e1-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="7d0e1-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7d0e1-116">PARAMETERS</span></span>

### <span data-ttu-id="7d0e1-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d0e1-117">-DataFactoryName</span></span>
<span data-ttu-id="7d0e1-118">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-118">The data factory name.</span></span>

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

### <span data-ttu-id="7d0e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0e1-119">-DefaultProfile</span></span>
<span data-ttu-id="7d0e1-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d0e1-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7d0e1-121">-Force</span></span>
<span data-ttu-id="7d0e1-122">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7d0e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d0e1-123">-InputObject</span></span>
<span data-ttu-id="7d0e1-124">Start des Triggerobjekts</span><span class="sxs-lookup"><span data-stu-id="7d0e1-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="7d0e1-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7d0e1-125">-Name</span></span>
<span data-ttu-id="7d0e1-126">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-126">The trigger name.</span></span>

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

### <span data-ttu-id="7d0e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d0e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d0e1-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-128">The resource group name.</span></span>

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

### <span data-ttu-id="7d0e1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d0e1-129">-ResourceId</span></span>
<span data-ttu-id="7d0e1-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7d0e1-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d0e1-131">-Confirm</span></span>
<span data-ttu-id="7d0e1-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d0e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d0e1-133">-WhatIf</span></span>
<span data-ttu-id="7d0e1-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7d0e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0e1-135">CommonParameters</span></span>
<span data-ttu-id="7d0e1-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d0e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0e1-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0e1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0e1-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d0e1-138">INPUTS</span></span>

### <span data-ttu-id="7d0e1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7d0e1-139">System.String</span></span>

### <span data-ttu-id="7d0e1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7d0e1-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d0e1-141">OUTPUTS</span></span>

### <span data-ttu-id="7d0e1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="7d0e1-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7d0e1-143">NOTES</span></span>

## <span data-ttu-id="7d0e1-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7d0e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="7d0e1-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d0e1-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d0e1-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="7d0e1-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="7d0e1-148">Remove-AzDataFactoryV2Trigger</span></span>]()
