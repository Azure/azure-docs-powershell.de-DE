---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 26e306c80f18f3e7d14ca073cfdedfbdc9e6567b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663585"
---
# <span data-ttu-id="2bdda-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2bdda-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="2bdda-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bdda-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdda-103">Ruft die Details eines Ereignisabonnements ab oder ruft eine Liste aller Ereignisabonnements im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2bdda-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bdda-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bdda-104">SYNTAX</span></span>

### <span data-ttu-id="2bdda-105">EventSubscriptionTopicNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bdda-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bdda-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bdda-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bdda-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bdda-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bdda-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2bdda-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bdda-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bdda-109">DESCRIPTION</span></span>
<span data-ttu-id="2bdda-110">Das Get-AzureRmEventGridSubscription-Cmdlet ruft entweder die Details eines angegebenen Ereignis Raster Abonnements oder eine Liste aller Ereignis Raster Abonnements im aktuellen Azure-Abonnement oder in der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2bdda-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="2bdda-111">Wenn der Name des Ereignisabonnements angegeben wird, werden die Details eines einzelnen Ereignis Raster-Abonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2bdda-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="2bdda-112">Wenn der Name des Ereignisabonnements nicht angegeben wird, wird eine Liste aller Ereignisabonnements zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2bdda-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="2bdda-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bdda-113">EXAMPLES</span></span>

### <span data-ttu-id="2bdda-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2bdda-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2bdda-115">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das Thema \` THEMA1 hat in der \` Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2bdda-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2bdda-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2bdda-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="2bdda-117">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für \` das Thema THEMA1 hat in der \` Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` , einschließlich der vollständigen Endpunkt-URL, wenn es sich um ein webhook-basiertes Ereignisabonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="2bdda-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="2bdda-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2bdda-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="2bdda-119">Rufen Sie eine Liste aller Ereignisabonnements ab, die für Topic \` THEMA1 hat \` in der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2bdda-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2bdda-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="2bdda-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2bdda-121">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für die Ressourcengruppen \` -MyResourceGroupName erstellt wurden \` .</span><span class="sxs-lookup"><span data-stu-id="2bdda-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2bdda-122">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="2bdda-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="2bdda-123">Ruft die Details der Ereignisabonnement \` EventSubscription1 ab \` , die für das aktuell ausgewählte Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="2bdda-124">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="2bdda-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="2bdda-125">Ruft die Liste aller globalen Ereignisabonnements ab, die unter der Ressourcengruppe MyResourceGroupName erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2bdda-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2bdda-126">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="2bdda-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="2bdda-127">Ruft die Liste aller globalen Ereignisabonnements ab, die unter dem aktuell ausgewählten Azure-Abonnement erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="2bdda-128">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="2bdda-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="2bdda-129">Ruft die Liste aller regionalen Ereignisabonnements ab, die unter Ressourcengruppen- \` MyResourceGroupName \` im angegebenen Speicherort westus2 erstellt wurden \` \` .</span><span class="sxs-lookup"><span data-stu-id="2bdda-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="2bdda-130">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="2bdda-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="2bdda-131">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen EventHub-Namespace erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="2bdda-132">Beispiel 10</span><span class="sxs-lookup"><span data-stu-id="2bdda-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="2bdda-133">Ruft die Liste aller Ereignisabonnements ab, die für den angegebenen Topic-Typ (EventHub-Namespaces) an der angegebenen Position erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="2bdda-134">Beispiel 11</span><span class="sxs-lookup"><span data-stu-id="2bdda-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="2bdda-135">Ruft die Liste aller Ereignisabonnements ab, die für die jeweilige Ressourcengruppe erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="2bdda-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bdda-136">PARAMETERS</span></span>

### <span data-ttu-id="2bdda-137">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2bdda-137">-EventSubscriptionName</span></span>
<span data-ttu-id="2bdda-138">Der Name des Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="2bdda-138">The name of the event subscription</span></span>

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

### <span data-ttu-id="2bdda-139">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="2bdda-139">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="2bdda-140">Schließen Sie die vollständige Endpunkt-URL des Ereignisabonnement Ziels ein.</span><span class="sxs-lookup"><span data-stu-id="2bdda-140">Include the full endpoint URL of the event subscription destination.</span></span>

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

### <span data-ttu-id="2bdda-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2bdda-141">-InputObject</span></span>
<span data-ttu-id="2bdda-142">EventGrid-Ereignisabonnement Objekt.</span><span class="sxs-lookup"><span data-stu-id="2bdda-142">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="2bdda-143">-Standort</span><span class="sxs-lookup"><span data-stu-id="2bdda-143">-Location</span></span>
<span data-ttu-id="2bdda-144">Lage</span><span class="sxs-lookup"><span data-stu-id="2bdda-144">Location</span></span>

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

### <span data-ttu-id="2bdda-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bdda-145">-ResourceGroupName</span></span>
<span data-ttu-id="2bdda-146">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2bdda-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="2bdda-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2bdda-147">-ResourceId</span></span>
<span data-ttu-id="2bdda-148">Der Bezeichner der Ressource, für die Ereignisabonnements erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2bdda-148">Identifier of the resource to which event subscriptions have been created.</span></span>

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

### <span data-ttu-id="2bdda-149">-Topicname</span><span class="sxs-lookup"><span data-stu-id="2bdda-149">-TopicName</span></span>
<span data-ttu-id="2bdda-150">EventGrid-Themen Name</span><span class="sxs-lookup"><span data-stu-id="2bdda-150">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="2bdda-151">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="2bdda-151">-TopicTypeName</span></span>
<span data-ttu-id="2bdda-152">TopicType-Name</span><span class="sxs-lookup"><span data-stu-id="2bdda-152">TopicType name</span></span>

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

### <span data-ttu-id="2bdda-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bdda-153">-DefaultProfile</span></span>
<span data-ttu-id="2bdda-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bdda-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bdda-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdda-155">CommonParameters</span></span>
<span data-ttu-id="2bdda-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bdda-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdda-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bdda-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdda-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bdda-158">INPUTS</span></span>

### <span data-ttu-id="2bdda-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2bdda-159">System.String</span></span>
<span data-ttu-id="2bdda-160">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2bdda-160">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2bdda-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bdda-161">OUTPUTS</span></span>

### <span data-ttu-id="2bdda-162">Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscription</span><span class="sxs-lookup"><span data-stu-id="2bdda-162">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>
<span data-ttu-id="2bdda-163">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSEventSubscriptionListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2bdda-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscriptionListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2bdda-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bdda-164">NOTES</span></span>

## <span data-ttu-id="2bdda-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bdda-165">RELATED LINKS</span></span>

