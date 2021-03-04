---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 053c9a503b6cb7d3833d214208ae7fe6bd60fe45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934963"
---
# <span data-ttu-id="72f89-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="72f89-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="72f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f89-102">SYNOPSIS</span></span>
<span data-ttu-id="72f89-103">Ruft die Details eines Themas zu einer Event Grid-Domäne ab, oder ruft eine Liste aller Themen für Ereignisrasterdomänen unter einer bestimmten Event Grid-Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="72f89-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="72f89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72f89-104">SYNTAX</span></span>

### <span data-ttu-id="72f89-105">DomainTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="72f89-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72f89-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f89-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72f89-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="72f89-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f89-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72f89-108">DESCRIPTION</span></span>
<span data-ttu-id="72f89-109">Das Get-AzEventGridDomainTopic-Cmdlet ruft entweder die Details eines angegebenen Themas "Ereignisrasterdomäne" oder eine Liste aller Themen der Ereignisrasterdomäne unter einer bestimmten Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="72f89-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="72f89-110">Wenn der Domänenthemaname angegeben wird, werden die Details eines einzelnen Themas "Ereignisrasterdomäne" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72f89-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="72f89-111">Wenn der Domänenthemaname nicht angegeben wird, wird eine Liste der Domänenthemen unter dem angegebenen Domänennamen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="72f89-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="72f89-112">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter Top gesteuert.</span><span class="sxs-lookup"><span data-stu-id="72f89-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="72f89-113">Wenn der Oberste Wert nicht angegeben oder nicht $null, enthält die Liste alle Domänenthemenelemente.</span><span class="sxs-lookup"><span data-stu-id="72f89-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="72f89-114">Andernfalls gibt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="72f89-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="72f89-115">Wenn noch weitere Domänenthemen verfügbar sind, sollte der Wert in NextLink im nächsten Aufruf verwendet werden, um die nächste Seite mit Domänenthemen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="72f89-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="72f89-116">Schließlich wird der Parameter ODataQuery zum Filtern der Suchergebnisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="72f89-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="72f89-117">Die Filterabfrage folgt der #A0 nur mit der Name-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="72f89-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="72f89-118">Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.</span><span class="sxs-lookup"><span data-stu-id="72f89-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="72f89-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72f89-119">EXAMPLES</span></span>

### <span data-ttu-id="72f89-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="72f89-120">Example 1</span></span>

<span data-ttu-id="72f89-121">Ruft in der Ressourcengruppe MyResourceGroupName die Details des Themas \` "Ereignisrasterdomäne" DomainTopic1 unter \` Ereignisrasterdomäne \` Domäne1 \` \` \` ab.</span><span class="sxs-lookup"><span data-stu-id="72f89-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="72f89-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="72f89-122">Example 2</span></span>

<span data-ttu-id="72f89-123">Ruft die Details des Themas "Ereignisrasterdomäne" \` DomainTopic1 unter \` Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName mit \` der Option ResourceId ab.</span><span class="sxs-lookup"><span data-stu-id="72f89-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="72f89-124">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="72f89-124">Example 3</span></span>

<span data-ttu-id="72f89-125">Listen Sie alle Themen der Ereignisrasterdomäne unter Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName ohne Paginierung auf (alle Ergebnisse werden in einem \` Einzigen Schuss zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="72f89-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="72f89-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="72f89-126">Example 4</span></span>

<span data-ttu-id="72f89-127">Listen Sie alle Themen der Ereignisrasterdomäne unter Ereignisrasterdomäne Domäne1 in der Ressourcengruppe \` \` \` MyResourceGroupName ohne Paginierung auf (alle Ergebnisse werden auf einen Schlag zurückgegeben) mithilfe der Option \` ResourceId</span><span class="sxs-lookup"><span data-stu-id="72f89-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="72f89-128">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="72f89-128">Example 5</span></span>

<span data-ttu-id="72f89-129">Listen Sie die Domänenthemen des Ereignisrasters (falls vorhanden) unter Domäne1 in der Ressourcengruppe \` \` MyResourceGroupName auf, die die Themen $odataFilter Abfrage \` 10 Domänen gleichzeitig \` erfüllen.</span><span class="sxs-lookup"><span data-stu-id="72f89-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="72f89-130">Wenn weitere Ergebnisse verfügbar sind, wird $result. NextLink wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="72f89-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="72f89-131">Um die nächsten Seite(n) mit Domänenthemen zu erhalten, wird erwartet, dass der Benutzer erneut Get-AzEventGridDomainTopic aufruft und das Ergebnis verwendet. NextLink, der aus dem vorherigen Aufruf ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="72f89-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="72f89-132">Der Anrufer sollte beim Ergebnis beenden. NextLink wird $null.</span><span class="sxs-lookup"><span data-stu-id="72f89-132">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## <span data-ttu-id="72f89-133">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="72f89-133">PARAMETERS</span></span>

### <span data-ttu-id="72f89-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f89-134">-DefaultProfile</span></span>
<span data-ttu-id="72f89-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72f89-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72f89-136">-DomainName</span><span class="sxs-lookup"><span data-stu-id="72f89-136">-DomainName</span></span>
<span data-ttu-id="72f89-137">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="72f89-137">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-138">-Name</span><span class="sxs-lookup"><span data-stu-id="72f89-138">-Name</span></span>
<span data-ttu-id="72f89-139">Name des Themas "EventGrid-Domäne".</span><span class="sxs-lookup"><span data-stu-id="72f89-139">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-140">-NextLink</span><span class="sxs-lookup"><span data-stu-id="72f89-140">-NextLink</span></span>
<span data-ttu-id="72f89-141">Der Link für die nächste Seite der zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="72f89-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="72f89-142">Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf ermittelt, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="72f89-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="72f89-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="72f89-143">-ODataQuery</span></span>
<span data-ttu-id="72f89-144">Die zum Filtern der Listenergebnisse verwendete OData-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="72f89-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="72f89-145">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.</span><span class="sxs-lookup"><span data-stu-id="72f89-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f89-146">-ResourceGroupName</span></span>
<span data-ttu-id="72f89-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="72f89-147">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72f89-148">-ResourceId</span></span>
<span data-ttu-id="72f89-149">Ressourcenbezeichner, der das Thema "Event Grid Domain" oder "Grid Domain Topic" darstellt.</span><span class="sxs-lookup"><span data-stu-id="72f89-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-150">-Top</span><span class="sxs-lookup"><span data-stu-id="72f89-150">-Top</span></span>
<span data-ttu-id="72f89-151">Die zum Filtern der Listenergebnisse verwendete OData-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="72f89-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="72f89-152">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, Eq (für gleich), ne (für nicht gleich), UND, ODER und NICHT.</span><span class="sxs-lookup"><span data-stu-id="72f89-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72f89-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f89-153">CommonParameters</span></span>
<span data-ttu-id="72f89-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f89-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f89-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72f89-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f89-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72f89-156">INPUTS</span></span>

### <span data-ttu-id="72f89-157">System.String</span><span class="sxs-lookup"><span data-stu-id="72f89-157">System.String</span></span>

### <span data-ttu-id="72f89-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="72f89-158">System.Int32</span></span>

## <span data-ttu-id="72f89-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72f89-159">OUTPUTS</span></span>

### <span data-ttu-id="72f89-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="72f89-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="72f89-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="72f89-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="72f89-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="72f89-162">NOTES</span></span>

## <span data-ttu-id="72f89-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="72f89-163">RELATED LINKS</span></span>
