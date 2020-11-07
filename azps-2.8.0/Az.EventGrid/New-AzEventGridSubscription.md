---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: ca404636f58eb3f4b4037ec05ab1822eb00b17ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651225"
---
# <span data-ttu-id="83718-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="83718-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="83718-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83718-102">SYNOPSIS</span></span>
<span data-ttu-id="83718-103">Erstellt ein neues Azure-Ereignis Raster-Ereignisabonnement für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83718-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="83718-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83718-104">SYNTAX</span></span>

### <span data-ttu-id="83718-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="83718-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>]
 [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [[-EndpointType] <String>] [[-SubjectBeginsWith] <String>]
 [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive] [[-IncludedEventType] <String[]>] [[-Label] <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83718-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83718-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="83718-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [[-EndpointType] <String>]
 [[-SubjectBeginsWith] <String>] [[-SubjectEndsWith] <String>] [-SubjectCaseSensitive]
 [[-IncludedEventType] <String[]>] [[-Label] <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83718-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83718-113">DESCRIPTION</span></span>
<span data-ttu-id="83718-114">Erstellen Sie ein neues Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="83718-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="83718-115">Wenn Sie ein Ereignisabonnement für das aktuell ausgewählte Azure-Abonnement erstellen möchten, geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="83718-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="83718-116">Wenn Sie ein Ereignisabonnement für eine Ressourcengruppe erstellen möchten, geben Sie neben dem Namen des Ereignisabonnements und dem Zielendpunkt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="83718-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="83718-117">Wenn Sie ein Ereignisabonnement für ein Azure-Ereignis Raster Thema erstellen möchten, geben Sie den Themen Namen ebenfalls an.</span><span class="sxs-lookup"><span data-stu-id="83718-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="83718-118">Wenn Sie ein Ereignisabonnement für eine unterstützte Azure-Ressource erstellen möchten, geben Sie die vollständige Ressourcen-ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="83718-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="83718-119">Führen Sie das Get-AzEventGridTopicType-Cmdlet aus, um die Liste der unterstützten Typen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="83718-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="83718-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83718-120">EXAMPLES</span></span>

### <span data-ttu-id="83718-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83718-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83718-122">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` zu einem Azure-Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` mit dem Zielendpunkt des webhooks https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="83718-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="83718-123">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="83718-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="83718-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="83718-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83718-125">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einer Ressourcengruppe \` MyResourceGroupName \` mit dem Zielweb-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="83718-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="83718-126">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="83718-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="83718-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="83718-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83718-128">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="83718-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="83718-129">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="83718-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="83718-130">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="83718-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="83718-131">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt https://requestb.in/19qlscd1 .</span><span class="sxs-lookup"><span data-stu-id="83718-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="83718-132">Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Betreff an, und nur Ereignisse, die diesen Filtern entsprechen, werden an den Zielendpunkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="83718-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="83718-133">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="83718-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="83718-134">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` des aktuell ausgewählten Azure-Abonnements mit dem angegebenen Ereignis-Hub als Ziel für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="83718-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="83718-135">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="83718-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="83718-136">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="83718-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="83718-137">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einem EventHub-Namespace mit dem angegebenen webhook https://requestb.in/19qlscd1 -Zielendpunkt.</span><span class="sxs-lookup"><span data-stu-id="83718-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint https://requestb.in/19qlscd1.</span></span> <span data-ttu-id="83718-138">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="83718-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="83718-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="83718-139">PARAMETERS</span></span>

### <span data-ttu-id="83718-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="83718-140">-AdvancedFilter</span></span>
<span data-ttu-id="83718-141">Erweiterter Filter, der ein Array mit mehreren Hashtable-Werten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83718-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="83718-142">Jeder Hashtable-Wert verfügt über die folgenden Schlüssel – Wert Informationen: Operation, Schlüssel und Wert oder Werte.</span><span class="sxs-lookup"><span data-stu-id="83718-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="83718-143">Der Operator kann einen der folgenden Werte aufweisen: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="83718-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="83718-144">Key stellt die Payload-Eigenschaft dar, in der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="83718-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="83718-145">Schließlich Stellenwert oder Werte den Wert oder die Gruppe von Werten dar, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83718-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="83718-146">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="83718-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="83718-147">Als Beispiel für die erweiterten Filterparameter: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), wobei $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. key1"; Values = @ (1; 2)} und $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "Betreff"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="83718-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83718-148">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="83718-148">-DeadLetterEndpoint</span></span>
<span data-ttu-id="83718-149">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83718-149">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="83718-150">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="83718-150">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="83718-151">Beispiel:/Subscriptions/[Abonnement-Nr]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/Containers/[Containername].</span><span class="sxs-lookup"><span data-stu-id="83718-151">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83718-152">-DefaultProfile</span></span>
<span data-ttu-id="83718-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="83718-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83718-154">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="83718-154">-DomainInputObject</span></span>
<span data-ttu-id="83718-155">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="83718-155">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-156">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="83718-156">-DomainName</span></span>
<span data-ttu-id="83718-157">Der Name der Ereignis Raster Domäne, in der das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83718-157">The name of the Event Grid domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-158">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="83718-158">-DomainTopicInputObject</span></span>
<span data-ttu-id="83718-159">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="83718-159">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-160">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="83718-160">-DomainTopicName</span></span>
<span data-ttu-id="83718-161">Der Name des Domänen Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83718-161">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-162">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="83718-162">-Endpoint</span></span>
<span data-ttu-id="83718-163">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="83718-163">Event subscription destination endpoint.</span></span>
<span data-ttu-id="83718-164">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID einer EventHub, Speicherwarteschlange, hybridconnection oder servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="83718-164">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="83718-165">Die Ressourcen-ID für eine hybridverbindung hat beispielsweise die folgende Form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Relay/Namespaces/[Namespacename]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="83718-165">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="83718-166">Es wird davon ausgegangen, dass der Zielendpunkt erstellt und für die Verwendung verfügbar ist, bevor Sie alle Ereignis Raster-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="83718-166">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-167">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="83718-167">-EndpointType</span></span>
<span data-ttu-id="83718-168">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="83718-168">Endpoint Type.</span></span>
<span data-ttu-id="83718-169">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="83718-169">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="83718-170">Der Standardwert ist webhook.</span><span class="sxs-lookup"><span data-stu-id="83718-170">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-171">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="83718-171">-EventSubscriptionName</span></span>
<span data-ttu-id="83718-172">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="83718-172">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-173">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="83718-173">-EventTtl</span></span>
<span data-ttu-id="83718-174">Die Zeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="83718-174">The time in minutes for the event delivery.</span></span> <span data-ttu-id="83718-175">Dieser Wert muss zwischen 1 und 1440 sein.</span><span class="sxs-lookup"><span data-stu-id="83718-175">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-176">-Wert des Felds</span><span class="sxs-lookup"><span data-stu-id="83718-176">-ExpirationDate</span></span>
<span data-ttu-id="83718-177">Bestimmt das Ablaufdatum für das Ereignisabonnement, nach dem das Ereignisabonnement in den Ruhestand geht.</span><span class="sxs-lookup"><span data-stu-id="83718-177">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83718-178">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="83718-178">-IncludedEventType</span></span>
<span data-ttu-id="83718-179">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="83718-179">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-180">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83718-180">-InputObject</span></span>
<span data-ttu-id="83718-181">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="83718-181">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="83718-182">-Label</span><span class="sxs-lookup"><span data-stu-id="83718-182">-Label</span></span>
<span data-ttu-id="83718-183">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="83718-183">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-184">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="83718-184">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="83718-185">Die maximale Anzahl von versuchen, das Ereignis zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="83718-185">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="83718-186">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="83718-186">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-187">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83718-187">-ResourceGroupName</span></span>
<span data-ttu-id="83718-188">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="83718-188">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-189">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83718-189">-ResourceId</span></span>
<span data-ttu-id="83718-190">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83718-190">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="83718-191">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="83718-191">-SubjectBeginsWith</span></span>
<span data-ttu-id="83718-192">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="83718-192">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="83718-193">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="83718-193">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-194">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="83718-194">-SubjectCaseSensitive</span></span>
<span data-ttu-id="83718-195">Filter, der angibt, dass das Feld Betreff in einer Groß-/Kleinschreibung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83718-195">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="83718-196">Wenn keine Angabe erfolgt, wird der Betreff in einem Fall unempfindlich verglichen.</span><span class="sxs-lookup"><span data-stu-id="83718-196">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="83718-197">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="83718-197">-SubjectEndsWith</span></span>
<span data-ttu-id="83718-198">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="83718-198">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="83718-199">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="83718-199">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83718-200">-Topicname</span><span class="sxs-lookup"><span data-stu-id="83718-200">-TopicName</span></span>
<span data-ttu-id="83718-201">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83718-201">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="83718-202">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83718-202">-Confirm</span></span>
<span data-ttu-id="83718-203">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83718-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83718-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83718-204">-WhatIf</span></span>
<span data-ttu-id="83718-205">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83718-205">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83718-206">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83718-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83718-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83718-207">CommonParameters</span></span>
<span data-ttu-id="83718-208">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83718-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83718-209">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83718-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83718-210">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83718-210">INPUTS</span></span>

### <span data-ttu-id="83718-211">System. String</span><span class="sxs-lookup"><span data-stu-id="83718-211">System.String</span></span>

### <span data-ttu-id="83718-212">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="83718-212">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="83718-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="83718-213">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="83718-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="83718-214">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="83718-215">System. String []</span><span class="sxs-lookup"><span data-stu-id="83718-215">System.String[]</span></span>

### <span data-ttu-id="83718-216">System. Int32</span><span class="sxs-lookup"><span data-stu-id="83718-216">System.Int32</span></span>

## <span data-ttu-id="83718-217">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83718-217">OUTPUTS</span></span>

### <span data-ttu-id="83718-218">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="83718-218">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="83718-219">Notizen</span><span class="sxs-lookup"><span data-stu-id="83718-219">NOTES</span></span>

## <span data-ttu-id="83718-220">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83718-220">RELATED LINKS</span></span>
