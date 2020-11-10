---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridSubscription.md
ms.openlocfilehash: 44441fa364c43242a7a4454ccdf62f920cb321e5
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395321"
---
# <span data-ttu-id="51588-101">New-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="51588-101">New-AzEventGridSubscription</span></span>

## <span data-ttu-id="51588-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51588-102">SYNOPSIS</span></span>
<span data-ttu-id="51588-103">Erstellt ein neues Azure-Ereignis Raster-Ereignisabonnement für ein Thema, eine Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51588-103">Creates a new Azure Event Grid Event Subscription to a topic, Azure resource, Azure subscription or Resource Group.</span></span>

## <span data-ttu-id="51588-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51588-104">SYNTAX</span></span>

### <span data-ttu-id="51588-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="51588-105">ResourceGroupNameParameterSet (Default)</span></span>
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

### <span data-ttu-id="51588-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51588-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
New-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-Endpoint] <String>
 [-EndpointType <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-SubjectCaseSensitive]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeliverySchema <String>] [-DeadLetterEndpoint <String>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryTenantId <String>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51588-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
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

### <span data-ttu-id="51588-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
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

### <span data-ttu-id="51588-110">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-110">CustomTopicEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="51588-111">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-111">DomainEventSubscriptionParameterSet</span></span>
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

### <span data-ttu-id="51588-112">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51588-112">DomainTopicEventSubscriptionParameterSet</span></span>
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

## <span data-ttu-id="51588-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51588-113">DESCRIPTION</span></span>
<span data-ttu-id="51588-114">Erstellen Sie ein neues Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine unterstützte Azure-Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51588-114">Create a new event subscription to an Azure Event Grid topic, a supported Azure resource, an Azure subscription or Resource Group.</span></span>
<span data-ttu-id="51588-115">Wenn Sie ein Ereignisabonnement für das aktuell ausgewählte Azure-Abonnement erstellen möchten, geben Sie den Namen des Ereignisabonnements und den Zielendpunkt an.</span><span class="sxs-lookup"><span data-stu-id="51588-115">To create an event subscription to the currently selected Azure subscription, specify the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="51588-116">Wenn Sie ein Ereignisabonnement für eine Ressourcengruppe erstellen möchten, geben Sie neben dem Namen des Ereignisabonnements und dem Zielendpunkt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="51588-116">To create an event subscription to a resource group, specify the resource group name in addition to the event subscription name and the destination endpoint.</span></span>
<span data-ttu-id="51588-117">Wenn Sie ein Ereignisabonnement für ein Azure-Ereignis Raster Thema erstellen möchten, geben Sie den Themen Namen ebenfalls an.</span><span class="sxs-lookup"><span data-stu-id="51588-117">To create an event subscription to an Azure Event Grid topic, specify the topic name as well.</span></span>
<span data-ttu-id="51588-118">Wenn Sie ein Ereignisabonnement für eine unterstützte Azure-Ressource erstellen möchten, geben Sie die vollständige Ressourcen-ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="51588-118">To create an event subscription to a supported Azure resource, specify the full resource ID of the resource.</span></span> <span data-ttu-id="51588-119">Führen Sie das Get-AzEventGridTopicType-Cmdlet aus, um die Liste der unterstützten Typen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51588-119">To view the list of supported types, run the Get-AzEventGridTopicType cmdlet.</span></span>

## <span data-ttu-id="51588-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51588-120">EXAMPLES</span></span>

### <span data-ttu-id="51588-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51588-121">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51588-122">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` zu einem Azure-Ereignis Raster Thema \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` mit dem Zielendpunkt des webhooks `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="51588-122">Creates a new event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="51588-123">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="51588-123">This event subscription uses default filters.</span></span>

### <span data-ttu-id="51588-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51588-124">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51588-125">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einer Ressourcengruppe \` MyResourceGroupName \` mit dem Zielweb-Zielendpunkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="51588-125">Creates a new event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\` with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="51588-126">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="51588-126">This event subscription uses default filters.</span></span>

### <span data-ttu-id="51588-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="51588-127">Example 3</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51588-128">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="51588-128">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="51588-129">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="51588-129">This event subscription uses default filters.</span></span>

### <span data-ttu-id="51588-130">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="51588-130">Example 4</span></span>
```powershell
PS C:\> $includedEventTypes = "Microsoft.Resources.ResourceWriteFailure", "Microsoft.Resources.ResourceWriteSuccess"
PS C:\> $labels = "Finance", "HR"
PS C:\> New-AzEventGridSubscription -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1 -SubjectBeginsWith "TestPrefix" -SubjectEndsWith "TestSuffix" -IncludedEventType $includedEventTypes -Label $labels
```

<span data-ttu-id="51588-131">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 des aktuell ausgewählten Azure-Abonnements mit dem webhook-Zielendpunkt `https://requestb.in/19qlscd1` .</span><span class="sxs-lookup"><span data-stu-id="51588-131">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="51588-132">Dieses Ereignisabonnement gibt die zusätzlichen Filter für Ereignistypen und Betreff an, und nur Ereignisse, die diesen Filtern entsprechen, werden an den Zielendpunkt übermittelt.</span><span class="sxs-lookup"><span data-stu-id="51588-132">This event subscription specifies the additional filters for event types and subject, and only events matching those filters will be delivered to the destination endpoint.</span></span>

### <span data-ttu-id="51588-133">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="51588-133">Example 5</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -EventSubscriptionName EventSubscription1 -EndpointType "eventhub" -Endpoint "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace/eventhubs/EH1"
```

<span data-ttu-id="51588-134">Erstellt ein neues Ereignisabonnement \` EventSubscription1 \` des aktuell ausgewählten Azure-Abonnements mit dem angegebenen Ereignis-Hub als Ziel für Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="51588-134">Creates a new event subscription \`EventSubscription1\` to the currently selected Azure subscription with the specified event hub as the destination for events.</span></span> <span data-ttu-id="51588-135">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="51588-135">This event subscription uses default filters.</span></span>

### <span data-ttu-id="51588-136">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="51588-136">Example 6</span></span>
```powershell
PS C:\> New-AzEventGridSubscription -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/19qlscd1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="51588-137">Erstellt ein neues Ereignisabonnement \` \` -EventSubscription1 zu einem EventHub-Namespace mit dem angegebenen webhook `https://requestb.in/19qlscd1` -Zielendpunkt.</span><span class="sxs-lookup"><span data-stu-id="51588-137">Creates a new event subscription \`EventSubscription1\` to an EventHub namespace with the specified webhook destination endpoint `https://requestb.in/19qlscd1`.</span></span> <span data-ttu-id="51588-138">Dieses Ereignisabonnement verwendet Standardfilter.</span><span class="sxs-lookup"><span data-stu-id="51588-138">This event subscription uses default filters.</span></span>

## <span data-ttu-id="51588-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="51588-139">PARAMETERS</span></span>

### <span data-ttu-id="51588-140">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="51588-140">-AdvancedFilter</span></span>
<span data-ttu-id="51588-141">Erweiterter Filter, der ein Array mit mehreren Hashtable-Werten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51588-141">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="51588-142">Jeder Hashtable-Wert verfügt über die folgenden Schlüssel – Wert Informationen: Operation, Schlüssel und Wert oder Werte.</span><span class="sxs-lookup"><span data-stu-id="51588-142">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="51588-143">Der Operator kann einen der folgenden Werte aufweisen: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="51588-143">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="51588-144">Key stellt die Payload-Eigenschaft dar, in der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51588-144">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="51588-145">Schließlich Stellenwert oder Werte den Wert oder die Gruppe von Werten dar, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51588-145">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="51588-146">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="51588-146">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="51588-147">Als Beispiel für die erweiterten Filterparameter: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), wobei $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. key1"; Values = @ (1; 2)} und $AdvFilter 2 = @ {Operator = "StringBringsWith"; Key = "Betreff"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="51588-147">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBringsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="51588-148">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="51588-148">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="51588-149">Die Azure Active Directory (AAD)-Anwendungs-ID oder der URI zum Abrufen des Zugriffstokens, das in Zustellungs Anforderungen als Träger Token enthalten ist. Gilt nur für webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="51588-149">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="51588-150">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="51588-150">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="51588-151">Die Azure Active Directory (AAD)-Mandanten-ID zum Abrufen des Zugriffstokens, das in Zustellungs Anforderungen als Träger Token enthalten ist. Gilt nur für webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="51588-151">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="51588-152">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="51588-152">-DeadLetterEndpoint</span></span>
<span data-ttu-id="51588-153">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51588-153">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="51588-154">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="51588-154">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="51588-155">Beispiel:/Subscriptions/[Abonnement-Nr]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/Containers/[Containername].</span><span class="sxs-lookup"><span data-stu-id="51588-155">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="51588-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51588-156">-DefaultProfile</span></span>
<span data-ttu-id="51588-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="51588-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51588-158">-DeliverySchema</span><span class="sxs-lookup"><span data-stu-id="51588-158">-DeliverySchema</span></span>
<span data-ttu-id="51588-159">Das Schema, das verwendet werden soll, wenn Ereignisse an das Ziel übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="51588-159">The schema to be used when delivering events to the destination.</span></span> <span data-ttu-id="51588-160">Mögliche Werte sind: eventgridschema, CustomInputSchema oder cloudeventv01schema.</span><span class="sxs-lookup"><span data-stu-id="51588-160">The possible values are: eventgridschema, CustomInputSchema, or cloudeventv01schema.</span></span> <span data-ttu-id="51588-161">Der Standardwert ist CustomInputSchema.</span><span class="sxs-lookup"><span data-stu-id="51588-161">Default value is CustomInputSchema.</span></span>

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

### <span data-ttu-id="51588-162">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="51588-162">-DomainInputObject</span></span>
<span data-ttu-id="51588-163">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="51588-163">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="51588-164">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="51588-164">-DomainName</span></span>
<span data-ttu-id="51588-165">Der Name der Ereignis Raster Domäne, in der das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51588-165">The name of the Event Grid domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="51588-166">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="51588-166">-DomainTopicInputObject</span></span>
<span data-ttu-id="51588-167">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="51588-167">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="51588-168">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="51588-168">-DomainTopicName</span></span>
<span data-ttu-id="51588-169">Der Name des Domänen Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51588-169">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="51588-170">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="51588-170">-Endpoint</span></span>
<span data-ttu-id="51588-171">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="51588-171">Event subscription destination endpoint.</span></span>
<span data-ttu-id="51588-172">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID einer EventHub, Speicherwarteschlange, hybridconnection oder servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="51588-172">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="51588-173">Die Ressourcen-ID für eine hybridverbindung hat beispielsweise die folgende Form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Relay/Namespaces/[Namespacename]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="51588-173">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="51588-174">Es wird davon ausgegangen, dass der Zielendpunkt erstellt und für die Verwendung verfügbar ist, bevor Sie alle Ereignis Raster-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="51588-174">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="51588-175">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="51588-175">-EndpointType</span></span>
<span data-ttu-id="51588-176">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="51588-176">Endpoint Type.</span></span>
<span data-ttu-id="51588-177">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="51588-177">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="51588-178">Der Standardwert ist webhook.</span><span class="sxs-lookup"><span data-stu-id="51588-178">Default value is webhook.</span></span>

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

### <span data-ttu-id="51588-179">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="51588-179">-EventSubscriptionName</span></span>
<span data-ttu-id="51588-180">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="51588-180">The name of the event subscription</span></span>

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

### <span data-ttu-id="51588-181">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="51588-181">-EventTtl</span></span>
<span data-ttu-id="51588-182">Die Zeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="51588-182">The time in minutes for the event delivery.</span></span> <span data-ttu-id="51588-183">Dieser Wert muss zwischen 1 und 1440 sein.</span><span class="sxs-lookup"><span data-stu-id="51588-183">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="51588-184">-Wert des Felds</span><span class="sxs-lookup"><span data-stu-id="51588-184">-ExpirationDate</span></span>
<span data-ttu-id="51588-185">Bestimmt das Ablaufdatum für das Ereignisabonnement, nach dem das Ereignisabonnement in den Ruhestand geht.</span><span class="sxs-lookup"><span data-stu-id="51588-185">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="51588-186">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="51588-186">-IncludedEventType</span></span>
<span data-ttu-id="51588-187">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="51588-187">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="51588-188">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51588-188">-InputObject</span></span>
<span data-ttu-id="51588-189">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="51588-189">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="51588-190">-Label</span><span class="sxs-lookup"><span data-stu-id="51588-190">-Label</span></span>
<span data-ttu-id="51588-191">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="51588-191">Labels for the event subscription</span></span>

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

### <span data-ttu-id="51588-192">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="51588-192">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="51588-193">Die maximale Anzahl von versuchen, das Ereignis zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="51588-193">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="51588-194">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="51588-194">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="51588-195">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="51588-195">-MaxEventsPerBatch</span></span>
<span data-ttu-id="51588-196">Die maximale Anzahl von Ereignissen in einem Batch.</span><span class="sxs-lookup"><span data-stu-id="51588-196">The maximum number of events in a batch.</span></span> <span data-ttu-id="51588-197">Dieser Wert muss zwischen 1 und 5000 liegen.</span><span class="sxs-lookup"><span data-stu-id="51588-197">This value must be between 1 and 5000.</span></span> <span data-ttu-id="51588-198">Dieser Parameter ist gültig, wenn der Endpint-Typ nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="51588-198">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="51588-199">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="51588-199">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="51588-200">Die bevorzugte Batchgröße in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="51588-200">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="51588-201">Dieser Wert muss zwischen 1 und 1024 liegen.</span><span class="sxs-lookup"><span data-stu-id="51588-201">This value must be between 1 and 1024.</span></span> <span data-ttu-id="51588-202">Dieser Parameter ist gültig, wenn der Endpint-Typ nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="51588-202">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="51588-203">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51588-203">-ResourceGroupName</span></span>
<span data-ttu-id="51588-204">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="51588-204">The resource group of the topic.</span></span>

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

### <span data-ttu-id="51588-205">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="51588-205">-ResourceId</span></span>
<span data-ttu-id="51588-206">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51588-206">The identifier of the resource to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="51588-207">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="51588-207">-SubjectBeginsWith</span></span>
<span data-ttu-id="51588-208">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="51588-208">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="51588-209">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51588-209">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="51588-210">-SubjectCaseSensitive</span><span class="sxs-lookup"><span data-stu-id="51588-210">-SubjectCaseSensitive</span></span>
<span data-ttu-id="51588-211">Filter, der angibt, dass das Feld Betreff in einer Groß-/Kleinschreibung verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="51588-211">Filter that specifies that the subject field should be compared in a case sensitive manner.</span></span>
<span data-ttu-id="51588-212">Wenn keine Angabe erfolgt, wird der Betreff in einem Fall unempfindlich verglichen.</span><span class="sxs-lookup"><span data-stu-id="51588-212">If not specified, subject will be compared in a case insensitive manner.</span></span>

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

### <span data-ttu-id="51588-213">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="51588-213">-SubjectEndsWith</span></span>
<span data-ttu-id="51588-214">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="51588-214">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="51588-215">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="51588-215">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="51588-216">-Topicname</span><span class="sxs-lookup"><span data-stu-id="51588-216">-TopicName</span></span>
<span data-ttu-id="51588-217">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51588-217">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="51588-218">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51588-218">-Confirm</span></span>
<span data-ttu-id="51588-219">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51588-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51588-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51588-220">-WhatIf</span></span>
<span data-ttu-id="51588-221">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51588-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51588-222">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51588-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51588-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51588-223">CommonParameters</span></span>
<span data-ttu-id="51588-224">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51588-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51588-225">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51588-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51588-226">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51588-226">INPUTS</span></span>

### <span data-ttu-id="51588-227">System. String</span><span class="sxs-lookup"><span data-stu-id="51588-227">System.String</span></span>

### <span data-ttu-id="51588-228">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="51588-228">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="51588-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="51588-229">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="51588-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="51588-230">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="51588-231">System. String []</span><span class="sxs-lookup"><span data-stu-id="51588-231">System.String[]</span></span>

### <span data-ttu-id="51588-232">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51588-232">System.Int32</span></span>

## <span data-ttu-id="51588-233">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51588-233">OUTPUTS</span></span>

### <span data-ttu-id="51588-234">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="51588-234">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="51588-235">Notizen</span><span class="sxs-lookup"><span data-stu-id="51588-235">NOTES</span></span>

## <span data-ttu-id="51588-236">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51588-236">RELATED LINKS</span></span>
