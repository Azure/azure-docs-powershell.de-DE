---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 0303ea7841a187002e4848c74ca656eeea970dbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175681"
---
# <span data-ttu-id="6cf09-101">Get-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6cf09-101">Get-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="6cf09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cf09-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf09-103">Ruft die Details des Themas einer Ereignis Raster Domäne ab oder ruft eine Liste aller Themen der Ereignis Raster Domäne unter einer bestimmten Ereignis Raster Domäne im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6cf09-103">Gets the details of an Event Grid domain topic, or gets a list of all Event Grid domain topics under specific Event Grid domain in the current Azure subscription.</span></span>

## <span data-ttu-id="6cf09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">SYNTAX</span></span>

### <span data-ttu-id="6cf09-105">DomainTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">DomainTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cf09-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">ResourceIdDomainTopicParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cf09-107">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cf09-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">DESCRIPTION</span></span>
<span data-ttu-id="6cf09-109">Das Get-AzEventGridDomainTopic-Cmdlet ruft entweder die Details eines angegebenen Event Grid-Domänen Themas ab oder eine Liste aller Themen der Ereignis Raster Domäne unter einer bestimmten Domäne im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">The Get-AzEventGridDomainTopic cmdlet gets either the details of a specified Event Grid domain topic, or a list of all Event Grid domain topics under a specific domain in the current Azure subscription.</span></span>
<span data-ttu-id="6cf09-110">Wenn der Name des Domänen Themas angegeben wird, werden die Details zu einem einzelnen Ereignis Raster-Domänen Thema zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">If the domain topic name is provided, the details of a single Event Grid domain topic is returned.</span></span>
<span data-ttu-id="6cf09-111">Wenn der Name des Domänen Themas nicht angegeben wird, wird eine Liste der Domänen Themen unter dem angegebenen Domänennamen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">If the domain topic name is not provided, a list of domain topics under the specified domain name is returned.</span></span> <span data-ttu-id="6cf09-112">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="6cf09-113">Wenn der oberste Wert nicht angegeben oder $NULL ist, enthält die Liste alle Domänen themenelemente.</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">If the Top value is not specified or $null, the list will contain all the domain topics items.</span></span> <span data-ttu-id="6cf09-114">Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="6cf09-115">Wenn noch weitere Domänen Themen verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite der Domänen Themen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">If more domain topics are still available, the value in NextLink should be used in the next call to get the next page of domain topics.</span></span>
<span data-ttu-id="6cf09-116">Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-116">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="6cf09-117">Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cf09-117">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="6cf09-118">Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="6cf09-118">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="6cf09-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cf09-119">EXAMPLES</span></span>

### <span data-ttu-id="6cf09-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cf09-120">Example 1</span></span>

<span data-ttu-id="6cf09-121">Ruft die Details der Ereignis Raster Domäne Topic \` DomainTopic1 \` unter Ereignis Raster-Domänen \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="6cf09-121">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6cf09-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6cf09-122">Example 2</span></span>

<span data-ttu-id="6cf09-123">Ruft die Details der Ereignis Raster Domäne Topic \` DomainTopic1 \` unter Ereignis Raster \` -Domänen domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` mithilfe der Option "Ressourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="6cf09-123">Gets the details of Event Grid domain topic \`DomainTopic1\` under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using the ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### <span data-ttu-id="6cf09-124">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6cf09-124">Example 3</span></span>

<span data-ttu-id="6cf09-125">Listen Sie alle Themen der Ereignis Raster Domäne unter Ereignis Raster \` -Domänen domain1 \` in der Ressourcengruppen \` \` -MyResourceGroupName ohne Paginierung auf (alle Ergebnisse werden in einem Schuß zurückgegeben).</span><span class="sxs-lookup"><span data-stu-id="6cf09-125">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot).</span></span>

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

### <span data-ttu-id="6cf09-126">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="6cf09-126">Example 4</span></span>

<span data-ttu-id="6cf09-127">Auflisten aller Themen der Ereignis Raster Domäne unter Ereignis \` Raster \` -Domänen domain1 in der Ressourcengruppen \` \` -MyResourceGroupName ohne Paginierung (alle Ergebnisse werden in einem einzigen shot zurückgegeben) mithilfe der Option "Resourcen-Option"</span><span class="sxs-lookup"><span data-stu-id="6cf09-127">List all the Event Grid domain topics under Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` without pagination (all results are returned in one shot) using ResourceId option</span></span>

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

### <span data-ttu-id="6cf09-128">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="6cf09-128">Example 5</span></span>

<span data-ttu-id="6cf09-129">Listen Sie die Themen der Ereignis Raster Domäne (sofern vorhanden) Unterdomänen \` domain1 \` in der Ressourcengruppen- \` MyResourceGroupName auf, die \` den $odataFilter Abfrage 10 Domänen Themen gleichzeitig entspricht.</span><span class="sxs-lookup"><span data-stu-id="6cf09-129">List the Event Grid domain topics (if any) under domain \`Domain1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domain topics at a time.</span></span> <span data-ttu-id="6cf09-130">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="6cf09-130">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="6cf09-131">Um die nächste Seite (n) der Domänen Themen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridDomainTopic erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6cf09-131">In order to get next page(s) of domain topics, user is expected to re-call Get-AzEventGridDomainTopic and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="6cf09-132">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="6cf09-132">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="6cf09-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cf09-133">PARAMETERS</span></span>

### <span data-ttu-id="6cf09-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf09-134">-DefaultProfile</span></span>
<span data-ttu-id="6cf09-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cf09-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cf09-136">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="6cf09-136">-DomainName</span></span>
<span data-ttu-id="6cf09-137">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="6cf09-137">EventGrid domain name.</span></span>

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

### <span data-ttu-id="6cf09-138">-Name</span><span class="sxs-lookup"><span data-stu-id="6cf09-138">-Name</span></span>
<span data-ttu-id="6cf09-139">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="6cf09-139">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="6cf09-140">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="6cf09-140">-NextLink</span></span>
<span data-ttu-id="6cf09-141">Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-141">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="6cf09-142">Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6cf09-142">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="6cf09-143">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6cf09-143">-ODataQuery</span></span>
<span data-ttu-id="6cf09-144">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cf09-144">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6cf09-145">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="6cf09-145">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="6cf09-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cf09-146">-ResourceGroupName</span></span>
<span data-ttu-id="6cf09-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6cf09-147">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cf09-148">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6cf09-148">-ResourceId</span></span>
<span data-ttu-id="6cf09-149">Ressourcenbezeichner, der das Thema "Ereignis Raster Domäne" oder "Raster Domäne" darstellt.</span><span class="sxs-lookup"><span data-stu-id="6cf09-149">Resource Identifier representing the Event Grid Domain or Grid Domain Topic.</span></span>

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

### <span data-ttu-id="6cf09-150">-Top</span><span class="sxs-lookup"><span data-stu-id="6cf09-150">-Top</span></span>
<span data-ttu-id="6cf09-151">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cf09-151">The OData query used for filtering the list results.</span></span> <span data-ttu-id="6cf09-152">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="6cf09-152">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="6cf09-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf09-153">CommonParameters</span></span>
<span data-ttu-id="6cf09-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf09-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf09-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf09-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf09-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cf09-156">INPUTS</span></span>

### <span data-ttu-id="6cf09-157">System. String</span><span class="sxs-lookup"><span data-stu-id="6cf09-157">System.String</span></span>

### <span data-ttu-id="6cf09-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6cf09-158">System.Int32</span></span>

## <span data-ttu-id="6cf09-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cf09-159">OUTPUTS</span></span>

### <span data-ttu-id="6cf09-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6cf09-160">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="6cf09-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span><span class="sxs-lookup"><span data-stu-id="6cf09-161">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance</span></span>

## <span data-ttu-id="6cf09-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cf09-162">NOTES</span></span>

## <span data-ttu-id="6cf09-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cf09-163">RELATED LINKS</span></span>
