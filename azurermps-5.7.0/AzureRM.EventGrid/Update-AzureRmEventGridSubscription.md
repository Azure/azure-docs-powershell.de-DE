---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/update-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Update-AzureRmEventGridSubscription.md
ms.openlocfilehash: 7a6f7833a2b123a4f0235d331952b1403316df37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482957"
---
# <span data-ttu-id="0e5fd-101">Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e5fd-101">Update-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="0e5fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5fd-103">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-103">Update the properties of an Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e5fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e5fd-104">SYNTAX</span></span>

### <span data-ttu-id="0e5fd-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e5fd-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5fd-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e5fd-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5fd-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e5fd-107">EventSubscriptionInputObjectSet</span></span>
```
Update-AzureRmEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5fd-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e5fd-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e5fd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e5fd-109">DESCRIPTION</span></span>
<span data-ttu-id="0e5fd-110">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="0e5fd-111">Dies kann verwendet werden, um den Filter, das Ziel oder die Bezeichnungen eines vorhandenen Ereignisabonnements zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="0e5fd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e5fd-112">EXAMPLES</span></span>

### <span data-ttu-id="0e5fd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e5fd-113">Example 1</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="0e5fd-114">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="0e5fd-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="0e5fd-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e5fd-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzureRmEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="0e5fd-116">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="0e5fd-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="0e5fd-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0e5fd-117">Example 3</span></span>
```
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="0e5fd-118">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für den EventHub-Namespace ContosoNamespace mit dem neuen Endpunkt als \` https://requestb.in/1kxxoui1\ "und dem neuen SubjectEndsWith-Filter als \` JPG\`</span><span class="sxs-lookup"><span data-stu-id="0e5fd-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="0e5fd-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0e5fd-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzureRmEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="0e5fd-120">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für die Ressourcengruppe \` MyResourceGroupName \` mit dem neuen Etiketten $Labels.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="0e5fd-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e5fd-121">PARAMETERS</span></span>

### <span data-ttu-id="0e5fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5fd-122">-DefaultProfile</span></span>
<span data-ttu-id="0e5fd-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e5fd-124">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="0e5fd-124">-Endpoint</span></span>
<span data-ttu-id="0e5fd-125">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="0e5fd-125">Event subscription destination endpoint.</span></span>
<span data-ttu-id="0e5fd-126">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID eines EventHub.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-126">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0e5fd-127">-EndpointType</span></span>
<span data-ttu-id="0e5fd-128">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-128">Endpoint Type.</span></span>
<span data-ttu-id="0e5fd-129">Dies kann webhook oder eventhub sein.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-129">This can be webhook or eventhub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: webhook, eventhub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-130">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="0e5fd-130">-EventSubscriptionName</span></span>
<span data-ttu-id="0e5fd-131">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="0e5fd-131">The name of the event subscription</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-132">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="0e5fd-132">-IncludedEventType</span></span>
<span data-ttu-id="0e5fd-133">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-133">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e5fd-134">-InputObject</span></span>
<span data-ttu-id="0e5fd-135">EventGridSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-135">EventGridSubscription object.</span></span>

```yaml
Type: PSEventSubscription
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-136">-Label</span><span class="sxs-lookup"><span data-stu-id="0e5fd-136">-Label</span></span>
<span data-ttu-id="0e5fd-137">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="0e5fd-137">Labels for the event subscription</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5fd-138">-ResourceGroupName</span></span>
<span data-ttu-id="0e5fd-139">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-139">The resource group of the topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e5fd-140">-ResourceId</span></span>
<span data-ttu-id="0e5fd-141">Der Bezeichner der Ressource, in der das Ereignisabonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-141">The identifier of the resource to which the event subscription was created.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-142">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0e5fd-142">-SubjectBeginsWith</span></span>
<span data-ttu-id="0e5fd-143">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-143">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="0e5fd-144">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-144">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-145">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="0e5fd-145">-SubjectEndsWith</span></span>
<span data-ttu-id="0e5fd-146">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-146">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="0e5fd-147">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-147">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-148">-Topicname</span><span class="sxs-lookup"><span data-stu-id="0e5fd-148">-TopicName</span></span>
<span data-ttu-id="0e5fd-149">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-149">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5fd-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e5fd-150">-Confirm</span></span>
<span data-ttu-id="0e5fd-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e5fd-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e5fd-152">-WhatIf</span></span>
<span data-ttu-id="0e5fd-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e5fd-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e5fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5fd-155">CommonParameters</span></span>
<span data-ttu-id="0e5fd-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5fd-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e5fd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5fd-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e5fd-158">INPUTS</span></span>

### <span data-ttu-id="0e5fd-159">System. String</span><span class="sxs-lookup"><span data-stu-id="0e5fd-159">System.String</span></span>
<span data-ttu-id="0e5fd-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. String []</span><span class="sxs-lookup"><span data-stu-id="0e5fd-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.String[]</span></span>

## <span data-ttu-id="0e5fd-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e5fd-161">OUTPUTS</span></span>

### <span data-ttu-id="0e5fd-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="0e5fd-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="0e5fd-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e5fd-163">NOTES</span></span>

## <span data-ttu-id="0e5fd-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e5fd-164">RELATED LINKS</span></span>

