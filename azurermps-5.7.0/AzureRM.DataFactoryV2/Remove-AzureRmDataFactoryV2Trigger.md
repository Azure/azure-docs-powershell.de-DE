---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 82af1131e2730cf1f78c0c04ff8540e2ef371d2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476810"
---
# <span data-ttu-id="2943f-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2943f-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="2943f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2943f-102">SYNOPSIS</span></span>
<span data-ttu-id="2943f-103">Entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2943f-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2943f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2943f-104">SYNTAX</span></span>

### <span data-ttu-id="2943f-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2943f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2943f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2943f-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2943f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2943f-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2943f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2943f-108">DESCRIPTION</span></span>
<span data-ttu-id="2943f-109">Das Cmdlet **Remove-AzureRmDataFactoryV2Trigger** entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2943f-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="2943f-110">Wenn der Parameter _Force_ angegeben wird, wird das Cmdlet vor dem Entfernen des Triggers nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2943f-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="2943f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2943f-111">EXAMPLES</span></span>

### <span data-ttu-id="2943f-112">Beispiel 1: Entfernen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="2943f-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="2943f-113">Entfernen Sie einen Trigger mit dem Namen "ScheduledTrigger" aus der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="2943f-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="2943f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2943f-114">PARAMETERS</span></span>

### <span data-ttu-id="2943f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2943f-115">-DataFactoryName</span></span>
<span data-ttu-id="2943f-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="2943f-116">The data factory name.</span></span>

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

### <span data-ttu-id="2943f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2943f-117">-DefaultProfile</span></span>
<span data-ttu-id="2943f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2943f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2943f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2943f-119">-Force</span></span>
<span data-ttu-id="2943f-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="2943f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2943f-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2943f-121">-InputObject</span></span>
<span data-ttu-id="2943f-122">Das zu entfernende Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2943f-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="2943f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2943f-123">-Name</span></span>
<span data-ttu-id="2943f-124">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="2943f-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2943f-125">-ResourceGroupName</span></span>
<span data-ttu-id="2943f-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2943f-126">The resource group name.</span></span>

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

### <span data-ttu-id="2943f-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2943f-127">-ResourceId</span></span>
<span data-ttu-id="2943f-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2943f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2943f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2943f-129">-Confirm</span></span>
<span data-ttu-id="2943f-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2943f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2943f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2943f-131">-WhatIf</span></span>
<span data-ttu-id="2943f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2943f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2943f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2943f-133">CommonParameters</span></span>
<span data-ttu-id="2943f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2943f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2943f-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2943f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2943f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2943f-136">INPUTS</span></span>

### <span data-ttu-id="2943f-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="2943f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="2943f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2943f-138">System.String</span></span>

## <span data-ttu-id="2943f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2943f-139">OUTPUTS</span></span>

### <span data-ttu-id="2943f-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="2943f-140">System.Object</span></span>

## <span data-ttu-id="2943f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2943f-141">NOTES</span></span>

## <span data-ttu-id="2943f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2943f-142">RELATED LINKS</span></span>

[<span data-ttu-id="2943f-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2943f-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2943f-144">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2943f-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2943f-145">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2943f-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2943f-146">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2943f-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

