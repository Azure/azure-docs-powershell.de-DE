---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 1625e3325164156b1809640c54d4b75698ae7363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938699"
---
# <span data-ttu-id="fbf96-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="fbf96-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="fbf96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbf96-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf96-103">Entfernt ein Azure Event Grid-Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="fbf96-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="fbf96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbf96-104">SYNTAX</span></span>

### <span data-ttu-id="fbf96-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbf96-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbf96-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbf96-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbf96-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbf96-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbf96-114">DESCRIPTION</span></span>
<span data-ttu-id="fbf96-115">Entfernt ein Azure Event Grid-Ereignisabonnement für ein Azure Event Grid-Thema, eine Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbf96-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="fbf96-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbf96-116">EXAMPLES</span></span>

### <span data-ttu-id="fbf96-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbf96-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fbf96-118">Entfernt das Ereignisabonnement \` EventSubscription1 zu einem Azure Event Grid \` \` Topic1 in \` der Ressourcengruppe \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="fbf96-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fbf96-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fbf96-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fbf96-120">Entfernt das Ereignisabonnement \` EventSubscription1 \` zu einer Ressourcengruppe \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="fbf96-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fbf96-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fbf96-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fbf96-122">Entfernt das Ereignisabonnement \` EventSubscription1 \` in das Standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbf96-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="fbf96-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="fbf96-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fbf96-124">Entfernt das Ereignisabonnement \` EventSubscription1 \` in einen Event Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="fbf96-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="fbf96-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="fbf96-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="fbf96-126">Entfernt das Ereignisabonnement \` EventSubscription1 \` in ein Ereignisrasterthema.</span><span class="sxs-lookup"><span data-stu-id="fbf96-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="fbf96-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fbf96-127">PARAMETERS</span></span>

### <span data-ttu-id="fbf96-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf96-128">-DefaultProfile</span></span>
<span data-ttu-id="fbf96-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fbf96-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbf96-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="fbf96-130">-DomainInputObject</span></span>
<span data-ttu-id="fbf96-131">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbf96-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="fbf96-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fbf96-132">-DomainName</span></span>
<span data-ttu-id="fbf96-133">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="fbf96-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="fbf96-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="fbf96-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="fbf96-135">EventGrid Domain Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbf96-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="fbf96-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="fbf96-136">-DomainTopicName</span></span>
<span data-ttu-id="fbf96-137">Name des Themas "EventGrid-Domäne".</span><span class="sxs-lookup"><span data-stu-id="fbf96-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="fbf96-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fbf96-138">-EventSubscriptionName</span></span>
<span data-ttu-id="fbf96-139">Name des Ereignisabonnements, das entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbf96-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="fbf96-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbf96-140">-InputObject</span></span>
<span data-ttu-id="fbf96-141">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbf96-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="fbf96-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbf96-142">-PassThru</span></span>
<span data-ttu-id="fbf96-143">Gibt den Status des Vorgangs "Entfernen" zurück.</span><span class="sxs-lookup"><span data-stu-id="fbf96-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="fbf96-144">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fbf96-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fbf96-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf96-145">-ResourceGroupName</span></span>
<span data-ttu-id="fbf96-146">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fbf96-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="fbf96-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbf96-147">-ResourceId</span></span>
<span data-ttu-id="fbf96-148">Bezeichner der Ressource, deren Ereignisabonnement entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbf96-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="fbf96-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="fbf96-149">-TopicName</span></span>
<span data-ttu-id="fbf96-150">Name des Themas "Ereignisraster".</span><span class="sxs-lookup"><span data-stu-id="fbf96-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="fbf96-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbf96-151">-Confirm</span></span>
<span data-ttu-id="fbf96-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbf96-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbf96-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbf96-153">-WhatIf</span></span>
<span data-ttu-id="fbf96-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbf96-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbf96-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbf96-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbf96-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf96-156">CommonParameters</span></span>
<span data-ttu-id="fbf96-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf96-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf96-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbf96-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf96-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbf96-159">INPUTS</span></span>

### <span data-ttu-id="fbf96-160">System.String</span><span class="sxs-lookup"><span data-stu-id="fbf96-160">System.String</span></span>

### <span data-ttu-id="fbf96-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="fbf96-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="fbf96-162">Microsoft.Azure.Commands.EventGrid.Models.PSDOmain</span><span class="sxs-lookup"><span data-stu-id="fbf96-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="fbf96-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="fbf96-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="fbf96-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbf96-164">OUTPUTS</span></span>

### <span data-ttu-id="fbf96-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbf96-165">System.Boolean</span></span>

## <span data-ttu-id="fbf96-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fbf96-166">NOTES</span></span>

## <span data-ttu-id="fbf96-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fbf96-167">RELATED LINKS</span></span>
