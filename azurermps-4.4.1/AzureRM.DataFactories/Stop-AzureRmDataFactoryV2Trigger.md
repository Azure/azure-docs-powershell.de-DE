---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 8e4f547d615a88957ffbf133dd725e2453ef7a11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663591"
---
# <span data-ttu-id="49e82-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="49e82-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="49e82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49e82-102">SYNOPSIS</span></span>
<span data-ttu-id="49e82-103">Beendet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="49e82-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49e82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49e82-104">SYNTAX</span></span>

### <span data-ttu-id="49e82-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="49e82-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e82-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="49e82-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49e82-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="49e82-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49e82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49e82-108">DESCRIPTION</span></span>
<span data-ttu-id="49e82-109">Das Cmdlet **Stop-AzureRmDataFactoryV2Trigger** beendet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="49e82-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="49e82-110">Wenn sich der Trigger im Zustand "Started" befindet, beendet das Cmdlet den Trigger und ruft keine Pipelines mehr auf.</span><span class="sxs-lookup"><span data-stu-id="49e82-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="49e82-111">Wenn sich der Trigger bereits im Zustand "beendet" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="49e82-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="49e82-112">Wenn der Parameter Force angegeben wird, fordert das Cmdlet vor dem Beenden des Triggers nicht auf.</span><span class="sxs-lookup"><span data-stu-id="49e82-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="49e82-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49e82-113">EXAMPLES</span></span>

### <span data-ttu-id="49e82-114">Beispiel 1: Beenden eines Triggers</span><span class="sxs-lookup"><span data-stu-id="49e82-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="49e82-115">Beendet einen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="49e82-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="49e82-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="49e82-116">PARAMETERS</span></span>

### <span data-ttu-id="49e82-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49e82-117">-Confirm</span></span>
<span data-ttu-id="49e82-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49e82-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49e82-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="49e82-119">-DataFactoryName</span></span>
<span data-ttu-id="49e82-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="49e82-120">The data factory name.</span></span>

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

### <span data-ttu-id="49e82-121">-Force</span><span class="sxs-lookup"><span data-stu-id="49e82-121">-Force</span></span>
<span data-ttu-id="49e82-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="49e82-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="49e82-123">-Name</span><span class="sxs-lookup"><span data-stu-id="49e82-123">-Name</span></span>
<span data-ttu-id="49e82-124">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="49e82-124">The trigger name.</span></span>

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

### <span data-ttu-id="49e82-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49e82-125">-ResourceGroupName</span></span>
<span data-ttu-id="49e82-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="49e82-126">The resource group name.</span></span>

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

### <span data-ttu-id="49e82-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49e82-127">-ResourceId</span></span>
<span data-ttu-id="49e82-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="49e82-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="49e82-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="49e82-129">-InputObject</span></span>
<span data-ttu-id="49e82-130">Trigger-Objekt, das gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49e82-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="49e82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49e82-131">-WhatIf</span></span>
<span data-ttu-id="49e82-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49e82-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="49e82-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e82-133">-DefaultProfile</span></span>
<span data-ttu-id="49e82-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49e82-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49e82-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e82-135">CommonParameters</span></span>
<span data-ttu-id="49e82-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e82-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e82-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e82-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e82-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49e82-138">INPUTS</span></span>

### <span data-ttu-id="49e82-139">System. String</span><span class="sxs-lookup"><span data-stu-id="49e82-139">System.String</span></span>
<span data-ttu-id="49e82-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="49e82-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="49e82-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49e82-141">OUTPUTS</span></span>

### <span data-ttu-id="49e82-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="49e82-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="49e82-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="49e82-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="49e82-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="49e82-144">NOTES</span></span>

## <span data-ttu-id="49e82-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49e82-145">RELATED LINKS</span></span>

[<span data-ttu-id="49e82-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="49e82-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="49e82-147">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="49e82-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="49e82-148">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="49e82-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="49e82-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="49e82-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
