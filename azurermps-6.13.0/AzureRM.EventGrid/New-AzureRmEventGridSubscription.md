---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridSubscription.md
ms.openlocfilehash: bb21a7d69d6e2afa810b9df1bb2fa676b6568782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497486"
---
# <span data-ttu-id="ab738-101">New-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ab738-101">New-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="ab738-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab738-102">SYNOPSIS</span></span>
<span data-ttu-id="ab738-103">Erstellt ein neues Azure-Ereignis Raster-Ereignisabonnement für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab738-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab738-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab738-104">SYNTAX</span></span>

### <span data-ttu-id="ab738-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab738-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab738-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab738-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab738-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab738-107">EventSubscriptionInputObjectSet</span></span>
```
New-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab738-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab738-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab738-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab738-109">DESCRIPTION</span></span>
<span data-ttu-id="ab738-110">Erstellen Sie ein neues Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ab738-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="ab738-111">Wenn Sie ein Ereignisabonnement für das aktuell ausgewählte Azure-Abonnement erstellen möchten, geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="ab738-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="ab738-112">Wenn Sie ein Ereignisabonnement für eine Ressourcengruppe erstellen möchten, geben Sie neben dem Namen des Ereignisabonnements und dem Zielendpunkt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ab738-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="ab738-113">Wenn Sie ein Ereignisabonnement für ein Azure-Ereignis Raster Thema erstellen möchten, geben Sie den Themen Namen ebenfalls an.</span><span class="sxs-lookup"><span data-stu-id="ab738-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="ab738-114">Wenn Sie ein Ereignisabonnement für eine unterstützte Azure-Ressource erstellen möchten, geben Sie die vollständige Ressourcen-ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ab738-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="ab738-115">Führen Sie das Get-AzureRmEventGridTopicType-Cmdlet aus, um die Liste der unterstützten Typen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ab738-115">To view the list of supported types, run the Get-AzureRmEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="ab738-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab738-116">EXAMPLES</span></span>

### <span data-ttu-id="ab738-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab738-117">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ab738-118">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` zu einem Azure-Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` mit dem Zielendpunkt des webhooks https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="ab738-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="ab738-119">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="ab738-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ab738-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ab738-120">Example 2</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ab738-121">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einer Ressourcengruppe \` MyResourceGroupName \` mit dem Zielweb-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="ab738-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="ab738-122">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="ab738-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ab738-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ab738-123">Example 3</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ab738-124">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="ab738-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="ab738-125">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="ab738-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ab738-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ab738-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzureRmEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="ab738-127">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="ab738-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="ab738-128">Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Betreff an, und nur Ereignisse, die diesen Filtern entsprechen, werden an den Zielendpunkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ab738-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="ab738-129">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ab738-129">Example 5</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="ab738-130">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` des aktuell ausgewählten Azure-Abonnements mit dem angegebenen Ereignis-Hub als Ziel für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="ab738-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="ab738-131">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="ab738-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="ab738-132">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="ab738-132">Example 6</span></span>
```
PS C:\> New-AzureRmEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ab738-133">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einem EventHub-Namespace mit dem angegebenen webhhok https://requestb.in/19qlscd1 -Zielendpunkt.</span><span class="sxs-lookup"><span data-stu-id="ab738-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="ab738-134">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="ab738-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="ab738-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab738-135">PARAMETERS</span></span>

### <span data-ttu-id="ab738-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab738-136">-DefaultProfile</span></span>
<span data-ttu-id="ab738-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ab738-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab738-138">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="ab738-138">-Endpoint</span></span>
<span data-ttu-id="ab738-139">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="ab738-139">Event subscription destination endpoint.</span></span>
<span data-ttu-id="ab738-140">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID eines EventHub.</span><span class="sxs-lookup"><span data-stu-id="ab738-140">This can be a webhook URL or the Azure resource ID of an EventHub.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-141">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ab738-141">-EndpointType</span></span>
<span data-ttu-id="ab738-142">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="ab738-142">Endpoint Type.</span></span>
<span data-ttu-id="ab738-143">Dies kann webhook oder eventhub sein.</span><span class="sxs-lookup"><span data-stu-id="ab738-143">This can be webhook or eventhub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:
Accepted values: webhook, eventhub

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-144">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ab738-144">-EventSubscriptionName</span></span>
<span data-ttu-id="ab738-145">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="ab738-145">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
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

### <span data-ttu-id="ab738-146">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="ab738-146">-IncludedEventType</span></span>
<span data-ttu-id="ab738-147">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="ab738-147">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-148">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab738-148">-InputObject</span></span>
<span data-ttu-id="ab738-149">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ab738-149">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ab738-150">-Label</span><span class="sxs-lookup"><span data-stu-id="ab738-150">-Label</span></span>
<span data-ttu-id="ab738-151">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="ab738-151">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab738-152">-ResourceGroupName</span></span>
<span data-ttu-id="ab738-153">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="ab738-153">The resource group of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-154">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ab738-154">-ResourceId</span></span>
<span data-ttu-id="ab738-155">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab738-155">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="ab738-156">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="ab738-156">-SubjectBeginsWith</span></span>
<span data-ttu-id="ab738-157">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ab738-157">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="ab738-158">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ab738-158">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-159">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="ab738-159">-SubjectCaseSensitive</span></span>
<span data-ttu-id="ab738-160">Filter, der angibt, dass das Feld Betreff in einer Groß-/Kleinschreibung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab738-160">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="ab738-161">Wenn keine Angabe erfolgt, wird der Betreff in einem Fall unempfindlich verglichen.</span><span class="sxs-lookup"><span data-stu-id="ab738-161">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="ab738-162">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="ab738-162">-SubjectEndsWith</span></span>
<span data-ttu-id="ab738-163">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ab738-163">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="ab738-164">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ab738-164">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-165">-Topicname</span><span class="sxs-lookup"><span data-stu-id="ab738-165">-TopicName</span></span>
<span data-ttu-id="ab738-166">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab738-166">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab738-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab738-167">-Confirm</span></span>
<span data-ttu-id="ab738-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab738-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab738-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab738-169">-WhatIf</span></span>
<span data-ttu-id="ab738-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab738-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab738-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab738-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab738-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab738-172">CommonParameters</span></span>
<span data-ttu-id="ab738-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab738-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab738-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab738-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab738-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab738-175">INPUTS</span></span>

### <span data-ttu-id="ab738-176">System. String</span><span class="sxs-lookup"><span data-stu-id="ab738-176">System.String</span></span>

### <span data-ttu-id="ab738-177">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ab738-177">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="ab738-178">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab738-178">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ab738-179">System. String []</span><span class="sxs-lookup"><span data-stu-id="ab738-179">System.String[]</span></span>

## <span data-ttu-id="ab738-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab738-180">OUTPUTS</span></span>

### <span data-ttu-id="ab738-181">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ab738-181">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ab738-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab738-182">NOTES</span></span>

## <span data-ttu-id="ab738-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab738-183">RELATED LINKS</span></span>
