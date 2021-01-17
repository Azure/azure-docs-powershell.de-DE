---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 587e42ac4c9f318ff46381fdef5b09fa7ce55b63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376801"
---
# <span data-ttu-id="ebb43-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ebb43-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="ebb43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb43-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb43-103">Ruft die Details eines Ereignisabonnements ab oder eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebb43-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="ebb43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebb43-104">SYNTAX</span></span>

### <span data-ttu-id="ebb43-105">EventSubscriptionTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ebb43-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb43-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebb43-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb43-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebb43-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebb43-113">DESCRIPTION</span></span>
<span data-ttu-id="ebb43-114">Das Get-AzEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Event Grid-Abonnements oder eine Liste aller Event Grid-Abonnements im aktuellen Abonnement oder der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ebb43-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="ebb43-115">Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Event Grid-Abonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ebb43-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="ebb43-116">Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ebb43-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="ebb43-117">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Parameter "Top" gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ebb43-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="ebb43-118">Wenn der Spitzenwert nicht angegeben oder nicht $null, enthält die Liste alle Ereignisabonnementelemente.</span><span class="sxs-lookup"><span data-stu-id="ebb43-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="ebb43-119">Andernfalls gibt "Top" die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ebb43-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="ebb43-120">Wenn noch weitere Ereignisabonnements verfügbar sind, sollte der Wert in "NextLink" beim nächsten Aufruf verwendet werden, um die nächste Seite mit Ereignisabonnements zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ebb43-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="ebb43-121">Schließlich wird der Parameter "ODataQuery" zum Filtern der Suchergebnisse verwendet.</span><span class="sxs-lookup"><span data-stu-id="ebb43-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="ebb43-122">Die Filterabfrage folgt der #A0 nur mit der Eigenschaft "Name".</span><span class="sxs-lookup"><span data-stu-id="ebb43-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="ebb43-123">Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="ebb43-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="ebb43-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebb43-124">EXAMPLES</span></span>

### <span data-ttu-id="ebb43-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebb43-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ebb43-126">Ruft die Details des Ereignisabonnements "EventSubscription1" ab, das für \` \` \` Thema1 in \` der Ressourcengruppe \` "MyResourceGroupName" erstellt \` wurde.</span><span class="sxs-lookup"><span data-stu-id="ebb43-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ebb43-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ebb43-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="ebb43-128">Ruft die Details des Ereignisabonnements "EventSubscription1" ab, das für Thema1 in der Ressourcengruppe \` \` \` \` "MyResourceGroupName" erstellt wurde, einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein \` \` webhookbasiertes Ereignisabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="ebb43-129">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ebb43-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="ebb43-130">Hier erhalten Sie eine Liste aller Ereignisabonnements, die für "Topic1" in der Ressourcengruppe \` \` \` "MyResourceGroupName" ohne \` Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ebb43-131">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ebb43-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-132">Listen Sie die ersten 10 Ereignisabonnements (sofern vorhanden) auf, die für Thema1 in der Ressourcengruppe \` \` \` "MyResourceGroupName" erstellt wurden, die die $odataFilter \` erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ebb43-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-133">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-134">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-135">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-136">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ebb43-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ebb43-137">Ruft die Details des Ereignisabonnements \` "EventSubscription1" ab, das \` für die Ressourcengruppe \` "MyResourceGroupName" erstellt \` wurde.</span><span class="sxs-lookup"><span data-stu-id="ebb43-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ebb43-138">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="ebb43-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ebb43-139">Ruft die Details des Ereignisabonnements "EventSubscription1" ab, das für das aktuell ausgewählte \` \` Azure-Abonnement erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ebb43-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="ebb43-140">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="ebb43-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ebb43-141">Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe \` "MyResourceGroupName" ohne \` Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="ebb43-142">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="ebb43-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-143">Listen Sie die ersten 5 Ereignisabonnements (sofern vorhanden) auf, die unter der Ressourcengruppe \` "MyResourceGroupName" erstellt wurden und den Anforderungen der \` $odataFilter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ebb43-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-144">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-145">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-146">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-147">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="ebb43-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="ebb43-148">Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Abonnement ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="ebb43-149">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="ebb43-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-150">Listen Sie die ersten 15 globalen Ereignisabonnements (sofern vorhanden) auf, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden, das die Anforderungen $odataFilter erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-151">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-152">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-153">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-154">Beispiel 11</span><span class="sxs-lookup"><span data-stu-id="ebb43-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="ebb43-155">Ruft die Liste aller regionalen Ereignisabonnements ab, die unter der Ressourcengruppe "MyResourceGroupName" am angegebenen Speicherort \` "westus2" erstellt wurden, ohne \` \` \` Paginierung.</span><span class="sxs-lookup"><span data-stu-id="ebb43-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="ebb43-156">Beispiel 12</span><span class="sxs-lookup"><span data-stu-id="ebb43-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-157">Listen Sie die ersten 15 regionalen Ereignisabonnements (sofern vorhanden) auf, die unter der Ressourcengruppe "MyResourceGroupName" erstellt wurden, am angegebenen Speicherort \` \` \` "westus2", der die $odataFilter \` erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-158">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-159">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-160">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-161">Beispiel 13</span><span class="sxs-lookup"><span data-stu-id="ebb43-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="ebb43-162">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="ebb43-163">Beispiel 14</span><span class="sxs-lookup"><span data-stu-id="ebb43-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-164">Listet die ersten 25 Ereignisabonnements (sofern vorhanden) auf, die für den angegebenen EventHub-Namespace erstellt wurden, der die $odataFilter erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-165">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-166">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-167">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-168">Beispiel 15</span><span class="sxs-lookup"><span data-stu-id="ebb43-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="ebb43-169">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Thementyp (EventHub-Namespaces) am angegebenen Speicherort ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="ebb43-170">Beispiel 16</span><span class="sxs-lookup"><span data-stu-id="ebb43-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-171">Listen Sie die ersten 15 Ereignisabonnements (sofern vorhanden) auf, die für den angegebenen Thementyp (EventHub-Namespaces) erstellt wurden, am angegebenen Speicherort, der den Anforderungen $odataFilter entspricht.</span><span class="sxs-lookup"><span data-stu-id="ebb43-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-172">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-173">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-174">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="ebb43-175">Beispiel 17</span><span class="sxs-lookup"><span data-stu-id="ebb43-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="ebb43-176">Ruft die Liste aller Ereignisabonnements ab, die für die spezifische Ressourcengruppe ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="ebb43-177">Beispiel 18</span><span class="sxs-lookup"><span data-stu-id="ebb43-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="ebb43-178">Listen Sie die ersten 100 Ereignisabonnements (sofern vorhanden) auf, die für die spezifische Ressourcengruppe erstellt wurden, die die $odataFilter erfüllt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="ebb43-179">Wenn weitere Ergebnisse verfügbar sind, wird $result. "NextLink" wird nicht $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="ebb43-180">Um die nächste Seite(n) mit Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer das Ereignis erneut aufruft Get-AzEventGridSubscription und das Ergebnis verwendet. NextLink aus dem vorherigen Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebb43-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="ebb43-181">Der Anrufer sollte beendet werden, wenn das Ergebnis vor sich geht. "NextLink" wird $null.</span><span class="sxs-lookup"><span data-stu-id="ebb43-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="ebb43-182">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebb43-182">PARAMETERS</span></span>

### <span data-ttu-id="ebb43-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb43-183">-DefaultProfile</span></span>
<span data-ttu-id="ebb43-184">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ebb43-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebb43-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ebb43-185">-DomainInputObject</span></span>
<span data-ttu-id="ebb43-186">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-186">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-187">-DomainName</span><span class="sxs-lookup"><span data-stu-id="ebb43-187">-DomainName</span></span>
<span data-ttu-id="ebb43-188">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="ebb43-188">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ebb43-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="ebb43-190">EventGrid Domain Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-190">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ebb43-191">-DomainTopicName</span></span>
<span data-ttu-id="ebb43-192">Name des Themas "EventGrid".</span><span class="sxs-lookup"><span data-stu-id="ebb43-192">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ebb43-193">-EventSubscriptionName</span></span>
<span data-ttu-id="ebb43-194">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="ebb43-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="ebb43-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="ebb43-196">Geben Sie die vollständige Endpunkt-URL des Ziels des Ereignisabonnements an.</span><span class="sxs-lookup"><span data-stu-id="ebb43-196">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-197">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebb43-197">-InputObject</span></span>
<span data-ttu-id="ebb43-198">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ebb43-198">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-199">-Location</span><span class="sxs-lookup"><span data-stu-id="ebb43-199">-Location</span></span>
<span data-ttu-id="ebb43-200">Position</span><span class="sxs-lookup"><span data-stu-id="ebb43-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-201">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ebb43-201">-NextLink</span></span>
<span data-ttu-id="ebb43-202">Der Link zur nächsten Seite der zu erhaltende Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ebb43-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="ebb43-203">Dieser Wert wird mit dem ersten Aufruf des Get-AzEventGrid-Cmdlet-Aufrufs ermittelt, wenn noch weitere Ressourcen zur Abfrage verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ebb43-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="ebb43-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ebb43-204">-ODataQuery</span></span>
<span data-ttu-id="ebb43-205">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebb43-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ebb43-206">Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="ebb43-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb43-207">-ResourceGroupName</span></span>
<span data-ttu-id="ebb43-208">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ebb43-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-209">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebb43-209">-ResourceId</span></span>
<span data-ttu-id="ebb43-210">Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="ebb43-210">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-211">-Top</span><span class="sxs-lookup"><span data-stu-id="ebb43-211">-Top</span></span>
<span data-ttu-id="ebb43-212">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebb43-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="ebb43-213">Filtern ist derzeit nur für die Eigenschaft "Name" zulässig. Zu den unterstützten Vorgängen gehören: CONTAINS, eq (for equal), ne (for not equal), AND, OR und NOT.</span><span class="sxs-lookup"><span data-stu-id="ebb43-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-214">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ebb43-214">-TopicName</span></span>
<span data-ttu-id="ebb43-215">Name des EventGrid-Themas.</span><span class="sxs-lookup"><span data-stu-id="ebb43-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="ebb43-216">-TopicTypeName</span></span>
<span data-ttu-id="ebb43-217">TopicType name</span><span class="sxs-lookup"><span data-stu-id="ebb43-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb43-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb43-218">CommonParameters</span></span>
<span data-ttu-id="ebb43-219">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb43-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb43-220">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebb43-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb43-221">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebb43-221">INPUTS</span></span>

### <span data-ttu-id="ebb43-222">System.String</span><span class="sxs-lookup"><span data-stu-id="ebb43-222">System.String</span></span>

### <span data-ttu-id="ebb43-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ebb43-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ebb43-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ebb43-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ebb43-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ebb43-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="ebb43-226">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ebb43-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ebb43-227">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebb43-227">OUTPUTS</span></span>

### <span data-ttu-id="ebb43-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="ebb43-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="ebb43-229">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ebb43-229">NOTES</span></span>

## <span data-ttu-id="ebb43-230">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ebb43-230">RELATED LINKS</span></span>
