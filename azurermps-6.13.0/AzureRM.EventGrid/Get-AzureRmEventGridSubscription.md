---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497489"
---
# <span data-ttu-id="b0c16-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="b0c16-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="b0c16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0c16-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c16-103">Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b0c16-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0c16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0c16-104">SYNTAX</span></span>

### <span data-ttu-id="b0c16-105">EventSubscriptionTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0c16-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c16-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c16-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c16-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c16-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c16-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b0c16-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0c16-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0c16-109">DESCRIPTION</span></span>
<span data-ttu-id="b0c16-110">Das Get-AzureRmEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b0c16-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="b0c16-111">Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0c16-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="b0c16-112">Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0c16-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="b0c16-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0c16-113">EXAMPLES</span></span>

### <span data-ttu-id="b0c16-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0c16-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b0c16-115">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="b0c16-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b0c16-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b0c16-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="b0c16-117">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="b0c16-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="b0c16-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b0c16-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="b0c16-119">Rufen Sie eine Liste aller Ereignisabonnements ab, die für Topic \` THEMA1 hat \` in der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="b0c16-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b0c16-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="b0c16-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b0c16-121">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .</span><span class="sxs-lookup"><span data-stu-id="b0c16-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b0c16-122">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="b0c16-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="b0c16-123">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="b0c16-124">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="b0c16-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="b0c16-125">Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="b0c16-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b0c16-126">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="b0c16-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="b0c16-127">Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="b0c16-128">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="b0c16-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="b0c16-129">Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcengruppen- \` MyResourceGroupName \` im angegebenen Speicherort westus2 erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="b0c16-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="b0c16-130">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="b0c16-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="b0c16-131">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="b0c16-132">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="b0c16-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="b0c16-133">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="b0c16-134">Beispiel 11</span><span class="sxs-lookup"><span data-stu-id="b0c16-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="b0c16-135">Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="b0c16-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0c16-136">PARAMETERS</span></span>

### <span data-ttu-id="b0c16-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c16-137">-DefaultProfile</span></span>
<span data-ttu-id="b0c16-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b0c16-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c16-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b0c16-139">-EventSubscriptionName</span></span>
<span data-ttu-id="b0c16-140">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="b0c16-140">The name of the event subscription</span></span>

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

### <span data-ttu-id="b0c16-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="b0c16-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="b0c16-142">Schließen Sie die vollständige Endpunkt-URL des Ereignisabonnement Ziels ein.</span><span class="sxs-lookup"><span data-stu-id="b0c16-142">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="b0c16-143">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0c16-143">-InputObject</span></span>
<span data-ttu-id="b0c16-144">EventGrid-Ereignisabonnement Objekt.</span><span class="sxs-lookup"><span data-stu-id="b0c16-144">EventGrid Event Subscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c16-145">-Standort</span><span class="sxs-lookup"><span data-stu-id="b0c16-145">-Location</span></span>
<span data-ttu-id="b0c16-146">Lage</span><span class="sxs-lookup"><span data-stu-id="b0c16-146">Location</span></span>

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

### <span data-ttu-id="b0c16-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0c16-147">-ResourceGroupName</span></span>
<span data-ttu-id="b0c16-148">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0c16-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0c16-149">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b0c16-149">-ResourceId</span></span>
<span data-ttu-id="b0c16-150">Der Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b0c16-150">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="b0c16-151">-Topicname</span><span class="sxs-lookup"><span data-stu-id="b0c16-151">-TopicName</span></span>
<span data-ttu-id="b0c16-152">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="b0c16-152">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="b0c16-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="b0c16-153">-TopicTypeName</span></span>
<span data-ttu-id="b0c16-154">TopicType-Name</span><span class="sxs-lookup"><span data-stu-id="b0c16-154">TopicType name</span></span>

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

### <span data-ttu-id="b0c16-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c16-155">CommonParameters</span></span>
<span data-ttu-id="b0c16-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c16-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c16-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c16-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c16-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0c16-158">INPUTS</span></span>

### <span data-ttu-id="b0c16-159">System. String</span><span class="sxs-lookup"><span data-stu-id="b0c16-159">System.String</span></span>

### <span data-ttu-id="b0c16-160">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="b0c16-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="b0c16-161">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0c16-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b0c16-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0c16-162">OUTPUTS</span></span>

### <span data-ttu-id="b0c16-163">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="b0c16-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="b0c16-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0c16-164">NOTES</span></span>

## <span data-ttu-id="b0c16-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0c16-165">RELATED LINKS</span></span>
