---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299219"
---
# <span data-ttu-id="135a3-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="135a3-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="135a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="135a3-102">SYNOPSIS</span></span>
<span data-ttu-id="135a3-103">Aktualisieren Sie die Eigenschaften eines Ereignisrasterereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="135a3-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="135a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="135a3-104">SYNTAX</span></span>

### <span data-ttu-id="135a3-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="135a3-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="135a3-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="135a3-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="135a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="135a3-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="135a3-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="135a3-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="135a3-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="135a3-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="135a3-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="135a3-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="135a3-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="135a3-111">DESCRIPTION</span></span>
<span data-ttu-id="135a3-112">Aktualisieren Sie die Eigenschaften eines Ereignisrasterereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="135a3-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="135a3-113">Dies kann verwendet werden, um den Filter, das Ziel oder die Bezeichnungen eines vorhandenen Ereignisabonnements zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="135a3-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="135a3-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="135a3-114">EXAMPLES</span></span>

### <span data-ttu-id="135a3-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="135a3-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="135a3-116">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` Topic1 in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="135a3-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="135a3-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="135a3-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="135a3-118">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` Topic1 in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="135a3-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="135a3-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="135a3-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="135a3-120">Aktualisiert die Eigenschaften des Ereignisabonnements ES1 für den EventHub-Namespace ContosoNamespace mit dem neuen Endpunkt als ' und dem neuen \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith-Filter als \` JPG\`</span><span class="sxs-lookup"><span data-stu-id="135a3-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="135a3-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="135a3-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="135a3-122">Aktualisiert die Eigenschaften des Ereignisabonnements \` ES1 \` für die Ressourcengruppe \` "MyResourceGroupName" mit den \` neuen Bezeichnungen $labels.</span><span class="sxs-lookup"><span data-stu-id="135a3-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="135a3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="135a3-123">PARAMETERS</span></span>

### <span data-ttu-id="135a3-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="135a3-124">-AdvancedFilter</span></span>
<span data-ttu-id="135a3-125">Erweiterter Filter, der ein Array mit mehreren Hashtablewerten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="135a3-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="135a3-126">Jeder Hashtablewert enthält die folgenden Schlüssel-Wert-Informationen: Operation, Schlüssel und Wert oder Werte.</span><span class="sxs-lookup"><span data-stu-id="135a3-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="135a3-127">Der Operator kann einer der folgenden Werte sein: NumberIn, NumberNotIn, NumberLessLite, NumberGreater Nur, NumberLessLiteOrEquals, NumberGreaterLiteOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="135a3-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="135a3-128">Der Schlüssel stellt die Nutzlasteigenschaft dar, in der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="135a3-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="135a3-129">Schließlich stellen "Wert" oder "Werte" den Wert oder die Gruppe von Werten dar, die übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="135a3-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="135a3-130">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="135a3-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="135a3-131">Beispiel für die erweiterten Filterparameter: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), wobei $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} und $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1";"SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="135a3-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="135a3-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="135a3-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="135a3-133">Die Azure Active Directory (AAD)-Anwendungs-ID oder der URI, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen eingeschlossen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="135a3-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadAppIdUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="135a3-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="135a3-135">Die Azure Active Directory (AAD)-Mandanten-ID, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen eingeschlossen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="135a3-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AliasAadTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="135a3-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="135a3-137">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="135a3-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="135a3-138">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="135a3-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="135a3-139">Beispiel: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="135a3-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135a3-140">-DefaultProfile</span></span>
<span data-ttu-id="135a3-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="135a3-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="135a3-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="135a3-142">-DomainName</span></span>
<span data-ttu-id="135a3-143">Der Name der Domäne, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="135a3-143">The name of the domain to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="135a3-144">-DomainTopicName</span></span>
<span data-ttu-id="135a3-145">Der Name des Domänenthemas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="135a3-145">The name of the domain topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-146">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="135a3-146">-Endpoint</span></span>
<span data-ttu-id="135a3-147">Endpunkt des Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="135a3-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="135a3-148">Dabei kann es sich um eine Webhook-URL oder die Azure-Ressourcen-ID eines EventHub, einer Speicherwarteschlange, Hybridverbindung oder eines Dienstbusqueues sein.</span><span class="sxs-lookup"><span data-stu-id="135a3-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="135a3-149">Beispielsweise hat die Ressourcen-ID für eine Hybridverbindung das folgende Format: /subscriptions/[Azure-Abonnement-ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="135a3-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="135a3-150">Es wird erwartet, dass der Zielendpunkt erstellt und zur Verwendung zur Verfügung steht, bevor Ereignisraster-Cmdlets ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="135a3-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="135a3-151">-EndpointType</span></span>
<span data-ttu-id="135a3-152">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="135a3-152">Endpoint Type.</span></span>
<span data-ttu-id="135a3-153">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="135a3-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="135a3-154">Der Standardwert ist "Webhook".</span><span class="sxs-lookup"><span data-stu-id="135a3-154">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection, servicebusqueue, servicebustopic, azurefunction

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="135a3-155">-EventSubscriptionName</span></span>
<span data-ttu-id="135a3-156">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="135a3-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="135a3-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="135a3-157">-EventTtl</span></span>
<span data-ttu-id="135a3-158">Die Uhrzeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="135a3-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="135a3-159">Dieser Wert muss zwischen 1 und 1440 liegen.</span><span class="sxs-lookup"><span data-stu-id="135a3-159">This value must be between 1 and 1440</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="135a3-160">-ExpirationDate</span></span>
<span data-ttu-id="135a3-161">Bestimmt den Ablauf von "DateTime" für das Ereignisabonnement, nach dem das Ereignisabonnement abläuft.</span><span class="sxs-lookup"><span data-stu-id="135a3-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="135a3-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="135a3-162">-IncludedEventType</span></span>
<span data-ttu-id="135a3-163">Filter, der eine Liste der hinzuzufügenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="135a3-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="135a3-164">-InputObject</span></span>
<span data-ttu-id="135a3-165">EventGridSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="135a3-165">EventGridSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-166">-Label</span><span class="sxs-lookup"><span data-stu-id="135a3-166">-Label</span></span>
<span data-ttu-id="135a3-167">Bezeichnungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="135a3-167">Labels for the event subscription</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="135a3-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="135a3-169">Die maximale Anzahl von Versuchen, das Ereignis zu liefern.</span><span class="sxs-lookup"><span data-stu-id="135a3-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="135a3-170">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="135a3-170">This value must be between 1 and 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="135a3-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="135a3-172">Die maximale Anzahl von Ereignissen in einem Batch.</span><span class="sxs-lookup"><span data-stu-id="135a3-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="135a3-173">Dieser Wert muss zwischen 1 und 5000 liegen.</span><span class="sxs-lookup"><span data-stu-id="135a3-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="135a3-174">Dieser Parameter ist gültig, wenn der Endpinttyp nur ein Webhook ist.</span><span class="sxs-lookup"><span data-stu-id="135a3-174">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="135a3-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="135a3-176">Die bevorzugte Batchgröße in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="135a3-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="135a3-177">Dieser Wert muss zwischen 1 und 1024 liegen.</span><span class="sxs-lookup"><span data-stu-id="135a3-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="135a3-178">Dieser Parameter ist gültig, wenn der Endpinttyp nur ein Webhook ist.</span><span class="sxs-lookup"><span data-stu-id="135a3-178">This parameter is valid when Endpint Type is webhook only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="135a3-179">-ResourceGroupName</span></span>
<span data-ttu-id="135a3-180">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="135a3-180">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="135a3-181">-ResourceId</span></span>
<span data-ttu-id="135a3-182">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="135a3-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="135a3-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="135a3-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="135a3-184">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffpräfix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="135a3-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="135a3-185">Wenn nichts angegeben wird, werden Ereignisse mit allen Betreffpräfixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="135a3-185">If not specified, events with all subject prefixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="135a3-186">-SubjectEndsWith</span></span>
<span data-ttu-id="135a3-187">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffsuffix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="135a3-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="135a3-188">Wenn nichts angegeben wird, werden Ereignisse mit allen Subjektsuffixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="135a3-188">If not specified, events with all subject suffixes will be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="135a3-189">-TopicName</span></span>
<span data-ttu-id="135a3-190">Der Name des Themas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="135a3-190">The name of the topic to which the event subscription should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="135a3-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="135a3-191">-Confirm</span></span>
<span data-ttu-id="135a3-192">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="135a3-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="135a3-193">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="135a3-193">-WhatIf</span></span>
<span data-ttu-id="135a3-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="135a3-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="135a3-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="135a3-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="135a3-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135a3-196">CommonParameters</span></span>
<span data-ttu-id="135a3-197">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135a3-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135a3-198">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="135a3-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135a3-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="135a3-199">INPUTS</span></span>

### <span data-ttu-id="135a3-200">System.String</span><span class="sxs-lookup"><span data-stu-id="135a3-200">System.String</span></span>

### <span data-ttu-id="135a3-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="135a3-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="135a3-202">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="135a3-202">OUTPUTS</span></span>

### <span data-ttu-id="135a3-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="135a3-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="135a3-204">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="135a3-204">NOTES</span></span>

## <span data-ttu-id="135a3-205">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="135a3-205">RELATED LINKS</span></span>
