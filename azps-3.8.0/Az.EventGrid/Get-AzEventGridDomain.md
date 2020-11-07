---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomain.md
ms.openlocfilehash: f2f3c3799ff16cdcc5f1091f8a66cb531cf46cc3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845624"
---
# <span data-ttu-id="e5ec2-101">Get-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e5ec2-101">Get-AzEventGridDomain</span></span>

## <span data-ttu-id="e5ec2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ec2-103">Ruft die Details einer Ereignis Raster Domäne ab oder ruft eine Liste aller Ereignis Raster Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-103">Gets the details of an Event Grid domain, or gets a list of all Event Grid domains in the current Azure subscription.</span></span>

## <span data-ttu-id="e5ec2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5ec2-104">SYNTAX</span></span>

### <span data-ttu-id="e5ec2-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5ec2-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomain [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ec2-106">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5ec2-106">DomainNameParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ec2-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5ec2-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomain [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5ec2-108">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5ec2-108">NextLinkParameterSet</span></span>
```
Get-AzEventGridDomain [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5ec2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5ec2-109">DESCRIPTION</span></span>
<span data-ttu-id="e5ec2-110">Das Get-AzEventGridDomain-Cmdlet ruft entweder die Details einer angegebenen Ereignis Raster Domäne oder eine Liste aller Ereignis Raster Domänen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-110">The Get-AzEventGridDomain cmdlet gets either the details of a specified Event Grid domain, or a list of all Event Grid domains in the current Azure subscription.</span></span>
<span data-ttu-id="e5ec2-111">Wenn der Domänenname bereitgestellt wird, werden die Details einer einzelnen Ereignis Raster Domäne zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-111">If the domain name is provided, the details of a single Event Grid domain is returned.</span></span>
<span data-ttu-id="e5ec2-112">Wenn der Domänenname nicht angegeben wird, wird eine Liste der Domänen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-112">If the domain name is not provided, a list of domains is returned.</span></span> <span data-ttu-id="e5ec2-113">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-113">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="e5ec2-114">Wenn der obere Wert nicht angegeben oder $NULL ist, enthält die Liste alle Domänen Elemente, die gleichzeitig zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-114">If the Top value is not specified or $null, the list will contain all the domains items returned at once.</span></span> <span data-ttu-id="e5ec2-115">Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-115">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="e5ec2-116">Wenn noch weitere Domänen verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite der Domänen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-116">If more domains are still available, the value in NextLink should be used in the next call to get the next page of domains.</span></span>
<span data-ttu-id="e5ec2-117">Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-117">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="e5ec2-118">Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-118">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="e5ec2-119">Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-119">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="e5ec2-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5ec2-120">EXAMPLES</span></span>

### <span data-ttu-id="e5ec2-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5ec2-121">Example 1</span></span>

<span data-ttu-id="e5ec2-122">Ruft die Details der Ereignis Raster-Domänen \` domain1 \` in der Ressourcengruppen \` -MyResourceGroupName ab \` .</span><span class="sxs-lookup"><span data-stu-id="e5ec2-122">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

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

### <span data-ttu-id="e5ec2-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5ec2-123">Example 2</span></span>

<span data-ttu-id="e5ec2-124">Ruft die Details der Ereignis Raster-Domänen \` domain1 \` in der Ressourcengruppen- \` MyResourceGroupName mit der Option "Ressourcen" auf \` .</span><span class="sxs-lookup"><span data-stu-id="e5ec2-124">Gets the details of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using ResourceId option.</span></span>

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

### <span data-ttu-id="e5ec2-125">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e5ec2-125">Example 3</span></span>

<span data-ttu-id="e5ec2-126">Auflisten aller Ereignis Raster Domänen in der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung (alle Domänen werden in einem einzigen shot zurückgegeben)</span><span class="sxs-lookup"><span data-stu-id="e5ec2-126">List all the Event Grid domains in resource group \`MyResourceGroupName\` without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="e5ec2-127">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="e5ec2-127">Example 4</span></span>

<span data-ttu-id="e5ec2-128">Listen Sie die Ereignis Raster Domänen (sofern vorhanden) in der Ressourcengruppe \` MyResourceGroupName \` auf, die den $odataFilter Abfrage 10 Domänen gleichzeitig entspricht.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-128">List the Event Grid domains (if any) in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query 10 domains at a time.</span></span> <span data-ttu-id="e5ec2-129">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-129">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="e5ec2-130">Um die nächste Seite (n) der Domänen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridDomain erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-130">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="e5ec2-131">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-131">Caller should stop when result.NextLink becomes $null.</span></span>

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

### <span data-ttu-id="e5ec2-132">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="e5ec2-132">Example 5</span></span>

<span data-ttu-id="e5ec2-133">Auflisten aller Ereignis Raster Domänen in Azure-Abonnement ohne Paginierung (alle Domänen werden in einem einzigen shot zurückgegeben)</span><span class="sxs-lookup"><span data-stu-id="e5ec2-133">List all the Event Grid domains in Azure Subscription without pagination (all domains are returned in one shot)</span></span>

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

### <span data-ttu-id="e5ec2-134">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="e5ec2-134">Example 6</span></span>

<span data-ttu-id="e5ec2-135">Listen Sie die Ereignis Raster Domänen (sofern vorhanden) in Azure-Abonnement auf, das die $odataFilter Abfrage 20 Domänen gleichzeitig erfüllt.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-135">List the Event Grid domains (if any) in Azure Subscription that satisfies the $odataFilter query 20 domains at a time.</span></span> <span data-ttu-id="e5ec2-136">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-136">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="e5ec2-137">Um die nächste Seite (n) der Domänen zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridDomain erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-137">In order to get next page(s) of domains, user is expected to re-call Get-AzEventGridDomain and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="e5ec2-138">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-138">Caller should stop when result.NextLink becomes $null.</span></span>

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

## <span data-ttu-id="e5ec2-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ec2-139">PARAMETERS</span></span>

### <span data-ttu-id="e5ec2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ec2-140">-DefaultProfile</span></span>
<span data-ttu-id="e5ec2-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5ec2-142">-Name</span><span class="sxs-lookup"><span data-stu-id="e5ec2-142">-Name</span></span>
<span data-ttu-id="e5ec2-143">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-143">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ec2-144">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="e5ec2-144">-NextLink</span></span>
<span data-ttu-id="e5ec2-145">Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-145">The link for the next page of resources to be obtained.</span></span>
<span data-ttu-id="e5ec2-146">Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-146">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ec2-147">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e5ec2-147">-ODataQuery</span></span>
<span data-ttu-id="e5ec2-148">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-148">The OData query used for filtering the list results.</span></span>
<span data-ttu-id="e5ec2-149">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-149">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ec2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ec2-150">-ResourceGroupName</span></span>
<span data-ttu-id="e5ec2-151">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ec2-152">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e5ec2-152">-ResourceId</span></span>
<span data-ttu-id="e5ec2-153">Der Ressourcenbezeichner, der die Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-153">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="e5ec2-154">-Top</span><span class="sxs-lookup"><span data-stu-id="e5ec2-154">-Top</span></span>
<span data-ttu-id="e5ec2-155">Die maximale Anzahl von Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-155">The maximum number of resources to be obtained.</span></span>
<span data-ttu-id="e5ec2-156">Gültiger Wert ist zwischen 1 und 100.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-156">Valid value is between 1 and 100.</span></span>
<span data-ttu-id="e5ec2-157">Wenn Top-Wert angegeben ist und weitere Ergebnisse weiterhin verfügbar sind, enthält das Ergebnis einen Link zur nächsten Seite, die in Nextlink abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-157">If top value is specified and more results are still available, the result will contain a link to the next page to be queried in NextLink.</span></span>
<span data-ttu-id="e5ec2-158">Wenn der obere Wert nicht angegeben wird, wird die vollständige Liste der Ressourcen gleichzeitig zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-158">If the Top value is not specified, the full list of resources will be returned at once.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResourceGroupNameParameterSet, DomainNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5ec2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ec2-159">CommonParameters</span></span>
<span data-ttu-id="e5ec2-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ec2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ec2-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ec2-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ec2-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5ec2-162">INPUTS</span></span>

### <span data-ttu-id="e5ec2-163">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ec2-163">System.String</span></span>

## <span data-ttu-id="e5ec2-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5ec2-164">OUTPUTS</span></span>

### <span data-ttu-id="e5ec2-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="e5ec2-165">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="e5ec2-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span><span class="sxs-lookup"><span data-stu-id="e5ec2-166">Microsoft.Azure.Commands.EventGrid.Models.PSDomainListInstance</span></span>

## <span data-ttu-id="e5ec2-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5ec2-167">NOTES</span></span>

## <span data-ttu-id="e5ec2-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5ec2-168">RELATED LINKS</span></span>
