---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847084"
---
# <span data-ttu-id="473e7-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="473e7-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="473e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="473e7-102">SYNOPSIS</span></span>
<span data-ttu-id="473e7-103">Beendet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="473e7-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="473e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="473e7-104">SYNTAX</span></span>

### <span data-ttu-id="473e7-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="473e7-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473e7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="473e7-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473e7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="473e7-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473e7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="473e7-108">DESCRIPTION</span></span>
<span data-ttu-id="473e7-109">Das Cmdlet **Stop-AzDataFactoryV2Trigger** beendet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="473e7-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="473e7-110">Wenn sich der Trigger im Zustand "Started" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="473e7-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="473e7-111">Wenn sich der Trigger bereits im Zustand "beendet" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="473e7-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="473e7-112">Wenn der Parameter Force angegeben wird, fordert das Cmdlet vor dem Beenden des Triggers nicht auf.</span><span class="sxs-lookup"><span data-stu-id="473e7-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="473e7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="473e7-113">EXAMPLES</span></span>

### <span data-ttu-id="473e7-114">Beispiel 1: Beenden eines Triggers</span><span class="sxs-lookup"><span data-stu-id="473e7-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="473e7-115">Beendet einen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="473e7-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="473e7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="473e7-116">PARAMETERS</span></span>

### <span data-ttu-id="473e7-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="473e7-117">-DataFactoryName</span></span>
<span data-ttu-id="473e7-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="473e7-118">The data factory name.</span></span>

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

### <span data-ttu-id="473e7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473e7-119">-DefaultProfile</span></span>
<span data-ttu-id="473e7-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="473e7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="473e7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="473e7-121">-Force</span></span>
<span data-ttu-id="473e7-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="473e7-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="473e7-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="473e7-123">-InputObject</span></span>
<span data-ttu-id="473e7-124">Trigger-Objekt, das gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="473e7-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="473e7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="473e7-125">-Name</span></span>
<span data-ttu-id="473e7-126">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="473e7-126">The trigger name.</span></span>

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

### <span data-ttu-id="473e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="473e7-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="473e7-128">The resource group name.</span></span>

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

### <span data-ttu-id="473e7-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="473e7-129">-ResourceId</span></span>
<span data-ttu-id="473e7-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="473e7-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="473e7-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="473e7-131">-Confirm</span></span>
<span data-ttu-id="473e7-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="473e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473e7-133">-WhatIf</span></span>
<span data-ttu-id="473e7-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="473e7-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="473e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473e7-135">CommonParameters</span></span>
<span data-ttu-id="473e7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473e7-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473e7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473e7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="473e7-138">INPUTS</span></span>

### <span data-ttu-id="473e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="473e7-139">System.String</span></span>

### <span data-ttu-id="473e7-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="473e7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="473e7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="473e7-141">OUTPUTS</span></span>

### <span data-ttu-id="473e7-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="473e7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="473e7-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="473e7-143">NOTES</span></span>

## <span data-ttu-id="473e7-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="473e7-144">RELATED LINKS</span></span>

[<span data-ttu-id="473e7-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="473e7-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="473e7-146">Satz-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="473e7-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="473e7-147">Anfang-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="473e7-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="473e7-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="473e7-148">Remove-AzDataFactoryV2Trigger</span></span>]()
