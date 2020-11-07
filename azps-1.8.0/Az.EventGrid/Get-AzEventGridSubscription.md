---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 2a6d73e14367d2ed8cf0782337a225f3c5dea4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661086"
---
# <span data-ttu-id="2fc25-101">Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2fc25-101">Get-AzEventGridSubscription</span></span>

## <span data-ttu-id="2fc25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fc25-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc25-103">Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2fc25-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

## <span data-ttu-id="2fc25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc25-104">SYNTAX</span></span>

### <span data-ttu-id="2fc25-105">EventSubscriptionTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fc25-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fc25-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc25-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc25-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc25-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fc25-108">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fc25-108">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fc25-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fc25-109">DESCRIPTION</span></span>
<span data-ttu-id="2fc25-110">Das Get-AzEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2fc25-110">The Get-AzEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="2fc25-111">Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fc25-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="2fc25-112">Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fc25-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="2fc25-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fc25-113">EXAMPLES</span></span>

### <span data-ttu-id="2fc25-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fc25-114">Example 1</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2fc25-115">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fc25-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2fc25-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2fc25-116">Example 2</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="2fc25-117">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="2fc25-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="2fc25-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2fc25-118">Example 3</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="2fc25-119">Rufen Sie eine Liste aller Ereignisabonnements ab, die für Topic \` THEMA1 hat \` in der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fc25-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2fc25-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2fc25-120">Example 4</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2fc25-121">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .</span><span class="sxs-lookup"><span data-stu-id="2fc25-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2fc25-122">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="2fc25-122">Example 5</span></span>
```
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2fc25-123">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="2fc25-124">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="2fc25-124">Example 6</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="2fc25-125">Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fc25-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2fc25-126">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="2fc25-126">Example 7</span></span>
```
PS C:\> Get-AzEventGridSubscription
```

<span data-ttu-id="2fc25-127">Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="2fc25-128">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="2fc25-128">Example 8</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="2fc25-129">Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcengruppen- \` MyResourceGroupName \` im angegebenen Speicherort westus2 erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2fc25-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="2fc25-130">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="2fc25-130">Example 9</span></span>
```
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="2fc25-131">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="2fc25-132">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="2fc25-132">Example 10</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="2fc25-133">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="2fc25-134">Beispiel 11</span><span class="sxs-lookup"><span data-stu-id="2fc25-134">Example 11</span></span>
```
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="2fc25-135">Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="2fc25-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc25-136">PARAMETERS</span></span>

### <span data-ttu-id="2fc25-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc25-137">-DefaultProfile</span></span>
<span data-ttu-id="2fc25-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2fc25-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fc25-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2fc25-139">-EventSubscriptionName</span></span>
<span data-ttu-id="2fc25-140">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="2fc25-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc25-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="2fc25-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="2fc25-142">Schließen Sie die vollständige Endpunkt-URL des Ereignisabonnement Ziels ein.</span><span class="sxs-lookup"><span data-stu-id="2fc25-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc25-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2fc25-143">-InputObject</span></span>
<span data-ttu-id="2fc25-144">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2fc25-144">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="2fc25-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="2fc25-145">-Location</span></span>
<span data-ttu-id="2fc25-146">Lage</span><span class="sxs-lookup"><span data-stu-id="2fc25-146">Location</span></span>

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

### <span data-ttu-id="2fc25-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc25-147">-ResourceGroupName</span></span>
<span data-ttu-id="2fc25-148">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2fc25-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc25-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2fc25-149">-ResourceId</span></span>
<span data-ttu-id="2fc25-150">Der Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2fc25-150">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="2fc25-151">-Topicname</span><span class="sxs-lookup"><span data-stu-id="2fc25-151">-TopicName</span></span>
<span data-ttu-id="2fc25-152">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="2fc25-152">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2fc25-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="2fc25-153">-TopicTypeName</span></span>
<span data-ttu-id="2fc25-154">TopicType-Name</span><span class="sxs-lookup"><span data-stu-id="2fc25-154">TopicType name</span></span>

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

### <span data-ttu-id="2fc25-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc25-155">CommonParameters</span></span>
<span data-ttu-id="2fc25-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc25-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc25-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc25-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc25-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fc25-158">INPUTS</span></span>

### <span data-ttu-id="2fc25-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2fc25-159">System.String</span></span>

### <span data-ttu-id="2fc25-160">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="2fc25-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="2fc25-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fc25-161">OUTPUTS</span></span>

### <span data-ttu-id="2fc25-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="2fc25-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="2fc25-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fc25-163">NOTES</span></span>

## <span data-ttu-id="2fc25-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fc25-164">RELATED LINKS</span></span>
