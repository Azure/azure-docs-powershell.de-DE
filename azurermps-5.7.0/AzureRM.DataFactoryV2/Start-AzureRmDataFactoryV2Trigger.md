---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: ed4769c26363c60aace191d439d4a450a894eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662748"
---
# <span data-ttu-id="df011-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df011-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="df011-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="df011-102">SYNOPSIS</span></span>
<span data-ttu-id="df011-103">Startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="df011-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df011-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="df011-104">SYNTAX</span></span>

### <span data-ttu-id="df011-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="df011-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df011-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df011-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df011-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df011-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df011-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df011-108">DESCRIPTION</span></span>
<span data-ttu-id="df011-109">Das Cmdlet **Start-AzureRmDataFactoryV2Trigger** startet einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="df011-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="df011-110">Wenn sich der Trigger im Zustand "stopped" befindet, startet das Cmdlet den Trigger und ruft schließlich Pipelines basierend auf seiner Definition auf.</span><span class="sxs-lookup"><span data-stu-id="df011-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="df011-111">Wenn sich der Trigger bereits im Zustand "Started" befindet, hat dieses Cmdlet keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="df011-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="df011-112">Wenn der Parameter Force angegeben wird, wird das Cmdlet vor dem Starten des Triggers nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="df011-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="df011-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df011-113">EXAMPLES</span></span>

### <span data-ttu-id="df011-114">Beispiel 1: Starten eines Triggers</span><span class="sxs-lookup"><span data-stu-id="df011-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="df011-115">Startet einen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="df011-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="df011-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="df011-116">PARAMETERS</span></span>

### <span data-ttu-id="df011-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="df011-117">-DataFactoryName</span></span>
<span data-ttu-id="df011-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="df011-118">The data factory name.</span></span>

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

### <span data-ttu-id="df011-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df011-119">-DefaultProfile</span></span>
<span data-ttu-id="df011-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="df011-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df011-121">-Force</span><span class="sxs-lookup"><span data-stu-id="df011-121">-Force</span></span>
<span data-ttu-id="df011-122">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="df011-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="df011-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df011-123">-InputObject</span></span>
<span data-ttu-id="df011-124">Trigger-Objekt, das gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="df011-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="df011-125">-Name</span><span class="sxs-lookup"><span data-stu-id="df011-125">-Name</span></span>
<span data-ttu-id="df011-126">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="df011-126">The trigger name.</span></span>

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

### <span data-ttu-id="df011-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df011-127">-ResourceGroupName</span></span>
<span data-ttu-id="df011-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="df011-128">The resource group name.</span></span>

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

### <span data-ttu-id="df011-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="df011-129">-ResourceId</span></span>
<span data-ttu-id="df011-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="df011-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="df011-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="df011-131">-Confirm</span></span>
<span data-ttu-id="df011-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df011-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df011-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df011-133">-WhatIf</span></span>
<span data-ttu-id="df011-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df011-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="df011-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df011-135">CommonParameters</span></span>
<span data-ttu-id="df011-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df011-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df011-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df011-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df011-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="df011-138">INPUTS</span></span>

### <span data-ttu-id="df011-139">System. String</span><span class="sxs-lookup"><span data-stu-id="df011-139">System.String</span></span>
<span data-ttu-id="df011-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="df011-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="df011-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="df011-141">OUTPUTS</span></span>

### <span data-ttu-id="df011-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="df011-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="df011-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="df011-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="df011-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="df011-144">NOTES</span></span>

## <span data-ttu-id="df011-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="df011-145">RELATED LINKS</span></span>

[<span data-ttu-id="df011-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df011-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df011-147">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df011-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df011-148">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df011-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="df011-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="df011-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
