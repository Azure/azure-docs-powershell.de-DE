---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458723"
---
# <span data-ttu-id="fc4a9-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fc4a9-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="fc4a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc4a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4a9-103">Erstellt ein neues Azure Event Grid Event Subscription für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="fc4a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc4a9-104">SYNTAX</span></span>

### <span data-ttu-id="fc4a9-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc4a9-105">ResourceGroupNameParameterSet (Default)</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [[-ResourceGroupName] <String>] [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-Endpoint] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-110">CustomTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-TopicName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-111">DomainEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> [-EndpointType <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-SubjectCaseSensitive] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeliverySchema <String>] [-DeadLetterEndpoint <String>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryTenantId <String>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a9-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a9-112">DomainTopicEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-ResourceGroupName] <String> [-DomainName] <String> -DomainTopicName <String> [-EndpointType <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4a9-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc4a9-113">DESCRIPTION</span></span>
<span data-ttu-id="fc4a9-114">Erstellen Sie ein neues Ereignisabonnement für ein Azure-Veranstaltungsrasterthema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="fc4a9-115">Zum Erstellen eines Ereignisabonnements für das aktuell ausgewählte Azure-Abonnement geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="fc4a9-116">Um ein Ereignisabonnement für eine Ressourcengruppe zu erstellen, geben Sie den Namen der Ressourcengruppe sowie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="fc4a9-117">Um ein Ereignisabonnement für ein Azure Event Grid-Thema zu erstellen, geben Sie auch den Themanamen an.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="fc4a9-118">Um ein Ereignisabonnement für eine unterstützte Azure-Ressource zu erstellen, geben Sie die vollständige Ressourcen-ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="fc4a9-119">Führen Sie zum Anzeigen der Liste der unterstützten Typen das cmdlet Get-AzEventGridTopicType aus.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="fc4a9-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc4a9-120">EXAMPLES</span></span>

### <span data-ttu-id="fc4a9-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc4a9-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fc4a9-122">Erstellt ein neues Ereignisabonnement \` "EventSubscription1" für ein \` Azure-Veranstaltungsrasterthema Thema1 in der Ressourcengruppe \` \` \` "MyResourceGroupName" mit dem \` Endpunkt des Webhook-Ziels. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="fc4a9-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="fc4a9-123">Für dieses Ereignisabonnement werden Standardfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="fc4a9-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fc4a9-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fc4a9-125">Erstellt ein neues Ereignisabonnement \` "EventSubscription1" für eine \` \` Ressourcengruppe "MyResourceGroupName" mit dem \` Endpunkt des Webhook-Ziels. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="fc4a9-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="fc4a9-126">Für dieses Ereignisabonnement werden Standardfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="fc4a9-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fc4a9-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fc4a9-128">Erstellt ein neues Ereignisabonnement "EventSubscription1" für das aktuell ausgewählte \` Azure-Abonnement mit dem Endpunkt des \` Webhook-Ziels. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="fc4a9-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="fc4a9-129">Für dieses Ereignisabonnement werden Standardfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="fc4a9-130">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fc4a9-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="fc4a9-131">Erstellt ein neues Ereignisabonnement "EventSubscription1" für das aktuell ausgewählte \` Azure-Abonnement mit dem Endpunkt des \` Webhook-Ziels. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="fc4a9-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="fc4a9-132">Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Themen an, und nur Ereignisse, die diesen Filtern übereinstimmen, werden an den Zielendpunkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="fc4a9-133">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="fc4a9-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="fc4a9-134">Erstellt ein neues Ereignisabonnement "EventSubscription1" für das aktuell ausgewählte Azure-Abonnement mit dem angegebenen Ereignishub \` \` als Ziel für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="fc4a9-135">Für dieses Ereignisabonnement werden Standardfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="fc4a9-136">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="fc4a9-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fc4a9-137">Erstellt ein neues Ereignisabonnement \` "EventSubscription1" für einen \` EventHub-Namespace mit dem angegebenen Endpunkt des Webhook-Ziels. `https://requestb.in/19qlscd1`</span><span class="sxs-lookup"><span data-stu-id="fc4a9-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="fc4a9-138">Für dieses Ereignisabonnement werden Standardfilter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="fc4a9-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc4a9-139">PARAMETERS</span></span>

### <span data-ttu-id="fc4a9-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="fc4a9-140">-AdvancedFilter</span></span>
<span data-ttu-id="fc4a9-141">Erweiterter Filter, der ein Array mit mehreren Hashtablewerten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="fc4a9-142">Jeder Hashtablewert enthält die folgenden Schlüssel-Wert-Informationen: "Operation", "Key" und "Value" oder "Values".</span><span class="sxs-lookup"><span data-stu-id="fc4a9-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="fc4a9-143">Der Operator kann einer der folgenden Werte sein: NumberIn, NumberNotIn, NumberLessLite, NumberGreater Nur, NumberLessLiteOrEquals, NumberGreater NurOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="fc4a9-144">Der Schlüssel stellt die Nutzlasteigenschaft dar, in der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="fc4a9-145">Schließlich stellen "Wert" oder "Werte" den Wert oder die Gruppe von Werten dar, die übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="fc4a9-146">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="fc4a9-147">Beispiel für die erweiterten Filterparameter: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), wobei $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} und $AdvFilter 2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="fc4a9-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="fc4a9-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="fc4a9-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="fc4a9-149">Die Azure Active Directory (AAD)-Anwendungs-ID oder der URI, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen eingeschlossen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="fc4a9-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="fc4a9-151">Die Azure Active Directory (AAD)-Mandanten-ID, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen eingeschlossen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="fc4a9-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="fc4a9-153">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="fc4a9-154">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="fc4a9-155">Beispiel: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="fc4a9-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="fc4a9-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4a9-156">-DefaultProfile</span></span>
<span data-ttu-id="fc4a9-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fc4a9-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc4a9-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="fc4a9-158">-DeliverySchema</span></span>
<span data-ttu-id="fc4a9-159">Das Schema, das verwendet werden soll, wenn Ereignisse an das Ziel übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="fc4a9-160">Die möglichen Werte sind: eventgridschema, CustomInputSchema oder cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="fc4a9-161">Der Standardwert ist "CustomInputSchema".</span><span class="sxs-lookup"><span data-stu-id="fc4a9-161">Default value is CustomInputSchema.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

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
Accepted values: EventGridSchema, CustomInputSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="fc4a9-162">-DomainInputObject</span></span>
<span data-ttu-id="fc4a9-163">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="fc4a9-164">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fc4a9-164">-DomainName</span></span>
<span data-ttu-id="fc4a9-165">Der Name der Ereignisrasterdomäne, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="fc4a9-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="fc4a9-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="fc4a9-167">EventGrid Domain Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="fc4a9-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="fc4a9-168">-DomainTopicName</span></span>
<span data-ttu-id="fc4a9-169">Der Name des Domänenthemas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="fc4a9-170">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="fc4a9-170">-Endpoint</span></span>
<span data-ttu-id="fc4a9-171">Endpunkt des Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="fc4a9-172">Dabei kann es sich um eine Webhook-URL oder die Azure-Ressourcen-ID eines EventHub, einer Speicherwarteschlange, Hybridverbindung oder eines Dienstbusqueues sein.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="fc4a9-173">Beispielsweise hat die Ressourcen-ID für eine Hybridverbindung das folgende Format: /subscriptions/[Azure-Abonnement-ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="fc4a9-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="fc4a9-174">Es wird erwartet, dass der Zielendpunkt erstellt und zur Verwendung zur Verfügung steht, bevor Ereignisraster-Cmdlets ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="fc4a9-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="fc4a9-175">-EndpointType</span></span>
<span data-ttu-id="fc4a9-176">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-176">Endpoint Type.</span></span>
<span data-ttu-id="fc4a9-177">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="fc4a9-178">Der Standardwert ist "Webhook".</span><span class="sxs-lookup"><span data-stu-id="fc4a9-178">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

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
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fc4a9-179">-EventSubscriptionName</span></span>
<span data-ttu-id="fc4a9-180">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="fc4a9-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="fc4a9-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="fc4a9-181">-EventTtl</span></span>
<span data-ttu-id="fc4a9-182">Die Uhrzeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="fc4a9-183">Dieser Wert muss zwischen 1 und 1440 liegen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="fc4a9-184">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="fc4a9-184">-ExpirationDate</span></span>
<span data-ttu-id="fc4a9-185">Bestimmt den Ablaufdatumszeit (DateTime) für das Ereignisabonnement, nach dem das Ereignisabonnement abläuft.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="fc4a9-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="fc4a9-186">-IncludedEventType</span></span>
<span data-ttu-id="fc4a9-187">Filter, der eine Liste der hinzuzufügenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-188">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc4a9-188">-InputObject</span></span>
<span data-ttu-id="fc4a9-189">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="fc4a9-190">-Label</span><span class="sxs-lookup"><span data-stu-id="fc4a9-190">-Label</span></span>
<span data-ttu-id="fc4a9-191">Bezeichnungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="fc4a9-191">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a9-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="fc4a9-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="fc4a9-193">Die maximale Anzahl von Versuchen, das Ereignis zu liefern.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="fc4a9-194">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="fc4a9-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="fc4a9-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="fc4a9-196">Die maximale Anzahl von Ereignissen in einem Batch.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="fc4a9-197">Dieser Wert muss zwischen 1 und 5000 liegen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="fc4a9-198">Dieser Parameter ist gültig, wenn der Endpinttyp nur ein Webhook ist.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="fc4a9-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="fc4a9-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="fc4a9-200">Die bevorzugte Batchgröße in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="fc4a9-201">Dieser Wert muss zwischen 1 und 1024 liegen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="fc4a9-202">Dieser Parameter ist gültig, wenn der Endpinttyp nur ein Webhook ist.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="fc4a9-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc4a9-203">-ResourceGroupName</span></span>
<span data-ttu-id="fc4a9-204">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="fc4a9-205">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc4a9-205">-ResourceId</span></span>
<span data-ttu-id="fc4a9-206">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="fc4a9-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="fc4a9-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="fc4a9-208">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffpräfix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="fc4a9-209">Wenn nichts angegeben wird, werden Ereignisse mit allen Betreffpräfixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="fc4a9-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="fc4a9-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="fc4a9-211">Filter, der angibt, dass das Betrefffeld unter Schreibung der Großen und Kleinschreibung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="fc4a9-212">Wenn keine Angabe ausgeführt wird, wird das Thema ohne Empfindlichkeit der Groß-/Kleinschreibung verglichen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="fc4a9-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="fc4a9-213">-SubjectEndsWith</span></span>
<span data-ttu-id="fc4a9-214">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffsuffix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="fc4a9-215">Wenn nichts angegeben wird, werden Ereignisse mit allen Subjektsuffixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="fc4a9-216">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fc4a9-216">-TopicName</span></span>
<span data-ttu-id="fc4a9-217">Der Name des Themas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="fc4a9-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc4a9-218">-Confirm</span></span>
<span data-ttu-id="fc4a9-219">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4a9-220">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc4a9-220">-WhatIf</span></span>
<span data-ttu-id="fc4a9-221">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4a9-222">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4a9-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4a9-223">CommonParameters</span></span>
<span data-ttu-id="fc4a9-224">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4a9-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4a9-225">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc4a9-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4a9-226">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc4a9-226">INPUTS</span></span>

### <span data-ttu-id="fc4a9-227">System.String</span><span class="sxs-lookup"><span data-stu-id="fc4a9-227">System.String</span></span>

### <span data-ttu-id="fc4a9-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="fc4a9-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="fc4a9-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="fc4a9-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="fc4a9-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fc4a9-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="fc4a9-231">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fc4a9-231">System.String[]</span></span>

### <span data-ttu-id="fc4a9-232">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fc4a9-232">System.Int32</span></span>

## <span data-ttu-id="fc4a9-233">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc4a9-233">OUTPUTS</span></span>

### <span data-ttu-id="fc4a9-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="fc4a9-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="fc4a9-235">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc4a9-235">NOTES</span></span>

## <span data-ttu-id="fc4a9-236">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc4a9-236">RELATED LINKS</span></span>
