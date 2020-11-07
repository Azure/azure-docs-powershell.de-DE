---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651238"
---
# <span data-ttu-id="299cf-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="299cf-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="299cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="299cf-102">SYNOPSIS</span></span>
<span data-ttu-id="299cf-103">Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="299cf-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="299cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="299cf-104">SYNTAX</span></span>

### <span data-ttu-id="299cf-105">EventSubscriptionTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="299cf-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299cf-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="299cf-107">EventSubscriptionDomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-107">EventSubscriptionDomainNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299cf-108">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-108">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="299cf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-109">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299cf-110">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-110">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299cf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-111">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="299cf-112">NextLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="299cf-112">NextLinkParameterSet</span></span>
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="299cf-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="299cf-113">DESCRIPTION</span></span>
<span data-ttu-id="299cf-114">Das Get-AzEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="299cf-114">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="299cf-115">Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="299cf-115">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="299cf-116">Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="299cf-116">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span> <span data-ttu-id="299cf-117">Die Anzahl der in dieser Liste zurückgegebenen Elemente wird durch den Top-Parameter gesteuert.</span><span class="sxs-lookup"><span data-stu-id="299cf-117">The number of elements returned in this list is controlled by the Top parameter.</span></span> <span data-ttu-id="299cf-118">Wenn der obere Wert nicht angegeben oder $NULL ist, enthält die Liste alle Ereignisabonnement Elemente.</span><span class="sxs-lookup"><span data-stu-id="299cf-118">If the Top value is not specified or $null, the list will contain all the event subscription items.</span></span> <span data-ttu-id="299cf-119">Andernfalls zeigt Top die maximale Anzahl von Elementen an, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="299cf-119">Otherwise, Top will indicate the maximum number of elements to be returned in the list.</span></span>
<span data-ttu-id="299cf-120">Wenn noch weitere Ereignisabonnements verfügbar sind, sollte der Wert in Nextlink beim nächsten Aufruf verwendet werden, um die nächste Seite der Ereignisabonnements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="299cf-120">If more event subscriptions are still available, the value in NextLink should be used in the next call to get the next page of event subscriptions.</span></span>
<span data-ttu-id="299cf-121">Schließlich wird ODataQuery-Parameter verwendet, um die Filterung für die Suchergebnisse durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="299cf-121">Finally, ODataQuery parameter is used to perform filtering for the search results.</span></span> <span data-ttu-id="299cf-122">Die Filterabfrage folgt der OData-Syntax, wobei nur die Name-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="299cf-122">The filtering query follows OData syntax using the Name property only.</span></span> <span data-ttu-id="299cf-123">Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="299cf-123">The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

## <span data-ttu-id="299cf-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="299cf-124">EXAMPLES</span></span>

### <span data-ttu-id="299cf-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="299cf-125">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="299cf-126">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="299cf-126">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="299cf-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="299cf-127">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="299cf-128">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="299cf-128">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="299cf-129">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="299cf-129">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="299cf-130">Abrufen einer Liste aller Ereignisabonnements, die für Topic \` THEMA1 hat \` in der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-130">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="299cf-131">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="299cf-131">Example 4</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-132">Listen Sie die ersten 10 Ereignisabonnements (sofern vorhanden) auf, die für \` die Themen THEMA1 hat \` in der Ressourcengruppen-MyResourceGroupName erstellt wurden \` \` , die der $odataFilter Abfrage entspricht.</span><span class="sxs-lookup"><span data-stu-id="299cf-132">List the first 10 event subscriptions (if any) created for topic \`Topic1\` in resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-133">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-133">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-134">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-134">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-135">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-135">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-136">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="299cf-136">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="299cf-137">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .</span><span class="sxs-lookup"><span data-stu-id="299cf-137">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="299cf-138">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="299cf-138">Example 6</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="299cf-139">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-139">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="299cf-140">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="299cf-140">Example 7</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="299cf-141">Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe \` MyResourceGroupName \` ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-141">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\` without pagination.</span></span>

### <span data-ttu-id="299cf-142">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="299cf-142">Example 8</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-143">Listen Sie die ersten fünf Ereignisabonnements (sofern vorhanden) auf, die unter Ressourcengruppen-MyResourceGroupName erstellt wurden \` \` , die der $odataFilter Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="299cf-143">List the first 5 event subscriptions (if any) created under resource group \`MyResourceGroupName\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-144">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-144">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-145">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-145">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-146">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-146">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-147">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="299cf-147">Example 9</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="299cf-148">Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-148">Gets the list of all global event subscriptions created under the currently selected Azure subscription without pagination.</span></span>

### <span data-ttu-id="299cf-149">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="299cf-149">Example 10</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-150">Listen Sie die ersten 15 globalen Ereignisabonnements (sofern vorhanden) auf, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden, das die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="299cf-150">List the first 15 global event subscriptions (if any) created under the currently selected Azure subscription that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-151">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-151">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-152">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-152">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-153">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-153">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-154">Beispiel 11</span><span class="sxs-lookup"><span data-stu-id="299cf-154">Example 11</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="299cf-155">Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcen \` Gruppen \` -MyResourceGroupName an der angegebenen Position \` westus2 \` ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-155">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` without pagination.</span></span>

### <span data-ttu-id="299cf-156">Beispiel 12</span><span class="sxs-lookup"><span data-stu-id="299cf-156">Example 12</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-157">Listen Sie die ersten 15 regionalen Ereignisabonnements (sofern vorhanden) auf, die unter Ressourcengruppen- \` MyResourceGroupName \` in der angegebenen Speicherort-westus2 erstellt wurden \` , die \` die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="299cf-157">List the first 15 regional event subscriptions (if any) created under resource group \`MyResourceGroupName\` in the specified location \`westus2\` that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-158">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-158">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-159">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-159">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-160">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-160">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-161">Beispiel 13</span><span class="sxs-lookup"><span data-stu-id="299cf-161">Example 13</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="299cf-162">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-162">Gets the list of all event subscriptions created for the specified EventHub namespace without pagination.</span></span>

### <span data-ttu-id="299cf-163">Beispiel 14</span><span class="sxs-lookup"><span data-stu-id="299cf-163">Example 14</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-164">Listen Sie die ersten 25 Ereignisabonnements (falls vorhanden) auf, die für den angegebenen EventHub-Namespace erstellt wurden, der die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="299cf-164">List the first 25 event subscriptions (if any) created for the specified EventHub namespace that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-165">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-165">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-166">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-166">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-167">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-167">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-168">Beispiel 15</span><span class="sxs-lookup"><span data-stu-id="299cf-168">Example 15</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="299cf-169">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-169">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location without pagination.</span></span>

### <span data-ttu-id="299cf-170">Beispiel 16</span><span class="sxs-lookup"><span data-stu-id="299cf-170">Example 16</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-171">Listen Sie die ersten 15 Ereignisabonnements (sofern vorhanden) für den angegebenen Thementyp (EventHub-Namespaces) an der angegebenen Position auf, die die $odataFilter Abfrage erfüllt.</span><span class="sxs-lookup"><span data-stu-id="299cf-171">List the first 15 event subscriptions (if any) created for the specified topic type (EventHub namespaces) in the specified location that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-172">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-172">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-173">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-173">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-174">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-174">Caller should stop when result.NextLink becomes $null.</span></span>

### <span data-ttu-id="299cf-175">Beispiel 17</span><span class="sxs-lookup"><span data-stu-id="299cf-175">Example 17</span></span>
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="299cf-176">Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe ohne Paginierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-176">Gets the list of all event subscriptions created for the specific resource group without pagination.</span></span>

### <span data-ttu-id="299cf-177">Beispiel 18</span><span class="sxs-lookup"><span data-stu-id="299cf-177">Example 18</span></span>
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

<span data-ttu-id="299cf-178">Listen Sie die ersten 100-Ereignisabonnements (sofern vorhanden) auf, die für die bestimmte Ressourcengruppe erstellt wurden, die der $odataFilter Abfrage entspricht.</span><span class="sxs-lookup"><span data-stu-id="299cf-178">List the first 100 event subscriptions (if any) created for the specific resource group that satisfies the $odataFilter query.</span></span> <span data-ttu-id="299cf-179">Wenn weitere Ergebnisse zur Verfügung stehen, wird die $Result. Nextlink wird nicht $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-179">If more results are available, the $result.NextLink will not be $null.</span></span> <span data-ttu-id="299cf-180">Um die nächste Seite (n) von Ereignisabonnements zu erhalten, wird erwartet, dass der Benutzer Get-AzEventGridSubscription erneut anruft und Ergebnis verwendet. Nextlink, der aus dem vorherigen Anruf abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="299cf-180">In order to get next page(s) of event subscriptions, user is expected to re-call Get-AzEventGridSubscription and uses result.NextLink obtained from the previous call.</span></span> <span data-ttu-id="299cf-181">Der Anrufer sollte beim Ergebnis beendet werden. Nextlink wird $NULL.</span><span class="sxs-lookup"><span data-stu-id="299cf-181">Caller should stop when result.NextLink becomes $null.</span></span>

## <span data-ttu-id="299cf-182">Parameter</span><span class="sxs-lookup"><span data-stu-id="299cf-182">PARAMETERS</span></span>

### <span data-ttu-id="299cf-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299cf-183">-DefaultProfile</span></span>
<span data-ttu-id="299cf-184">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="299cf-184">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="299cf-185">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="299cf-185">-DomainInputObject</span></span>
<span data-ttu-id="299cf-186">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="299cf-186">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="299cf-187">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="299cf-187">-DomainName</span></span>
<span data-ttu-id="299cf-188">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="299cf-188">EventGrid domain name.</span></span>

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

### <span data-ttu-id="299cf-189">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="299cf-189">-DomainTopicInputObject</span></span>
<span data-ttu-id="299cf-190">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="299cf-190">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="299cf-191">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="299cf-191">-DomainTopicName</span></span>
<span data-ttu-id="299cf-192">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="299cf-192">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="299cf-193">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="299cf-193">-EventSubscriptionName</span></span>
<span data-ttu-id="299cf-194">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="299cf-194">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299cf-195">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="299cf-195">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="299cf-196">Schließen Sie die vollständige Endpunkt-URL des Ereignisabonnement Ziels ein.</span><span class="sxs-lookup"><span data-stu-id="299cf-196">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="299cf-197">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="299cf-197">-InputObject</span></span>
<span data-ttu-id="299cf-198">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="299cf-198">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="299cf-199">-Standort</span><span class="sxs-lookup"><span data-stu-id="299cf-199">-Location</span></span>
<span data-ttu-id="299cf-200">Lage</span><span class="sxs-lookup"><span data-stu-id="299cf-200">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299cf-201">-Nextlink</span><span class="sxs-lookup"><span data-stu-id="299cf-201">-NextLink</span></span>
<span data-ttu-id="299cf-202">Der Link für die nächste Seite der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="299cf-202">The link for the next page of resources to be obtained.</span></span> <span data-ttu-id="299cf-203">Dieser Wert wird mit dem ersten Get-AzEventGrid-Cmdlet-Aufruf abgerufen, wenn noch weitere Ressourcen zur Abfrage zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="299cf-203">This value is obtained with the first Get-AzEventGrid cmdlet call when more resources are still available to be queried.</span></span>

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

### <span data-ttu-id="299cf-204">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="299cf-204">-ODataQuery</span></span>
<span data-ttu-id="299cf-205">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="299cf-205">The OData query used for filtering the list results.</span></span> <span data-ttu-id="299cf-206">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="299cf-206">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="299cf-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="299cf-207">-ResourceGroupName</span></span>
<span data-ttu-id="299cf-208">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="299cf-208">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299cf-209">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="299cf-209">-ResourceId</span></span>
<span data-ttu-id="299cf-210">Der Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="299cf-210">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="299cf-211">-Top</span><span class="sxs-lookup"><span data-stu-id="299cf-211">-Top</span></span>
<span data-ttu-id="299cf-212">Die OData-Abfrage, die zum Filtern der Listenergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="299cf-212">The OData query used for filtering the list results.</span></span> <span data-ttu-id="299cf-213">Das Filtern ist derzeit nur für die Name-Eigenschaft zulässig. Zu den unterstützten Vorgängen gehören: Contains, EQ (für EQUAL), ne (für ungleich), und, oder und nicht.</span><span class="sxs-lookup"><span data-stu-id="299cf-213">Filtering is currently allowed on the Name property only.The supported operations include: CONTAINS, eq (for equal), ne (for not equal), AND, OR and NOT.</span></span>

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

### <span data-ttu-id="299cf-214">-Topicname</span><span class="sxs-lookup"><span data-stu-id="299cf-214">-TopicName</span></span>
<span data-ttu-id="299cf-215">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="299cf-215">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299cf-216">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="299cf-216">-TopicTypeName</span></span>
<span data-ttu-id="299cf-217">TopicType-Name</span><span class="sxs-lookup"><span data-stu-id="299cf-217">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="299cf-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299cf-218">CommonParameters</span></span>
<span data-ttu-id="299cf-219">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="299cf-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299cf-220">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299cf-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299cf-221">Eingaben</span><span class="sxs-lookup"><span data-stu-id="299cf-221">INPUTS</span></span>

### <span data-ttu-id="299cf-222">System. String</span><span class="sxs-lookup"><span data-stu-id="299cf-222">System.String</span></span>

### <span data-ttu-id="299cf-223">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="299cf-223">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="299cf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="299cf-224">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="299cf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="299cf-225">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

### <span data-ttu-id="299cf-226">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="299cf-226">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="299cf-227">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="299cf-227">OUTPUTS</span></span>

### <span data-ttu-id="299cf-228">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="299cf-228">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="299cf-229">Notizen</span><span class="sxs-lookup"><span data-stu-id="299cf-229">NOTES</span></span>

## <span data-ttu-id="299cf-230">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="299cf-230">RELATED LINKS</span></span>
