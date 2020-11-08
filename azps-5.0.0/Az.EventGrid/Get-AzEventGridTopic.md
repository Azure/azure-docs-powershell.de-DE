---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177670"
---
# <span data-ttu-id="d93ae-101">Get-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="d93ae-101">Get-AzEventGridTopic</span></span>

## <span data-ttu-id="d93ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d93ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d93ae-103">Ruft die Details eines Ereignis Raster Themas ab oder ruft eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d93ae-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

## <span data-ttu-id="d93ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d93ae-104">SYNTAX</span></span>

### <span data-ttu-id="d93ae-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d93ae-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93ae-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93ae-106">TopicNameParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93ae-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93ae-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93ae-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93ae-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d93ae-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d93ae-109">DESCRIPTION</span></span>
<span data-ttu-id="d93ae-110">Das Get-AzEventGridTopic-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Themas oder eine Liste aller Themen des Ereignis Rasters im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d93ae-110">The Get-AzEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="d93ae-111">Wenn der Name des Themas angegeben ist, werden die Details für ein einzelnes Ereignis Raster Thema zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d93ae-111">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="d93ae-112">Wenn der Name des Themas nicht angegeben wird, wird eine Liste der Themen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d93ae-112">If the topic name is not provided, a list of topics is returned.</span></span> <span data-ttu-id="d93ae-113">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="d93ae-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="d93ae-114">Wenn der obere Wert nicht angegeben oder $NULL ist, enthält die Liste alle themenelemente.</span><span class="sxs-lookup"><span data-stu-id="d93ae-114">If the Top value is not specified or $null, the list will contain all the topics items.</span></span> <span data-ttu-id="d93ae-115">Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="d93ae-116">Wenn noch weitere Themen verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite mit Themen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-116">If more topics are still available, the value in NextLink should be used in the next call to get the next page of topics.</span></span>
<span data-ttu-id="d93ae-117">Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="d93ae-118">Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d93ae-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="d93ae-119">Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="d93ae-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="d93ae-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d93ae-120">EXAMPLES</span></span>

### <span data-ttu-id="d93ae-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d93ae-121">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="d93ae-122">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d93ae-122">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d93ae-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d93ae-123">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="d93ae-124">Ruft die Details des Ereignis Rasters Topic \` THEMA1 hat \` in Resource Group \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d93ae-124">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d93ae-125">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d93ae-125">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="d93ae-126">Listen Sie alle Themen des Ereignis Rasters in der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung auf.</span><span class="sxs-lookup"><span data-stu-id="d93ae-126">List all the Event Grid topics in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="d93ae-127">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d93ae-127">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="d93ae-128">Listen Sie die ersten 10 Themen des Ereignis Rasters (sofern vorhanden) in der Ressourcengruppe \` MyResourceGroupName auf \` , die die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d93ae-128">List the first 10 Event Grid topics (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d93ae-129">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="d93ae-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d93ae-130">Um die nächste Seite (n) von Themen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridTopic erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d93ae-130">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d93ae-131">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="d93ae-131">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="d93ae-132">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="d93ae-132">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic
```

<span data-ttu-id="d93ae-133">Listen Sie alle Themen des Ereignis Rasters im Abonnement ohne Paginierung auf.</span><span class="sxs-lookup"><span data-stu-id="d93ae-133">List all the Event Grid topics in the subscription without pagination.</span></span>

### <span data-ttu-id="d93ae-134">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="d93ae-134">Example 6</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

<span data-ttu-id="d93ae-135">Listen Sie die ersten 10 Themen des Ereignis Rasters (sofern vorhanden) im Abonnement auf, das die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d93ae-135">List the first 10 Event Grid topics (if any) in the subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="d93ae-136">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="d93ae-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="d93ae-137">Um die nächste Seite (n) von Themen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridTopic erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d93ae-137">In order to get next page(s) of topics, user is expected to re-call Get-AzEventGridTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="d93ae-138">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="d93ae-138">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="d93ae-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="d93ae-139">PARAMETERS</span></span>

### <span data-ttu-id="d93ae-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93ae-140">-DefaultProfile</span></span>
<span data-ttu-id="d93ae-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d93ae-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d93ae-142">-Name</span><span class="sxs-lookup"><span data-stu-id="d93ae-142">-Name</span></span>
<span data-ttu-id="d93ae-143">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="d93ae-143">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="d93ae-144">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="d93ae-144">-NextLink</span></span>
<span data-ttu-id="d93ae-145">Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-145">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="d93ae-146">Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="d93ae-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d93ae-147">-ODataQuery</span></span>
<span data-ttu-id="d93ae-148">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d93ae-148">The OData query used for filtering the list results.</span></span> <span data-ttu-id="d93ae-149">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="d93ae-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="d93ae-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93ae-150">-ResourceGroupName</span></span>
<span data-ttu-id="d93ae-151">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d93ae-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="d93ae-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d93ae-152">-ResourceId</span></span>
<span data-ttu-id="d93ae-153">Ressourcenbezeichner, der das Thema des Ereignis Rasters darstellt.</span><span class="sxs-lookup"><span data-stu-id="d93ae-153">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d93ae-154">-Top</span><span class="sxs-lookup"><span data-stu-id="d93ae-154">-Top</span></span>
<span data-ttu-id="d93ae-155">Die maximale Anzahl von Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d93ae-155">The maximum number of resources to be obtained.</span></span> <span data-ttu-id="d93ae-156">Gültiger Wert ist zwischen 1 und 100.</span><span class="sxs-lookup"><span data-stu-id="d93ae-156">Valid value is between 1 and 100.</span></span> <span data-ttu-id="d93ae-157">Wenn Top-Wert angegeben ist und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in Nextlink abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d93ae-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span> <span data-ttu-id="d93ae-158">Wenn der obere Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen gleichzeitig zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d93ae-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

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

### <span data-ttu-id="d93ae-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93ae-159">CommonParameters</span></span>
<span data-ttu-id="d93ae-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93ae-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93ae-161">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d93ae-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93ae-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d93ae-162">INPUTS</span></span>

### <span data-ttu-id="d93ae-163">System. String</span><span class="sxs-lookup"><span data-stu-id="d93ae-163">System.String</span></span>

### <span data-ttu-id="d93ae-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d93ae-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d93ae-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d93ae-165">OUTPUTS</span></span>

### <span data-ttu-id="d93ae-166">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="d93ae-166">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="d93ae-167">Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="d93ae-167">Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance</span></span>

## <span data-ttu-id="d93ae-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="d93ae-168">NOTES</span></span>

## <span data-ttu-id="d93ae-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d93ae-169">RELATED LINKS</span></span>
