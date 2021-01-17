---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458744"
---
# <span data-ttu-id="5edfb-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="5edfb-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="5edfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5edfb-102">SYNOPSIS</span></span>
<span data-ttu-id="5edfb-103">Ruft die Details eines Themas "Veranstaltungsraster" ab oder ruft eine Liste aller Themen zum Veranstaltungsraster im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="5edfb-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="5edfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5edfb-104">SYNTAX</span></span>

### <span data-ttu-id="5edfb-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5edfb-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5edfb-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edfb-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5edfb-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edfb-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5edfb-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="5edfb-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edfb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5edfb-109">DESCRIPTION</span></span>
<span data-ttu-id="5edfb-110">Das Get-AzEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen "Veranstaltungsrasterthemas" oder eine Liste aller Themen zum Veranstaltungsraster im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="5edfb-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="5edfb-111">Wenn der Themaname angegeben wird, werden die Details eines einzelnen Ereignisrasterthemas zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5edfb-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="5edfb-112">Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5edfb-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="5edfb-113">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter "Top" gesteuert.</span><span class="sxs-lookup"><span data-stu-id="5edfb-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="5edfb-114">Wenn der Oberste Wert nicht angegeben oder nicht $null, enthält die Liste alle Themenelemente.</span><span class="sxs-lookup"><span data-stu-id="5edfb-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="5edfb-115">Andernfalls gibt "Top" die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5edfb-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="5edfb-116">Wenn noch weitere Themen verfügbar sind, sollte der Wert in "NextLink" im nächsten Aufruf verwendet werden, um die nächste Seite mit Themen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5edfb-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="5edfb-117">Schließlich wird der Parameter "ODataQuery" zum Filtern der Suchergebnisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="5edfb-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="5edfb-118">Die Filterabfrage folgt der #A0 nur mit der Eigenschaft "Name".</span><span class="sxs-lookup"><span data-stu-id="5edfb-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="5edfb-119">Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="5edfb-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="5edfb-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5edfb-120">EXAMPLES</span></span>

### <span data-ttu-id="5edfb-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5edfb-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5edfb-122">Ruft die Details des Themas "Veranstaltungsraster" \` "Topic1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="5edfb-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5edfb-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5edfb-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="5edfb-124">Ruft die Details des Themas "Veranstaltungsraster" \` "Topic1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="5edfb-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5edfb-125">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5edfb-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="5edfb-126">Listet alle Themen zum Veranstaltungsraster in der Ressourcengruppe \` "MyResourceGroupName" \` ohne Paginierung auf.</span><span class="sxs-lookup"><span data-stu-id="5edfb-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="5edfb-127">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="5edfb-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="5edfb-128">Listen Sie die ersten 10 Themen des Ereignisrasters (sofern vorhanden) in der Ressourcengruppe \` "MyResourceGroupName" auf, die den Anforderungen $odataFilter \` entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5edfb-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5edfb-129">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="5edfb-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5edfb-130">Um die nächste Seite(n) mit Themen zu erhalten, wird erwartet, dass der Benutzer die Seite(n) erneut aufruft Get-AzEventGridTopic ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="5edfb-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5edfb-131">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="5edfb-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="5edfb-132">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="5edfb-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="5edfb-133">Listen Sie alle Themen des Veranstaltungsrasters im Abonnement ohne Paginierung auf.</span><span class="sxs-lookup"><span data-stu-id="5edfb-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="5edfb-134">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="5edfb-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="5edfb-135">Listen Sie die ersten 10 Themen zum Veranstaltungsraster (sofern vorhanden) im Abonnement auf, die den Anforderungen $odataFilter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5edfb-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="5edfb-136">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="5edfb-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="5edfb-137">Um die nächste Seite(n) mit Themen zu erhalten, wird erwartet, dass der Benutzer die Seite(n) erneut aufruft Get-AzEventGridTopic ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="5edfb-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="5edfb-138">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="5edfb-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="5edfb-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5edfb-139">PARAMETERS</span></span>

### <span data-ttu-id="5edfb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edfb-140">-DefaultProfile</span></span>
<span data-ttu-id="5edfb-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5edfb-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5edfb-142">-Name</span><span class="sxs-lookup"><span data-stu-id="5edfb-142">-Name</span></span>
<span data-ttu-id="5edfb-143">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="5edfb-143">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edfb-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="5edfb-144">-NextLink</span></span>
<span data-ttu-id="5edfb-145">Der Link zur nächsten Seite der zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5edfb-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="5edfb-146">Dieser Wert wird mit dem ersten Aufruf des Get-AzEventGrid-Cmdlet-Aufrufs ermittelt, wenn noch weitere Ressourcen zur Abfrage verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5edfb-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edfb-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5edfb-147">-ODataQuery</span></span>
<span data-ttu-id="5edfb-148">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5edfb-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="5edfb-149">Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="5edfb-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edfb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5edfb-150">-ResourceGroupName</span></span>
<span data-ttu-id="5edfb-151">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5edfb-151">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edfb-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5edfb-152">-ResourceId</span></span>
<span data-ttu-id="5edfb-153">Ressourcenbezeichner, der das Thema "Veranstaltungsraster" darstellt.</span><span class="sxs-lookup"><span data-stu-id="5edfb-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="5edfb-154">-Top</span><span class="sxs-lookup"><span data-stu-id="5edfb-154">-Top</span></span>
<span data-ttu-id="5edfb-155">Die maximale Anzahl zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="5edfb-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="5edfb-156">Gültiger Wert zwischen 1 und 100.</span><span class="sxs-lookup"><span data-stu-id="5edfb-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="5edfb-157">Wenn der oberste Wert angegeben wird und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in "NextLink" abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edfb-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="5edfb-158">Wenn der oberste Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen auf einmal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5edfb-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5edfb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edfb-159">CommonParameters</span></span>
<span data-ttu-id="5edfb-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edfb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edfb-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5edfb-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edfb-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5edfb-162">INPUTS</span></span>

### <span data-ttu-id="5edfb-163">System.String</span><span class="sxs-lookup"><span data-stu-id="5edfb-163">System.String</span></span>

### <span data-ttu-id="5edfb-164">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5edfb-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5edfb-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5edfb-165">OUTPUTS</span></span>

### <span data-ttu-id="5edfb-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="5edfb-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="5edfb-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="5edfb-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="5edfb-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5edfb-168">NOTES</span></span>

## <span data-ttu-id="5edfb-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5edfb-169">RELATED LINKS</span></span>
