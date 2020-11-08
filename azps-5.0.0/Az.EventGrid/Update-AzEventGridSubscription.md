---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: 7398dd0a80e2f84dcce929019038c616f6c7c1c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177659"
---
# <span data-ttu-id="7bb5d-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7bb5d-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="7bb5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb5d-103">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="7bb5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bb5d-104">SYNTAX</span></span>

### <span data-ttu-id="7bb5d-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bb5d-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb5d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb5d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb5d-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb5d-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>]
 [-PreferredBatchSizeInKiloBytes <Int32>] [-AzureActiveDirectoryApplicationIdOrUri <String>]
 [-AzureActiveDirectoryTenantId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb5d-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb5d-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb5d-109">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb5d-109">DomainEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-ExpirationDate <DateTime>]
 [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bb5d-110">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb5d-110">DomainTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName] <String> [-EndpointType <String>] [-Endpoint <String>]
 [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>]
 [-ExpirationDate <DateTime>] [-AdvancedFilter <Hashtable[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-MaxEventsPerBatch <Int32>] [-PreferredBatchSizeInKiloBytes <Int32>]
 [-AzureActiveDirectoryApplicationIdOrUri <String>] [-AzureActiveDirectoryTenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb5d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bb5d-111">DESCRIPTION</span></span>
<span data-ttu-id="7bb5d-112">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-112">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="7bb5d-113">Dies kann verwendet werden, um den Filter, das Ziel oder die Bezeichnungen eines vorhandenen Ereignisabonnements zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-113">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="7bb5d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bb5d-114">EXAMPLES</span></span>

### <span data-ttu-id="7bb5d-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bb5d-115">Example 1</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="7bb5d-116">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="7bb5d-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="7bb5d-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7bb5d-117">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="7bb5d-118">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="7bb5d-118">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="7bb5d-119">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7bb5d-119">Example 3</span></span>
```powershell
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="7bb5d-120">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für den EventHub-Namespace ContosoNamespace mit dem neuen Endpunkt als \` https://requestb.in/1kxxoui1\ "und dem neuen SubjectEndsWith-Filter als \` JPG\`</span><span class="sxs-lookup"><span data-stu-id="7bb5d-120">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="7bb5d-121">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="7bb5d-121">Example 4</span></span>
```powershell
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="7bb5d-122">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für die Ressourcengruppe \` MyResourceGroupName \` mit dem neuen Etiketten $Labels.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-122">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="7bb5d-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bb5d-123">PARAMETERS</span></span>

### <span data-ttu-id="7bb5d-124">-AdvancedFilter</span><span class="sxs-lookup"><span data-stu-id="7bb5d-124">-AdvancedFilter</span></span>
<span data-ttu-id="7bb5d-125">Erweiterter Filter, der ein Array mit mehreren Hashtable-Werten angibt, die für die attributbasierte Filterung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-125">Advanced filter that specifies an array of multiple Hashtable values that are used for the attribute-based filtering.</span></span> <span data-ttu-id="7bb5d-126">Jeder Hashtable-Wert verfügt über die folgenden Schlüssel – Wert Informationen: Operation, Schlüssel und Wert oder Werte.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-126">Each Hashtable value has the following keys-value info: Operation, Key and Value or Values.</span></span> <span data-ttu-id="7bb5d-127">Der Operator kann einen der folgenden Werte aufweisen: numberin, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, stringIn, StringNotIn, StringBeginsWith, StringEndsWith oder StringContains.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-127">Operator can be one of the following values: NumberIn, NumberNotIn, NumberLessThan, NumberGreaterThan, NumberLessThanOrEquals, NumberGreaterThanOrEquals, BoolEquals, StringIn, StringNotIn, StringBeginsWith, StringEndsWith or StringContains.</span></span> <span data-ttu-id="7bb5d-128">Key stellt die Payload-Eigenschaft dar, in der die erweiterten Filterrichtlinien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-128">Key represents the payload property where the advanced filtering policies are applied.</span></span> <span data-ttu-id="7bb5d-129">Schließlich Stellenwert oder Werte den Wert oder die Gruppe von Werten dar, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-129">Finally, Value or Values represent the value or set of values to be matched.</span></span> <span data-ttu-id="7bb5d-130">Dies kann ein einzelner Wert des entsprechenden Typs oder ein Array von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-130">This can be a single value of the corresponding type or an array of values.</span></span> <span data-ttu-id="7bb5d-131">Als Beispiel für die erweiterten Filterparameter: $AdvancedFilters = @ ($AdvFilter 1, $AdvFilter 2), wobei $AdvFilter 1 = @ {Operator = "numberin"; Key = "Data. key1"; Values = @ (1; 2)} und $AdvFilter 2 = @ {Operator = "StringBeginsWith"; Key = "Betreff"; Values = @ ("SubjectPrefix1"; "SubjectPrefix2")}</span><span class="sxs-lookup"><span data-stu-id="7bb5d-131">As an example of the advanced filter parameters: $AdvancedFilters=@($AdvFilter1, $AdvFilter2) where $AdvFilter1=@{operator="NumberIn"; key="Data.Key1"; Values=@(1,2)} and $AdvFilter2=@{operator="StringBeginsWith"; key="Subject"; Values=@("SubjectPrefix1","SubjectPrefix2")}</span></span>

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

### <span data-ttu-id="7bb5d-132">-AzureActiveDirectoryApplicationIdOrUri</span><span class="sxs-lookup"><span data-stu-id="7bb5d-132">-AzureActiveDirectoryApplicationIdOrUri</span></span>
<span data-ttu-id="7bb5d-133">Die Azure Active Directory (AAD)-Anwendungs-ID oder der URI zum Abrufen des Zugriffstokens, das in Zustellungs Anforderungen als Träger Token enthalten ist. Gilt nur für webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-133">The Azure Active Directory (AAD) Application Id or Uri to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="7bb5d-134">-AzureActiveDirectoryTenantId</span><span class="sxs-lookup"><span data-stu-id="7bb5d-134">-AzureActiveDirectoryTenantId</span></span>
<span data-ttu-id="7bb5d-135">Die Azure Active Directory (AAD)-Mandanten-ID zum Abrufen des Zugriffstokens, das in Zustellungs Anforderungen als Träger Token enthalten ist. Gilt nur für webhook als Ziel.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-135">The Azure Active Directory (AAD) Tenant Id to get the access token that will be included as the bearer token in delivery requests.Applicable only for webhook as a destination.</span></span>

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

### <span data-ttu-id="7bb5d-136">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bb5d-136">-DeadLetterEndpoint</span></span>
<span data-ttu-id="7bb5d-137">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-137">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="7bb5d-138">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-138">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="7bb5d-139">Beispiel:/Subscriptions/[Abonnement-Nr]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/Containers/[Containername].</span><span class="sxs-lookup"><span data-stu-id="7bb5d-139">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="7bb5d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb5d-140">-DefaultProfile</span></span>
<span data-ttu-id="7bb5d-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb5d-142">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="7bb5d-142">-DomainName</span></span>
<span data-ttu-id="7bb5d-143">Der Name der Domäne, in der das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-143">The name of the domain to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7bb5d-144">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="7bb5d-144">-DomainTopicName</span></span>
<span data-ttu-id="7bb5d-145">Der Name des Domänen Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-145">The name of the domain topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7bb5d-146">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7bb5d-146">-Endpoint</span></span>
<span data-ttu-id="7bb5d-147">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="7bb5d-147">Event subscription destination endpoint.</span></span>
<span data-ttu-id="7bb5d-148">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID einer EventHub, Speicherwarteschlange, hybridconnection oder servicebusqueue.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-148">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="7bb5d-149">Die Ressourcen-ID für eine hybridverbindung hat beispielsweise die folgende Form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Relay/Namespaces/[Namespacename]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="7bb5d-149">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="7bb5d-150">Es wird davon ausgegangen, dass der Zielendpunkt erstellt und für die Verwendung verfügbar ist, bevor Sie alle Ereignis Raster-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-150">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>

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

### <span data-ttu-id="7bb5d-151">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="7bb5d-151">-EndpointType</span></span>
<span data-ttu-id="7bb5d-152">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-152">Endpoint Type.</span></span>
<span data-ttu-id="7bb5d-153">Dies kann webhook, eventhub, storagequeue, hybridconnection oder servicebusqueue sein.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-153">This can be webhook, eventhub, storagequeue, hybridconnection or servicebusqueue.</span></span> <span data-ttu-id="7bb5d-154">Der Standardwert ist webhook.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-154">Default value is webhook.</span></span>

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

### <span data-ttu-id="7bb5d-155">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="7bb5d-155">-EventSubscriptionName</span></span>
<span data-ttu-id="7bb5d-156">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="7bb5d-156">The name of the event subscription</span></span>

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

### <span data-ttu-id="7bb5d-157">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="7bb5d-157">-EventTtl</span></span>
<span data-ttu-id="7bb5d-158">Die Zeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-158">The time in minutes for the event delivery.</span></span> <span data-ttu-id="7bb5d-159">Dieser Wert muss zwischen 1 und 1440 sein.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-159">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="7bb5d-160">-Wert des Felds</span><span class="sxs-lookup"><span data-stu-id="7bb5d-160">-ExpirationDate</span></span>
<span data-ttu-id="7bb5d-161">Bestimmt das Ablaufdatum für das Ereignisabonnement, nach dem das Ereignisabonnement in den Ruhestand geht.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-161">Determines the expiration DateTime for the event subscription after which event subscription will retire.</span></span>

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

### <span data-ttu-id="7bb5d-162">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="7bb5d-162">-IncludedEventType</span></span>
<span data-ttu-id="7bb5d-163">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-163">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="7bb5d-164">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7bb5d-164">-InputObject</span></span>
<span data-ttu-id="7bb5d-165">EventGridSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-165">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="7bb5d-166">-Label</span><span class="sxs-lookup"><span data-stu-id="7bb5d-166">-Label</span></span>
<span data-ttu-id="7bb5d-167">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="7bb5d-167">Labels for the event subscription</span></span>

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

### <span data-ttu-id="7bb5d-168">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="7bb5d-168">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="7bb5d-169">Die maximale Anzahl von versuchen, das Ereignis zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-169">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="7bb5d-170">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-170">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="7bb5d-171">-MaxEventsPerBatch</span><span class="sxs-lookup"><span data-stu-id="7bb5d-171">-MaxEventsPerBatch</span></span>
<span data-ttu-id="7bb5d-172">Die maximale Anzahl von Ereignissen in einem Batch.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-172">The maximum number of events in a batch.</span></span> <span data-ttu-id="7bb5d-173">Dieser Wert muss zwischen 1 und 5000 liegen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-173">This value must be between 1 and 5000.</span></span> <span data-ttu-id="7bb5d-174">Dieser Parameter ist gültig, wenn der Endpint-Typ nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-174">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="7bb5d-175">-PreferredBatchSizeInKiloBytes</span><span class="sxs-lookup"><span data-stu-id="7bb5d-175">-PreferredBatchSizeInKiloBytes</span></span>
<span data-ttu-id="7bb5d-176">Die bevorzugte Batchgröße in Kilobytes.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-176">The preferred batch size in kilobytes.</span></span> <span data-ttu-id="7bb5d-177">Dieser Wert muss zwischen 1 und 1024 liegen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-177">This value must be between 1 and 1024.</span></span> <span data-ttu-id="7bb5d-178">Dieser Parameter ist gültig, wenn der Endpint-Typ nur webhook ist.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-178">This parameter is valid when Endpint Type is webhook only.</span></span>

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

### <span data-ttu-id="7bb5d-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb5d-179">-ResourceGroupName</span></span>
<span data-ttu-id="7bb5d-180">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-180">The resource group of the topic.</span></span>

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

### <span data-ttu-id="7bb5d-181">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7bb5d-181">-ResourceId</span></span>
<span data-ttu-id="7bb5d-182">Der Bezeichner der Ressource, in der das Ereignisabonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-182">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="7bb5d-183">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="7bb5d-183">-SubjectBeginsWith</span></span>
<span data-ttu-id="7bb5d-184">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-184">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="7bb5d-185">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-185">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="7bb5d-186">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="7bb5d-186">-SubjectEndsWith</span></span>
<span data-ttu-id="7bb5d-187">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-187">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="7bb5d-188">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-188">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="7bb5d-189">-Topicname</span><span class="sxs-lookup"><span data-stu-id="7bb5d-189">-TopicName</span></span>
<span data-ttu-id="7bb5d-190">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-190">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="7bb5d-191">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bb5d-191">-Confirm</span></span>
<span data-ttu-id="7bb5d-192">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb5d-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb5d-193">-WhatIf</span></span>
<span data-ttu-id="7bb5d-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb5d-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb5d-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb5d-196">CommonParameters</span></span>
<span data-ttu-id="7bb5d-197">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb5d-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb5d-198">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bb5d-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb5d-199">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bb5d-199">INPUTS</span></span>

### <span data-ttu-id="7bb5d-200">System. String</span><span class="sxs-lookup"><span data-stu-id="7bb5d-200">System.String</span></span>

### <span data-ttu-id="7bb5d-201">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7bb5d-201">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="7bb5d-202">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bb5d-202">OUTPUTS</span></span>

### <span data-ttu-id="7bb5d-203">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="7bb5d-203">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="7bb5d-204">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bb5d-204">NOTES</span></span>

## <span data-ttu-id="7bb5d-205">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bb5d-205">RELATED LINKS</span></span>
