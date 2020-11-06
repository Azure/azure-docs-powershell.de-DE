---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505049"
---
# <span data-ttu-id="ef5b0-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ef5b0-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="ef5b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5b0-103">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef5b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef5b0-104">SYNTAX</span></span>

### <span data-ttu-id="ef5b0-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef5b0-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5b0-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5b0-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5b0-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef5b0-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef5b0-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef5b0-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef5b0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef5b0-109">DESCRIPTION</span></span>
<span data-ttu-id="ef5b0-110">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="ef5b0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef5b0-111">EXAMPLES</span></span>

### <span data-ttu-id="ef5b0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ef5b0-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ef5b0-113">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Azure-Ereignis Raster Thema \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ef5b0-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ef5b0-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ef5b0-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ef5b0-115">Entfernt das Ereignisabonnement \` EventSubscription1 \` in eine Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ef5b0-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ef5b0-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ef5b0-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ef5b0-117">Entfernt das Ereignisabonnement \` EventSubscription1 \` in das standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="ef5b0-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ef5b0-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ef5b0-119">Entfernt das Ereignisabonnement \` \` -EventSubscription1 in einen Event Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="ef5b0-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ef5b0-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ef5b0-121">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="ef5b0-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef5b0-122">PARAMETERS</span></span>

### <span data-ttu-id="ef5b0-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ef5b0-123">-EventSubscriptionName</span></span>
<span data-ttu-id="ef5b0-124">Der Name des Ereignisabonnements, das entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-124">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b0-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ef5b0-125">-InputObject</span></span>
<span data-ttu-id="ef5b0-126">EventGrid-EventSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef5b0-127">-PassThru</span></span>
<span data-ttu-id="ef5b0-128">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ef5b0-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef5b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef5b0-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b0-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ef5b0-132">-ResourceId</span></span>
<span data-ttu-id="ef5b0-133">Der Bezeichner der Ressource, deren Ereignisabonnement entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b0-134">-Topicname</span><span class="sxs-lookup"><span data-stu-id="ef5b0-134">-TopicName</span></span>
<span data-ttu-id="ef5b0-135">Themen Name des Ereignis Rasters</span><span class="sxs-lookup"><span data-stu-id="ef5b0-135">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef5b0-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef5b0-136">-Confirm</span></span>
<span data-ttu-id="ef5b0-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef5b0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5b0-138">-WhatIf</span></span>
<span data-ttu-id="ef5b0-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef5b0-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef5b0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5b0-141">-DefaultProfile</span></span>
<span data-ttu-id="ef5b0-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef5b0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5b0-143">CommonParameters</span></span>
<span data-ttu-id="ef5b0-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef5b0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5b0-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef5b0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5b0-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef5b0-146">INPUTS</span></span>

### <span data-ttu-id="ef5b0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef5b0-147">System.String</span></span>
<span data-ttu-id="ef5b0-148">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ef5b0-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ef5b0-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef5b0-149">OUTPUTS</span></span>

### <span data-ttu-id="ef5b0-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="ef5b0-150">System.Object</span></span>

## <span data-ttu-id="ef5b0-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef5b0-151">NOTES</span></span>

## <span data-ttu-id="ef5b0-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef5b0-152">RELATED LINKS</span></span>

