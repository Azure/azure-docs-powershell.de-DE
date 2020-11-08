---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175194"
---
# <span data-ttu-id="f05fa-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f05fa-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="f05fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f05fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f05fa-103">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="f05fa-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="f05fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f05fa-104">SYNTAX</span></span>

### <span data-ttu-id="f05fa-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f05fa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f05fa-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f05fa-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f05fa-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f05fa-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f05fa-114">DESCRIPTION</span></span>
<span data-ttu-id="f05fa-115">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f05fa-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="f05fa-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f05fa-116">EXAMPLES</span></span>

### <span data-ttu-id="f05fa-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f05fa-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f05fa-118">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Azure-Ereignis Raster Thema \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f05fa-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f05fa-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f05fa-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f05fa-120">Entfernt das Ereignisabonnement \` EventSubscription1 \` in eine Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f05fa-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f05fa-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f05fa-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f05fa-122">Entfernt das Ereignisabonnement \` EventSubscription1 \` in das standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f05fa-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="f05fa-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="f05fa-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f05fa-124">Entfernt das Ereignisabonnement \` \` -EventSubscription1 in einen Event Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f05fa-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="f05fa-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="f05fa-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="f05fa-126">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="f05fa-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="f05fa-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="f05fa-127">PARAMETERS</span></span>

### <span data-ttu-id="f05fa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05fa-128">-DefaultProfile</span></span>
<span data-ttu-id="f05fa-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f05fa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f05fa-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="f05fa-130">-DomainInputObject</span></span>
<span data-ttu-id="f05fa-131">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f05fa-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="f05fa-132">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="f05fa-132">-DomainName</span></span>
<span data-ttu-id="f05fa-133">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="f05fa-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="f05fa-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="f05fa-135">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="f05fa-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="f05fa-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="f05fa-136">-DomainTopicName</span></span>
<span data-ttu-id="f05fa-137">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="f05fa-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f05fa-138">-EventSubscriptionName</span></span>
<span data-ttu-id="f05fa-139">Der Name des Ereignisabonnements, das entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f05fa-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f05fa-140">-InputObject</span></span>
<span data-ttu-id="f05fa-141">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f05fa-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f05fa-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f05fa-142">-PassThru</span></span>
<span data-ttu-id="f05fa-143">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="f05fa-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="f05fa-144">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f05fa-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05fa-145">-ResourceGroupName</span></span>
<span data-ttu-id="f05fa-146">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f05fa-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f05fa-147">-ResourceId</span></span>
<span data-ttu-id="f05fa-148">Der Bezeichner der Ressource, deren Ereignisabonnement entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f05fa-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="f05fa-149">-Topicname</span><span class="sxs-lookup"><span data-stu-id="f05fa-149">-TopicName</span></span>
<span data-ttu-id="f05fa-150">Themen Name des Ereignis Rasters</span><span class="sxs-lookup"><span data-stu-id="f05fa-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f05fa-151">-Confirm</span></span>
<span data-ttu-id="f05fa-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f05fa-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05fa-153">-WhatIf</span></span>
<span data-ttu-id="f05fa-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f05fa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05fa-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f05fa-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f05fa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05fa-156">CommonParameters</span></span>
<span data-ttu-id="f05fa-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05fa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05fa-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f05fa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05fa-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f05fa-159">INPUTS</span></span>

### <span data-ttu-id="f05fa-160">System. String</span><span class="sxs-lookup"><span data-stu-id="f05fa-160">System.String</span></span>

### <span data-ttu-id="f05fa-161">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f05fa-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="f05fa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="f05fa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="f05fa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f05fa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="f05fa-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f05fa-164">OUTPUTS</span></span>

### <span data-ttu-id="f05fa-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f05fa-165">System.Boolean</span></span>

## <span data-ttu-id="f05fa-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="f05fa-166">NOTES</span></span>

## <span data-ttu-id="f05fa-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f05fa-167">RELATED LINKS</span></span>
