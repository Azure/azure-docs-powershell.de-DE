---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/update-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Update-AzEventGridSubscription.md
ms.openlocfilehash: a5aee2c8df132a4218ece171453e04d1224f7adc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661068"
---
# <span data-ttu-id="cc924-101">Update-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cc924-101">Update-AzEventGridSubscription</span></span>

## <span data-ttu-id="cc924-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc924-102">SYNOPSIS</span></span>
<span data-ttu-id="cc924-103">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="cc924-103">Update the properties of an Event Grid event subscription.</span></span>

## <span data-ttu-id="cc924-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc924-104">SYNTAX</span></span>

### <span data-ttu-id="cc924-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc924-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc924-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc924-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String>
 [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>]
 [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>]
 [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc924-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc924-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Update-AzEventGridSubscription [-InputObject] <PSEventSubscription> [-EndpointType <String>]
 [-Endpoint <String>] [-SubjectBeginsWith <String>] [-SubjectEndsWith <String>] [-IncludedEventType <String[]>]
 [-Label <String[]>] [-EventTtl <Int32>] [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc924-108">CustomTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc924-108">CustomTopicEventSubscriptionParameterSet</span></span>
```
Update-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-EndpointType <String>] [-Endpoint <String>] [-SubjectBeginsWith <String>]
 [-SubjectEndsWith <String>] [-IncludedEventType <String[]>] [-Label <String[]>] [-EventTtl <Int32>]
 [-MaxDeliveryAttempt <Int32>] [-DeadLetterEndpoint <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc924-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc924-109">DESCRIPTION</span></span>
<span data-ttu-id="cc924-110">Aktualisieren Sie die Eigenschaften eines Ereignis Raster-Ereignisabonnements.</span><span class="sxs-lookup"><span data-stu-id="cc924-110">Update the properties of an Event Grid event subscription.</span></span> <span data-ttu-id="cc924-111">Dies kann verwendet werden, um den Filter, das Ziel oder die Bezeichnungen eines vorhandenen Ereignisabonnements zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="cc924-111">This can be used to update the filter, destination, or labels of an existing event subscription.</span></span>

## <span data-ttu-id="cc924-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc924-112">EXAMPLES</span></span>

### <span data-ttu-id="cc924-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc924-113">Example 1</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="cc924-114">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="cc924-114">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="cc924-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cc924-115">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName ES1 -TopicName Topic1 -ResourceGroup MyResourceGroupName | Update-AzEventGridSubscription -Endpoint https://requestb.in/1kxxoui1
```

<span data-ttu-id="cc924-116">Aktualisiert den Endpunkt des Ereignisabonnements \` ES1 \` für Topic \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` auf \`https://requestb.in/1kxxoui1\`</span><span class="sxs-lookup"><span data-stu-id="cc924-116">Updates the endpoint of the event subscription \`ES1\` for topic \`Topic1\` in resource group \`MyResourceGroupName\` to \`https://requestb.in/1kxxoui1\`</span></span>

### <span data-ttu-id="cc924-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cc924-117">Example 3</span></span>
```
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceId "/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/TestRG/providers/Microsoft.EventHub/namespaces/ContosoNamespace" -Endpoint https://requestb.in/1kxxoui1 -SubjectEndsWith "jpg"
```

<span data-ttu-id="cc924-118">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für den EventHub-Namespace ContosoNamespace mit dem neuen Endpunkt als \` https://requestb.in/1kxxoui1\ "und dem neuen SubjectEndsWith-Filter als \` JPG\`</span><span class="sxs-lookup"><span data-stu-id="cc924-118">Updates the properties of the event subscription \`ES1\` for the EventHub namespace ContosoNamespace with the new endpoint as \`https://requestb.in/1kxxoui1\` and the new SubjectEndsWith filter as \`jpg\`</span></span>

### <span data-ttu-id="cc924-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cc924-119">Example 4</span></span>
```
PS C:\> $labels = "Finance", "HR"
PS C:\> Update-AzEventGridSubscription -EventSubscriptionName ES1 -ResourceGroup MyResourceGroupName -Label $labels
```

<span data-ttu-id="cc924-120">Aktualisiert die Eigenschaften des Ereignisabonnement- \` ES1 \` für die Ressourcengruppe \` MyResourceGroupName \` mit dem neuen Etiketten $Labels.</span><span class="sxs-lookup"><span data-stu-id="cc924-120">Updates the properties of the event subscription \`ES1\` for the resource group \`MyResourceGroupName\` with the new labels $labels.</span></span>

## <span data-ttu-id="cc924-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc924-121">PARAMETERS</span></span>

### <span data-ttu-id="cc924-122">-DeadLetterEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc924-122">-DeadLetterEndpoint</span></span>
<span data-ttu-id="cc924-123">Der Endpunkt, der zum Speichern nicht zugestellter Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc924-123">The endpoint used for storing undelivered events.</span></span> <span data-ttu-id="cc924-124">Geben Sie die Azure-Ressourcen-ID eines Speicher-BLOB-Containers an.</span><span class="sxs-lookup"><span data-stu-id="cc924-124">Specify the Azure resource ID of a Storage blob container.</span></span> <span data-ttu-id="cc924-125">Beispiel:/Subscriptions/[Abonnement-Nr]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/Containers/[Containername].</span><span class="sxs-lookup"><span data-stu-id="cc924-125">For example: /subscriptions/[SubscriptionId]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Storage/storageAccounts/[StorageAccountName]/blobServices/default/containers/[ContainerName].</span></span>

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

### <span data-ttu-id="cc924-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc924-126">-DefaultProfile</span></span>
<span data-ttu-id="cc924-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc924-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc924-128">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="cc924-128">-Endpoint</span></span>
<span data-ttu-id="cc924-129">Zielendpunkt des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="cc924-129">Event subscription destination endpoint.</span></span>
<span data-ttu-id="cc924-130">Hierbei kann es sich um eine webhook-URL oder die Azure-Ressourcen-ID eines EventHub, einer Speicherwarteschlange oder eines hybridconnection handeln.</span><span class="sxs-lookup"><span data-stu-id="cc924-130">This can be a webhook URL, or the Azure resource ID of an EventHub, storage queue or hybridconnection.</span></span> <span data-ttu-id="cc924-131">Die Ressourcen-ID für eine hybridverbindung hat beispielsweise die folgende Form:/Subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/Providers/Microsoft.Relay/Namespaces/[Namespacename]/hybridConnections/[HybridConnectionName].</span><span class="sxs-lookup"><span data-stu-id="cc924-131">For example, the resource ID for a hybrid connection takes the following form: /subscriptions/[Azure Subscription ID]/resourceGroups/[ResourceGroupName]/providers/Microsoft.Relay/namespaces/[NamespaceName]/hybridConnections/[HybridConnectionName].</span></span> <span data-ttu-id="cc924-132">Es wird davon ausgegangen, dass der Zielendpunkt erstellt und für die Verwendung verfügbar ist, bevor Sie alle Ereignis Raster-Cmdlets ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc924-132">It is expected that the destination endpoint to be created and available for use before executing any Event Grid cmdlets.</span></span>


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

### <span data-ttu-id="cc924-133">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cc924-133">-EndpointType</span></span>
<span data-ttu-id="cc924-134">Endpunkttyp.</span><span class="sxs-lookup"><span data-stu-id="cc924-134">Endpoint Type.</span></span>
<span data-ttu-id="cc924-135">Dies kann webhook, eventhub, storagequeue oder hybridconnection sein.</span><span class="sxs-lookup"><span data-stu-id="cc924-135">This can be webhook, eventhub, storagequeue, or hybridconnection.</span></span> <span data-ttu-id="cc924-136">Der Standardwert ist webhook.</span><span class="sxs-lookup"><span data-stu-id="cc924-136">Default value is webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: webhook, eventhub, storagequeue, hybridconnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc924-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cc924-137">-EventSubscriptionName</span></span>
<span data-ttu-id="cc924-138">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="cc924-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="cc924-139">-EventTtl</span><span class="sxs-lookup"><span data-stu-id="cc924-139">-EventTtl</span></span>
<span data-ttu-id="cc924-140">Die Zeit in Minuten für die Ereigniszustellung.</span><span class="sxs-lookup"><span data-stu-id="cc924-140">The time in minutes for the event delivery.</span></span> <span data-ttu-id="cc924-141">Dieser Wert muss zwischen 1 und 1440 sein.</span><span class="sxs-lookup"><span data-stu-id="cc924-141">This value must be between 1 and 1440</span></span>

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

### <span data-ttu-id="cc924-142">-IncludedEventType</span><span class="sxs-lookup"><span data-stu-id="cc924-142">-IncludedEventType</span></span>
<span data-ttu-id="cc924-143">Filter, der eine Liste der einzubeziehenden Ereignistypen angibt. Wenn nicht angegeben, werden alle Ereignistypen einbezogen.</span><span class="sxs-lookup"><span data-stu-id="cc924-143">Filter that specifies a list of event types to include.If not specified, all event types will be included.</span></span>

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

### <span data-ttu-id="cc924-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc924-144">-InputObject</span></span>
<span data-ttu-id="cc924-145">EventGridSubscription-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc924-145">EventGridSubscription object.</span></span>

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

### <span data-ttu-id="cc924-146">-Label</span><span class="sxs-lookup"><span data-stu-id="cc924-146">-Label</span></span>
<span data-ttu-id="cc924-147">Beschriftungen für das Ereignisabonnement</span><span class="sxs-lookup"><span data-stu-id="cc924-147">Labels for the event subscription</span></span>

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

### <span data-ttu-id="cc924-148">-MaxDeliveryAttempt</span><span class="sxs-lookup"><span data-stu-id="cc924-148">-MaxDeliveryAttempt</span></span>
<span data-ttu-id="cc924-149">Die maximale Anzahl von versuchen, das Ereignis zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="cc924-149">The maximum number of attempts to deliver the event.</span></span> <span data-ttu-id="cc924-150">Dieser Wert muss zwischen 1 und 30 liegen.</span><span class="sxs-lookup"><span data-stu-id="cc924-150">This value must be between 1 and 30</span></span>

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

### <span data-ttu-id="cc924-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc924-151">-ResourceGroupName</span></span>
<span data-ttu-id="cc924-152">Die Ressourcengruppe des Themas.</span><span class="sxs-lookup"><span data-stu-id="cc924-152">The resource group of the topic.</span></span>

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
Parameter Sets: CustomTopicEventSubscriptionParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc924-153">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cc924-153">-ResourceId</span></span>
<span data-ttu-id="cc924-154">Der Bezeichner der Ressource, in der das Ereignisabonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cc924-154">The identifier of the resource to which the event subscription was created.</span></span>

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

### <span data-ttu-id="cc924-155">-SubjectBeginsWith</span><span class="sxs-lookup"><span data-stu-id="cc924-155">-SubjectBeginsWith</span></span>
<span data-ttu-id="cc924-156">Filter, der angibt, dass nur Ereignisse, die dem angegebenen Subjektpräfix entsprechen, enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cc924-156">Filter that specifies that only events matching the specified subject prefix will be included.</span></span>
<span data-ttu-id="cc924-157">Wenn nicht angegeben, werden Ereignisse mit allen Subjekt Präfixen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cc924-157">If not specified, events with all subject prefixes will be included.</span></span>

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

### <span data-ttu-id="cc924-158">-SubjectEndsWith</span><span class="sxs-lookup"><span data-stu-id="cc924-158">-SubjectEndsWith</span></span>
<span data-ttu-id="cc924-159">Filter, der angibt, dass nur Ereignisse enthalten sind, die dem angegebenen Subjekt Suffix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cc924-159">Filter that specifies that only events matching the specified subject suffix will be included.</span></span>
<span data-ttu-id="cc924-160">Wenn keine Angabe erfolgt, werden Ereignisse mit allen Subjekt Suffixen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="cc924-160">If not specified, events with all subject suffixes will be included.</span></span>

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

### <span data-ttu-id="cc924-161">-Topicname</span><span class="sxs-lookup"><span data-stu-id="cc924-161">-TopicName</span></span>
<span data-ttu-id="cc924-162">Der Name des Themas, in das das Ereignisabonnement erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc924-162">The name of the topic to which the event subscription should be created.</span></span>

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

### <span data-ttu-id="cc924-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cc924-163">-Confirm</span></span>
<span data-ttu-id="cc924-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc924-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc924-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc924-165">-WhatIf</span></span>
<span data-ttu-id="cc924-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc924-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc924-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc924-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc924-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc924-168">CommonParameters</span></span>
<span data-ttu-id="cc924-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc924-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc924-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc924-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc924-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc924-171">INPUTS</span></span>

### <span data-ttu-id="cc924-172">System. String</span><span class="sxs-lookup"><span data-stu-id="cc924-172">System.String</span></span>

### <span data-ttu-id="cc924-173">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="cc924-173">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="cc924-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc924-174">OUTPUTS</span></span>

### <span data-ttu-id="cc924-175">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="cc924-175">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="cc924-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc924-176">NOTES</span></span>

## <span data-ttu-id="cc924-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc924-177">RELATED LINKS</span></span>
