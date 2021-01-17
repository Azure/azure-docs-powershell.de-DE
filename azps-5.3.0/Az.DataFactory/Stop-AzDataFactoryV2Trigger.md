---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472622"
---
# <span data-ttu-id="f3232-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f3232-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="f3232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3232-102">SYNOPSIS</span></span>
<span data-ttu-id="f3232-103">Beendet einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="f3232-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="f3232-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3232-104">SYNTAX</span></span>

### <span data-ttu-id="f3232-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3232-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3232-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3232-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3232-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3232-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3232-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3232-108">DESCRIPTION</span></span>
<span data-ttu-id="f3232-109">Das **Cmdlet "Stop-AzDataFactoryV2Trigger"** beendet einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="f3232-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="f3232-110">Wenn sich der Trigger im Zustand "Gestartet" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="f3232-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="f3232-111">Wenn sich der Trigger bereits im Zustand "Beendet" befindet, hat dieses Cmdlet keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="f3232-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="f3232-112">Wenn der Parameter "Force" angegeben ist, fordert das Cmdlet vor dem Beenden des Triggers keine Eingabeaufforderung an.</span><span class="sxs-lookup"><span data-stu-id="f3232-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="f3232-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3232-113">EXAMPLES</span></span>

### <span data-ttu-id="f3232-114">Beispiel 1: Beenden eines Triggers</span><span class="sxs-lookup"><span data-stu-id="f3232-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="f3232-115">Beendet einen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="f3232-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="f3232-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3232-116">PARAMETERS</span></span>

### <span data-ttu-id="f3232-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f3232-117">-DataFactoryName</span></span>
<span data-ttu-id="f3232-118">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="f3232-118">The data factory name.</span></span>

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

### <span data-ttu-id="f3232-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3232-119">-DefaultProfile</span></span>
<span data-ttu-id="f3232-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3232-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3232-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f3232-121">-Force</span></span>
<span data-ttu-id="f3232-122">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="f3232-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f3232-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3232-123">-InputObject</span></span>
<span data-ttu-id="f3232-124">Auslösen des Startobjekts</span><span class="sxs-lookup"><span data-stu-id="f3232-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="f3232-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f3232-125">-Name</span></span>
<span data-ttu-id="f3232-126">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="f3232-126">The trigger name.</span></span>

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

### <span data-ttu-id="f3232-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3232-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3232-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3232-128">The resource group name.</span></span>

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

### <span data-ttu-id="f3232-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3232-129">-ResourceId</span></span>
<span data-ttu-id="f3232-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f3232-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f3232-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3232-131">-Confirm</span></span>
<span data-ttu-id="f3232-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3232-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3232-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f3232-133">-WhatIf</span></span>
<span data-ttu-id="f3232-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3232-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f3232-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3232-135">CommonParameters</span></span>
<span data-ttu-id="f3232-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3232-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3232-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3232-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3232-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3232-138">INPUTS</span></span>

### <span data-ttu-id="f3232-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f3232-139">System.String</span></span>

### <span data-ttu-id="f3232-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f3232-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f3232-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3232-141">OUTPUTS</span></span>

### <span data-ttu-id="f3232-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f3232-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f3232-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f3232-143">NOTES</span></span>

## <span data-ttu-id="f3232-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f3232-144">RELATED LINKS</span></span>

[<span data-ttu-id="f3232-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f3232-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f3232-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f3232-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f3232-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f3232-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="f3232-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="f3232-148">Remove-AzDataFactoryV2Trigger</span></span>]()
