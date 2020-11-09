---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298215"
---
# <span data-ttu-id="91449-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="91449-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="91449-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91449-102">SYNOPSIS</span></span>
<span data-ttu-id="91449-103">Startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="91449-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="91449-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91449-104">SYNTAX</span></span>

### <span data-ttu-id="91449-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="91449-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91449-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91449-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91449-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91449-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91449-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91449-108">DESCRIPTION</span></span>
<span data-ttu-id="91449-109">Das Cmdlet **Start-AzDataFactoryV2Trigger** startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="91449-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="91449-110">Wenn sich der Trigger im Zustand "stopped" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="91449-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="91449-111">Wenn sich der Trigger bereits im Zustand "Started" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="91449-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="91449-112">Wenn der Parameter Force angegeben wird, wird das Cmdlet vor dem Starten des Triggers nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="91449-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="91449-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91449-113">EXAMPLES</span></span>

### <span data-ttu-id="91449-114">Beispiel 1: Starten eines Triggers</span><span class="sxs-lookup"><span data-stu-id="91449-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="91449-115">Startet einen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="91449-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="91449-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="91449-116">PARAMETERS</span></span>

### <span data-ttu-id="91449-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="91449-117">-DataFactoryName</span></span>
<span data-ttu-id="91449-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="91449-118">The data factory name.</span></span>

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

### <span data-ttu-id="91449-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91449-119">-DefaultProfile</span></span>
<span data-ttu-id="91449-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91449-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91449-121">-Force</span><span class="sxs-lookup"><span data-stu-id="91449-121">-Force</span></span>
<span data-ttu-id="91449-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="91449-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="91449-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91449-123">-InputObject</span></span>
<span data-ttu-id="91449-124">Trigger-Objekt, das gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="91449-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="91449-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91449-125">-Name</span></span>
<span data-ttu-id="91449-126">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="91449-126">The trigger name.</span></span>

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

### <span data-ttu-id="91449-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91449-127">-ResourceGroupName</span></span>
<span data-ttu-id="91449-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="91449-128">The resource group name.</span></span>

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

### <span data-ttu-id="91449-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="91449-129">-ResourceId</span></span>
<span data-ttu-id="91449-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="91449-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="91449-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91449-131">-Confirm</span></span>
<span data-ttu-id="91449-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91449-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91449-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91449-133">-WhatIf</span></span>
<span data-ttu-id="91449-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91449-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="91449-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91449-135">CommonParameters</span></span>
<span data-ttu-id="91449-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91449-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91449-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91449-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91449-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91449-138">INPUTS</span></span>

### <span data-ttu-id="91449-139">System. String</span><span class="sxs-lookup"><span data-stu-id="91449-139">System.String</span></span>

### <span data-ttu-id="91449-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="91449-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="91449-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91449-141">OUTPUTS</span></span>

### <span data-ttu-id="91449-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="91449-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="91449-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="91449-143">NOTES</span></span>

## <span data-ttu-id="91449-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91449-144">RELATED LINKS</span></span>

[<span data-ttu-id="91449-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="91449-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="91449-146">Satz-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="91449-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="91449-147">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="91449-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="91449-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="91449-148">Remove-AzDataFactoryV2Trigger</span></span>]()
