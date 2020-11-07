---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aecbc105a87cc058567cb0ff35f0bb0e8cc84c7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665066"
---
# <span data-ttu-id="2effa-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="2effa-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="2effa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2effa-102">SYNOPSIS</span></span>
<span data-ttu-id="2effa-103">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="2effa-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2effa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2effa-104">SYNTAX</span></span>

### <span data-ttu-id="2effa-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2effa-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2effa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2effa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2effa-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2effa-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2effa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2effa-108">DESCRIPTION</span></span>
<span data-ttu-id="2effa-109">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="2effa-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="2effa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2effa-110">EXAMPLES</span></span>

### <span data-ttu-id="2effa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2effa-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="2effa-112">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2effa-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2effa-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2effa-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="2effa-114">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="2effa-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2effa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2effa-115">PARAMETERS</span></span>

### <span data-ttu-id="2effa-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2effa-116">-InputObject</span></span>
<span data-ttu-id="2effa-117">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2effa-117">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2effa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2effa-118">-Name</span></span>
<span data-ttu-id="2effa-119">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="2effa-119">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effa-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2effa-120">-PassThru</span></span>
<span data-ttu-id="2effa-121">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="2effa-121">Returns the status of the Remove operation.</span></span> <span data-ttu-id="2effa-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2effa-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2effa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2effa-123">-ResourceGroupName</span></span>
<span data-ttu-id="2effa-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2effa-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effa-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2effa-125">-ResourceId</span></span>
<span data-ttu-id="2effa-126">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="2effa-126">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2effa-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2effa-127">-Confirm</span></span>
<span data-ttu-id="2effa-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2effa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2effa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2effa-129">-WhatIf</span></span>
<span data-ttu-id="2effa-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2effa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2effa-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2effa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2effa-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2effa-132">-DefaultProfile</span></span>
<span data-ttu-id="2effa-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2effa-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2effa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2effa-134">CommonParameters</span></span>
<span data-ttu-id="2effa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2effa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2effa-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2effa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2effa-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2effa-137">INPUTS</span></span>

### <span data-ttu-id="2effa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2effa-138">System.String</span></span>
<span data-ttu-id="2effa-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2effa-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="2effa-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2effa-140">OUTPUTS</span></span>

### <span data-ttu-id="2effa-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="2effa-141">System.Object</span></span>

## <span data-ttu-id="2effa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2effa-142">NOTES</span></span>

## <span data-ttu-id="2effa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2effa-143">RELATED LINKS</span></span>

