---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: dc8515cb37d18a36fa00c6803fda06a1e4d1f1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944176"
---
# <span data-ttu-id="e3942-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e3942-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="e3942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3942-102">SYNOPSIS</span></span>
<span data-ttu-id="e3942-103">Aktualisieren Sie die Eigenschaften eines Event Grid-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="e3942-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="e3942-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3942-104">SYNTAX</span></span>

### <span data-ttu-id="e3942-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3942-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3942-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3942-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3942-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3942-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3942-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3942-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3942-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3942-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3942-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3942-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3942-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3942-111">DESCRIPTION</span></span>
<span data-ttu-id="e3942-112">Aktualisieren Sie die Eigenschaften eines Event Grid-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="e3942-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="e3942-113">Dies kann verwendet werden, um den Filter, das Ziel oder die Bezeichnungen eines vorhandenen Ereignisabonnements zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e3942-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="e3942-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3942-114">EXAMPLES</span></span>

### <span data-ttu-id="e3942-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3942-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e3942-116">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für \` Topic1 \` in der Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e3942-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e3942-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e3942-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="e3942-118">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für \` Topic1 \` in der Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="e3942-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="e3942-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e3942-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="e3942-120">Aktualisiert die Eigenschaften des Ereignisabonnements ES1 für den EventHub-Namespace ContosoNamespace mit dem neuen Endpunkt als ' und dem neuen \` \` \` https://requestb.in/1kxxoui1\ SubjectEndsWith-Filter als \` jpg\`</span><span class="sxs-lookup"><span data-stu-id="e3942-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="e3942-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e3942-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="e3942-122">Aktualisiert die Eigenschaften des Ereignisabonnements ES1 für \` \` die Ressourcengruppe \` MyResourceGroupName mit den neuen \` Bezeichnungen $labels.</span><span class="sxs-lookup"><span data-stu-id="e3942-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="e3942-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e3942-123">PARAMETERS</span></span>

### <span data-ttu-id="e3942-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="e3942-124">-AdvancedFilter</span></span>
<span data-ttu-id="e3942-125">Erweiterter Filter, der ein Array mit mehreren Hashtablewerten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3942-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="e3942-126">Jeder Hashtablewert enthält die folgenden Schlüssel-Wert-Informationen: Vorgang, Schlüssel und Wert oder Werte.</span><span class="sxs-lookup"><span data-stu-id="e3942-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="e3942-127">Operator kann einer der folgenden Werte sein: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="e3942-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="e3942-128">Key stellt die Nutzlasteigenschaft dar, bei der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3942-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="e3942-129">Schließlich stellen "Wert" oder "Werte" den Wert oder eine Gruppe von Werten dar, die übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="e3942-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="e3942-130">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="e3942-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="e3942-131">Beispiel für die erweiterten Filterparameter: $AdvancedFilters=@($AdvFilter 1; $AdvFilter 2), wobei $AdvFilter 1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} und $AdvFilter 2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1";SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="e3942-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="e3942-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="e3942-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="e3942-133">Die Azure Active Directory (AAD)-Anwendungs-ID oder der Uri, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen eingeschlossen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="e3942-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="e3942-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="e3942-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="e3942-135">Die Azure Active Directory (AAD)-Mandanten-ID, um das Zugriffstoken abzurufen, das als Bearertoken in Übermittlungsanforderungen einbezogen wird. Gilt nur für Webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="e3942-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="e3942-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3942-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="e3942-137">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3942-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="e3942-138">Geben Sie die Azure-Ressourcen-ID eines Speicherblobscontainers an.</span><span class="sxs-lookup"><span data-stu-id="e3942-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="e3942-139">Beispiel: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span><span class="sxs-lookup"><span data-stu-id="e3942-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="e3942-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3942-140">-DefaultProfile</span></span>
<span data-ttu-id="e3942-141">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3942-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3942-142">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e3942-142">-DomainName</span></span>
<span data-ttu-id="e3942-143">Der Name der Domäne, für die das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3942-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e3942-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="e3942-144">-DomainTopicName</span></span>
<span data-ttu-id="e3942-145">Der Name des Domänenthemas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3942-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e3942-146">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e3942-146">-Endpoint</span></span>
<span data-ttu-id="e3942-147">Endpunkt des Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="e3942-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="e3942-148">Dies kann eine Webhook-URL oder die Azure-Ressourcen-ID eines EventHubs, einer Speicherwarteschlange, einer Hybridverbindung oder eines Dienstbusqueues sein.</span><span class="sxs-lookup"><span data-stu-id="e3942-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="e3942-149">Beispielsweise hat die Ressourcen-ID für eine Hybridverbindung das folgende Formular: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="e3942-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="e3942-150">Es wird erwartet, dass der Zielendpunkt erstellt und zur Verwendung verfügbar ist, bevor Ereignisraster-Cmdlets ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3942-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="e3942-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="e3942-151">-EndpointType</span></span>
<span data-ttu-id="e3942-152">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="e3942-152">Endpoint Type.</span></span>
<span data-ttu-id="e3942-153">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="e3942-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="e3942-154">Standardwert ist Webhook.</span><span class="sxs-lookup"><span data-stu-id="e3942-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="e3942-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e3942-155">-EventSubscriptionName</span></span>
<span data-ttu-id="e3942-156">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="e3942-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="e3942-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="e3942-157">-EventTtl</span></span>
<span data-ttu-id="e3942-158">Die Uhrzeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="e3942-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="e3942-159">Dieser Wert muss zwischen 1 und 1440 liegen.</span><span class="sxs-lookup"><span data-stu-id="e3942-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="e3942-160">-ExpirationDate</span><span class="sxs-lookup"><span data-stu-id="e3942-160">-ExpirationDate</span></span>
<span data-ttu-id="e3942-161">Bestimmt den Ablauf von DateTime für das Ereignisabonnement, nach dem das Ereignisabonnement ausläuft.</span><span class="sxs-lookup"><span data-stu-id="e3942-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="e3942-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="e3942-162">-IncludedEventType</span></span>
<span data-ttu-id="e3942-163">Filter, der eine Liste der hinzuzufügenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e3942-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="e3942-164">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3942-164">-InputObject</span></span>
<span data-ttu-id="e3942-165">EventGridSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e3942-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="e3942-166">-Label</span><span class="sxs-lookup"><span data-stu-id="e3942-166">-Label</span></span>
<span data-ttu-id="e3942-167">Bezeichnungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="e3942-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="e3942-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="e3942-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="e3942-169">Die maximale Anzahl von Versuchen, das Ereignis zu liefern.</span><span class="sxs-lookup"><span data-stu-id="e3942-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="e3942-170">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="e3942-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="e3942-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="e3942-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="e3942-172">Die maximale Anzahl von Ereignissen in einem Batch.</span><span class="sxs-lookup"><span data-stu-id="e3942-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="e3942-173">Dieser Wert muss zwischen 1 und 5000 liegen.</span><span class="sxs-lookup"><span data-stu-id="e3942-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="e3942-174">Dieser Parameter ist gültig, wenn endpint Type nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="e3942-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="e3942-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="e3942-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="e3942-176">Die bevorzugte Batchgröße in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="e3942-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="e3942-177">Dieser Wert muss zwischen 1 und 1024 liegen.</span><span class="sxs-lookup"><span data-stu-id="e3942-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="e3942-178">Dieser Parameter ist gültig, wenn endpint Type nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="e3942-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="e3942-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3942-179">-ResourceGroupName</span></span>
<span data-ttu-id="e3942-180">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="e3942-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="e3942-181">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3942-181">-ResourceId</span></span>
<span data-ttu-id="e3942-182">Der Bezeichner der Ressource, für die das Ereignisabonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3942-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="e3942-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="e3942-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="e3942-184">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffpräfix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e3942-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="e3942-185">Wenn nicht angegeben, werden Ereignisse mit allen Betreffpräfixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e3942-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="e3942-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="e3942-186">-SubjectEndsWith</span></span>
<span data-ttu-id="e3942-187">Filter, der angibt, dass nur Ereignisse einbezogen werden, die mit dem angegebenen Betreffsuffix übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="e3942-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="e3942-188">Wenn nicht angegeben, werden Ereignisse mit allen Betreffsuffixen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="e3942-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="e3942-189">-TopicName</span><span class="sxs-lookup"><span data-stu-id="e3942-189">-TopicName</span></span>
<span data-ttu-id="e3942-190">Der Name des Themas, für das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3942-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="e3942-191">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3942-191">-Confirm</span></span>
<span data-ttu-id="e3942-192">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3942-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3942-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3942-193">-WhatIf</span></span>
<span data-ttu-id="e3942-194">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3942-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3942-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3942-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3942-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3942-196">CommonParameters</span></span>
<span data-ttu-id="e3942-197">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3942-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3942-198">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3942-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3942-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3942-199">INPUTS</span></span>

### <span data-ttu-id="e3942-200">System.String</span><span class="sxs-lookup"><span data-stu-id="e3942-200">System.String</span></span>

### <span data-ttu-id="e3942-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e3942-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e3942-202">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3942-202">OUTPUTS</span></span>

### <span data-ttu-id="e3942-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="e3942-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="e3942-204">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e3942-204">NOTES</span></span>

## <span data-ttu-id="e3942-205">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e3942-205">RELATED LINKS</span></span>
