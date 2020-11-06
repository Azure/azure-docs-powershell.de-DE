---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: aa9ef35ec0571628eb209163e91c9415706b57a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482958"
---
# <span data-ttu-id="63082-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="63082-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="63082-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63082-102">SYNOPSIS</span></span>
<span data-ttu-id="63082-103">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="63082-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63082-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63082-104">SYNTAX</span></span>

### <span data-ttu-id="63082-105">TopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63082-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63082-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="63082-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63082-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63082-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63082-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63082-108">DESCRIPTION</span></span>
<span data-ttu-id="63082-109">Entfernt ein Azure-Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="63082-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="63082-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63082-110">EXAMPLES</span></span>

### <span data-ttu-id="63082-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63082-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="63082-112">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="63082-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="63082-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="63082-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="63082-114">Entfernt das Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcen \` Gruppe \` MyResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="63082-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="63082-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="63082-115">PARAMETERS</span></span>

### <span data-ttu-id="63082-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63082-116">-DefaultProfile</span></span>
<span data-ttu-id="63082-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63082-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63082-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="63082-118">-InputObject</span></span>
<span data-ttu-id="63082-119">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63082-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63082-120">-Name</span><span class="sxs-lookup"><span data-stu-id="63082-120">-Name</span></span>
<span data-ttu-id="63082-121">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="63082-121">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63082-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63082-122">-PassThru</span></span>
<span data-ttu-id="63082-123">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="63082-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="63082-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="63082-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="63082-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63082-125">-ResourceGroupName</span></span>
<span data-ttu-id="63082-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63082-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63082-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="63082-127">-ResourceId</span></span>
<span data-ttu-id="63082-128">EventGrid Topic.</span><span class="sxs-lookup"><span data-stu-id="63082-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63082-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63082-129">-Confirm</span></span>
<span data-ttu-id="63082-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63082-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63082-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63082-131">-WhatIf</span></span>
<span data-ttu-id="63082-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63082-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63082-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63082-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63082-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63082-134">CommonParameters</span></span>
<span data-ttu-id="63082-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63082-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63082-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63082-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63082-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63082-137">INPUTS</span></span>

### <span data-ttu-id="63082-138">System. String</span><span class="sxs-lookup"><span data-stu-id="63082-138">System.String</span></span>
<span data-ttu-id="63082-139">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="63082-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="63082-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63082-140">OUTPUTS</span></span>

### <span data-ttu-id="63082-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="63082-141">System.Object</span></span>

## <span data-ttu-id="63082-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="63082-142">NOTES</span></span>

## <span data-ttu-id="63082-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63082-143">RELATED LINKS</span></span>

