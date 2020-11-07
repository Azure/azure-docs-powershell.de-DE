---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: f61f411f3d4f23ddfd35e2b5dcbfea07b9b85cb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661077"
---
# <span data-ttu-id="39f52-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="39f52-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="39f52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39f52-102">SYNOPSIS</span></span>
<span data-ttu-id="39f52-103">Erstellt ein neues Azure-Ereignis Raster-Ereignisabonnement für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39f52-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="39f52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39f52-104">SYNTAX</span></span>

### <span data-ttu-id="39f52-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="39f52-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f52-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f52-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f52-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f52-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f52-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="39f52-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39f52-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39f52-109">DESCRIPTION</span></span>
<span data-ttu-id="39f52-110">Erstellen Sie ein neues Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39f52-110">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="39f52-111">Wenn Sie ein Ereignisabonnement für das aktuell ausgewählte Azure-Abonnement erstellen möchten, geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="39f52-111">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="39f52-112">Wenn Sie ein Ereignisabonnement für eine Ressourcengruppe erstellen möchten, geben Sie neben dem Namen des Ereignisabonnements und dem Zielendpunkt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="39f52-112">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="39f52-113">Wenn Sie ein Ereignisabonnement für ein Azure-Ereignis Raster Thema erstellen möchten, geben Sie den Themen Namen ebenfalls an.</span><span class="sxs-lookup"><span data-stu-id="39f52-113">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="39f52-114">Wenn Sie ein Ereignisabonnement für eine unterstützte Azure-Ressource erstellen möchten, geben Sie die vollständige Ressourcen-ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="39f52-114">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="39f52-115">Führen Sie das Get-AzEventGridTopicType-Cmdlet aus, um die Liste der unterstützten Typen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="39f52-115">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="39f52-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39f52-116">EXAMPLES</span></span>

### <span data-ttu-id="39f52-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="39f52-117">Example 1</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="39f52-118">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` zu einem Azure-Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` mit dem Zielendpunkt des webhooks https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="39f52-118">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="39f52-119">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="39f52-119">This event subscription uses default filters.</span></span>

### <span data-ttu-id="39f52-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="39f52-120">Example 2</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="39f52-121">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einer Ressourcengruppe \` MyResourceGroupName \` mit dem Zielweb-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="39f52-121">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="39f52-122">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="39f52-122">This event subscription uses default filters.</span></span>

### <span data-ttu-id="39f52-123">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="39f52-123">Example 3</span></span>
```
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="39f52-124">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="39f52-124">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="39f52-125">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="39f52-125">This event subscription uses default filters.</span></span>

### <span data-ttu-id="39f52-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="39f52-126">Example 4</span></span>
```
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="39f52-127">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="39f52-127">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="39f52-128">Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Betreff an, und nur Ereignisse, die diesen Filtern entsprechen, werden an den Zielendpunkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="39f52-128">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="39f52-129">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="39f52-129">Example 5</span></span>
```
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="39f52-130">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` des aktuell ausgewählten Azure-Abonnements mit dem angegebenen Ereignis-Hub als Ziel für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="39f52-130">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="39f52-131">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="39f52-131">This event subscription uses default filters.</span></span>

### <span data-ttu-id="39f52-132">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="39f52-132">Example 6</span></span>
```
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="39f52-133">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einem EventHub-Namespace mit dem angegebenen webhhok https://requestb.in/19qlscd1 -Zielendpunkt.</span><span class="sxs-lookup"><span data-stu-id="39f52-133">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhhok destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="39f52-134">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="39f52-134">This event subscription uses default filters.</span></span>

## <span data-ttu-id="39f52-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="39f52-135">PARAMETERS</span></span>

### <span data-ttu-id="39f52-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="39f52-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="39f52-137">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39f52-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="39f52-138">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="39f52-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="39f52-139">Beispiel:/Subscriptions/[Abonnement-Nr]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/Containers/[Containername].</span><span class="sxs-lookup"><span data-stu-id="39f52-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f52-140">-DefaultProfile</span></span>
<span data-ttu-id="39f52-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="39f52-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39f52-142">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="39f52-142">-Endpoint</span></span>
<span data-ttu-id="39f52-143">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="39f52-143">Event subscription destination endpoint.</span></span>
<span data-ttu-id="39f52-144">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID eines EventHub, einer Speicherwarteschlange oder eines hybridconnection handeln.</span><span class="sxs-lookup"><span data-stu-id="39f52-144">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="39f52-145">Die Ressourcen-ID für eine hybridverbindung hat beispielsweise die folgende Form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Relay/Namespaces/[Namespacename]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="39f52-145">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="39f52-146">Es wird davon ausgegangen, dass der Zielendpunkt erstellt und für die Verwendung verfügbar ist, bevor Sie alle Ereignis Raster-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="39f52-146">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-147">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="39f52-147">-EndpointType</span></span>
<span data-ttu-id="39f52-148">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="39f52-148">Endpoint Type.</span></span>
<span data-ttu-id="39f52-149">Dies kann webhook, eventhub, storagequeue oder hybridconnection sein.</span><span class="sxs-lookup"><span data-stu-id="39f52-149">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="39f52-150">Der Standardwert ist webhook.</span><span class="sxs-lookup"><span data-stu-id="39f52-150">Default value is webhook.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-151">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="39f52-151">-EventSubscriptionName</span></span>
<span data-ttu-id="39f52-152">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="39f52-152">The name of the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-153">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="39f52-153">-EventTtl</span></span>
<span data-ttu-id="39f52-154">Die Zeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="39f52-154">The time in minutes for the event delivery.</span></span> <span data-ttu-id="39f52-155">Dieser Wert muss zwischen 1 und 1440 sein.</span><span class="sxs-lookup"><span data-stu-id="39f52-155">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-156">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="39f52-156">-IncludedEventType</span></span>
<span data-ttu-id="39f52-157">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="39f52-157">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-158">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="39f52-158">-InputObject</span></span>
<span data-ttu-id="39f52-159">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="39f52-159">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-160">-Label</span><span class="sxs-lookup"><span data-stu-id="39f52-160">-Label</span></span>
<span data-ttu-id="39f52-161">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="39f52-161">Labels for the event subscription</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-162">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="39f52-162">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="39f52-163">Die maximale Anzahl von versuchen, das Ereignis zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="39f52-163">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="39f52-164">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="39f52-164">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f52-165">-ResourceGroupName</span></span>
<span data-ttu-id="39f52-166">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="39f52-166">The resource group of the topic.</span></span>

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

### <span data-ttu-id="39f52-167">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="39f52-167">-ResourceId</span></span>
<span data-ttu-id="39f52-168">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39f52-168">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="39f52-169">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="39f52-169">-SubjectBeginsWith</span></span>
<span data-ttu-id="39f52-170">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="39f52-170">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="39f52-171">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="39f52-171">If not specified, events with all subject prefixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-172">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="39f52-172">-SubjectCaseSensitive</span></span>
<span data-ttu-id="39f52-173">Filter, der angibt, dass das Feld Betreff in einer Groß-/Kleinschreibung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39f52-173">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="39f52-174">Wenn keine Angabe erfolgt, wird der Betreff in einem Fall unempfindlich verglichen.</span><span class="sxs-lookup"><span data-stu-id="39f52-174">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="39f52-175">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="39f52-175">-SubjectEndsWith</span></span>
<span data-ttu-id="39f52-176">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="39f52-176">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="39f52-177">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="39f52-177">If not specified, events with all subject suffixes will be included.</span></span>

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
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f52-178">-Topicname</span><span class="sxs-lookup"><span data-stu-id="39f52-178">-TopicName</span></span>
<span data-ttu-id="39f52-179">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39f52-179">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="39f52-180">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39f52-180">-Confirm</span></span>
<span data-ttu-id="39f52-181">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39f52-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39f52-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f52-182">-WhatIf</span></span>
<span data-ttu-id="39f52-183">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39f52-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39f52-184">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39f52-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39f52-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f52-185">CommonParameters</span></span>
<span data-ttu-id="39f52-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f52-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f52-187">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f52-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f52-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39f52-188">INPUTS</span></span>

### <span data-ttu-id="39f52-189">System. String</span><span class="sxs-lookup"><span data-stu-id="39f52-189">System.String</span></span>

### <span data-ttu-id="39f52-190">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="39f52-190">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="39f52-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="39f52-191">System.String[]</span></span>

## <span data-ttu-id="39f52-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39f52-192">OUTPUTS</span></span>

### <span data-ttu-id="39f52-193">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="39f52-193">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="39f52-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="39f52-194">NOTES</span></span>

## <span data-ttu-id="39f52-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39f52-195">RELATED LINKS</span></span>
