---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: 467b7141735cdce31bbdcf964e058f892238ec1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376829"
---
# <span data-ttu-id="63255-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="63255-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="63255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63255-102">SYNOPSIS</span></span>
<span data-ttu-id="63255-103">Ruft die Details einer Ereignisrasterdomäne oder eine Liste aller Ereignisrasterdomänen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="63255-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="63255-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63255-104">SYNTAX</span></span>

### <span data-ttu-id="63255-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63255-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63255-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="63255-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63255-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="63255-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63255-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="63255-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63255-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63255-109">DESCRIPTION</span></span>
<span data-ttu-id="63255-110">Das Get-AzEventGridDomain-Cmdlet ruft entweder die Details einer angegebenen "Event Grid"-Domäne oder eine Liste aller Event Grid-Domänen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="63255-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="63255-111">Wenn der Domänenname angegeben wird, werden die Details einer einzelnen Ereignisrasterdomäne zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63255-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="63255-112">Wenn der Domänenname nicht angegeben wird, wird eine Liste der Domänen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63255-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="63255-113">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter "Top" gesteuert.</span><span class="sxs-lookup"><span data-stu-id="63255-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="63255-114">Wenn der Spitzenwert nicht angegeben oder nicht $null, enthält die Liste alle Domänenelemente, die auf einmal zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="63255-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="63255-115">Andernfalls gibt "Top" die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63255-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="63255-116">Wenn noch weitere Domänen verfügbar sind, sollte der Wert in "NextLink" beim nächsten Aufruf verwendet werden, um die nächste Seite mit Domänen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="63255-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="63255-117">Schließlich wird der Parameter "ODataQuery" zum Filtern der Suchergebnisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="63255-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="63255-118">Die Filterabfrage folgt der #A0 nur mit der Eigenschaft "Name".</span><span class="sxs-lookup"><span data-stu-id="63255-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="63255-119">Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="63255-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="63255-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63255-120">EXAMPLES</span></span>

### <span data-ttu-id="63255-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63255-121">Example 1</span></span>

<span data-ttu-id="63255-122">Ruft die Details von "Event Grid \` \` Domain1" in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="63255-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="63255-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="63255-123">Example 2</span></span>

<span data-ttu-id="63255-124">Ruft die Details der Ereignisrasterdomäne \` "Domäne1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` mithilfe der Option "ResourceId" ab.</span><span class="sxs-lookup"><span data-stu-id="63255-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}
```

### <span data-ttu-id="63255-125">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="63255-125">Example 3</span></span>

<span data-ttu-id="63255-126">Auflisten aller Domänen des Ereignisrasters in der Ressourcengruppe \` "MyResourceGroupName" ohne Paginierung (alle Domänen werden \` in einem Foto zurückgegeben)</span><span class="sxs-lookup"><span data-stu-id="63255-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain -ResourceGroup MyResourceGroupName
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="63255-127">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="63255-127">Example 4</span></span>

<span data-ttu-id="63255-128">Listen Sie die Ereignisrasterdomänen (sofern vorhanden) in der Ressourcengruppe "MyResourceGroupName" auf, die die $odataFilter Abfrage \` \` 10 Domänen gleichzeitig erfüllt.</span><span class="sxs-lookup"><span data-stu-id="63255-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="63255-129">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="63255-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="63255-130">Damit die nächste Seite(n) mit Domänen angezeigt wird, wird erwartet, dass der Benutzer die Domäne erneut aufruft Get-AzEventGridDomain ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="63255-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="63255-131">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="63255-131">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domains is $Total"
```

### <span data-ttu-id="63255-132">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="63255-132">Example 5</span></span>

<span data-ttu-id="63255-133">Auflisten aller Event Grid-Domänen im Abonnement von Azure ohne Paginierung (alle Domänen werden in einem Foto zurückgegeben)</span><span class="sxs-lookup"><span data-stu-id="63255-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

```powershell
PS C:\> $result=Get-AzEventGridDomain
PS C:\> echo $result.PsDomainsList

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag1, Value1], [Tag2, Value2]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain2
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname1/providers/Microsoft.EventGrid/domains/domain2
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain2.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :

ResourceGroupName : MyResourceGroupName
DomainName        : Domain3
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname2/providers/Microsoft.EventGrid/domains/domain3
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain3.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Tag3, Value3], [Tag4, Value4]}

ResourceGroupName : MyResourceGroupName
DomainName        : Domain4
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/myresourcegroupname3/providers/Microsoft.EventGrid/domains/domain4
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain4.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="63255-134">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="63255-134">Example 6</span></span>

<span data-ttu-id="63255-135">Listen Sie die Ereignisrasterdomänen (sofern vorhanden) im Azure-Abonnement auf, die die $odataFilter 20 Domänen gleichzeitig erfüllen.</span><span class="sxs-lookup"><span data-stu-id="63255-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="63255-136">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="63255-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="63255-137">Damit die nächste Seite(n) mit Domänen angezeigt wird, wird erwartet, dass der Benutzer die Domäne erneut aufruft Get-AzEventGridDomain ergebnisse verwendet. NextLink, der aus dem vorherigen Anruf erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="63255-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="63255-138">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="63255-138">Caller should stop when result.NextLink becomes $null.</span></span>

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Contains(Name, 'ABCD')"
PS C:\> $result = Get-AzEventGridDomain -Top 20 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomain -NextLink $result.NextLink
        $total += $result.Count
    }
PS C:\> echo "Total number of domains is $Total"
```

## <span data-ttu-id="63255-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63255-139">PARAMETERS</span></span>

### <span data-ttu-id="63255-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63255-140">-DefaultProfile</span></span>
<span data-ttu-id="63255-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63255-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63255-142">-Name</span><span class="sxs-lookup"><span data-stu-id="63255-142">-Name</span></span>
<span data-ttu-id="63255-143">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="63255-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63255-144">-NextLink</span><span class="sxs-lookup"><span data-stu-id="63255-144">-NextLink</span></span>
<span data-ttu-id="63255-145">Der Link zur nächsten Seite der zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="63255-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="63255-146">Dieser Wert wird mit dem ersten Aufruf des Get-AzEventGrid-Cmdlet-Aufrufs ermittelt, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="63255-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="63255-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="63255-147">-ODataQuery</span></span>
<span data-ttu-id="63255-148">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="63255-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="63255-149">Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="63255-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63255-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63255-150">-ResourceGroupName</span></span>
<span data-ttu-id="63255-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63255-151">The name of the resource group.</span></span>

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
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63255-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63255-152">-ResourceId</span></span>
<span data-ttu-id="63255-153">Ressourcenbezeichner, der die "Event Grid Domain" darstellt.</span><span class="sxs-lookup"><span data-stu-id="63255-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="63255-154">-Top</span><span class="sxs-lookup"><span data-stu-id="63255-154">-Top</span></span>
<span data-ttu-id="63255-155">Die maximale Anzahl zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="63255-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="63255-156">Gültiger Wert zwischen 1 und 100.</span><span class="sxs-lookup"><span data-stu-id="63255-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="63255-157">Wenn der oberste Wert angegeben wird und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in "NextLink" abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63255-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="63255-158">Wenn der Oberste Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen auf einmal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63255-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63255-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63255-159">CommonParameters</span></span>
<span data-ttu-id="63255-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63255-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63255-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63255-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63255-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63255-162">INPUTS</span></span>

### <span data-ttu-id="63255-163">System.String</span><span class="sxs-lookup"><span data-stu-id="63255-163">System.String</span></span>

## <span data-ttu-id="63255-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63255-164">OUTPUTS</span></span>

### <span data-ttu-id="63255-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="63255-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="63255-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="63255-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="63255-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="63255-167">NOTES</span></span>

## <span data-ttu-id="63255-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="63255-168">RELATED LINKS</span></span>
