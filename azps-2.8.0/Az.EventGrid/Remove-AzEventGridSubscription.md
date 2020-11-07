---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 2e2abe03d0df4ccf662f99945c45e837669a1de9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651214"
---
# <span data-ttu-id="ea3ba-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ea3ba-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="ea3ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3ba-103">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="ea3ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea3ba-104">SYNTAX</span></span>

### <span data-ttu-id="ea3ba-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea3ba-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea3ba-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea3ba-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea3ba-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea3ba-114">DESCRIPTION</span></span>
<span data-ttu-id="ea3ba-115">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="ea3ba-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea3ba-116">EXAMPLES</span></span>

### <span data-ttu-id="ea3ba-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea3ba-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ea3ba-118">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Azure-Ereignis Raster Thema \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ea3ba-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ea3ba-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ea3ba-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ea3ba-120">Entfernt das Ereignisabonnement \` EventSubscription1 \` in eine Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ea3ba-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ea3ba-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ea3ba-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ea3ba-122">Entfernt das Ereignisabonnement \` EventSubscription1 \` in das standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="ea3ba-123">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="ea3ba-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ea3ba-124">Entfernt das Ereignisabonnement \` \` -EventSubscription1 in einen Event Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="ea3ba-125">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="ea3ba-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="ea3ba-126">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="ea3ba-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea3ba-127">PARAMETERS</span></span>

### <span data-ttu-id="ea3ba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3ba-128">-DefaultProfile</span></span>
<span data-ttu-id="ea3ba-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ea3ba-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea3ba-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="ea3ba-130">-DomainInputObject</span></span>
<span data-ttu-id="ea3ba-131">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="ea3ba-132">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="ea3ba-132">-DomainName</span></span>
<span data-ttu-id="ea3ba-133">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="ea3ba-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="ea3ba-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="ea3ba-135">Topic-Objekt der EventGrid-Domäne</span><span class="sxs-lookup"><span data-stu-id="ea3ba-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="ea3ba-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="ea3ba-136">-DomainTopicName</span></span>
<span data-ttu-id="ea3ba-137">EventGrid Domain Topic Name.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="ea3ba-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ea3ba-138">-EventSubscriptionName</span></span>
<span data-ttu-id="ea3ba-139">Der Name des Ereignisabonnements, das entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="ea3ba-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea3ba-140">-InputObject</span></span>
<span data-ttu-id="ea3ba-141">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ea3ba-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea3ba-142">-PassThru</span></span>
<span data-ttu-id="ea3ba-143">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ea3ba-144">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea3ba-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea3ba-145">-ResourceGroupName</span></span>
<span data-ttu-id="ea3ba-146">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea3ba-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea3ba-147">-ResourceId</span></span>
<span data-ttu-id="ea3ba-148">Der Bezeichner der Ressource, deren Ereignisabonnement entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="ea3ba-149">-Topicname</span><span class="sxs-lookup"><span data-stu-id="ea3ba-149">-TopicName</span></span>
<span data-ttu-id="ea3ba-150">Themen Name des Ereignis Rasters</span><span class="sxs-lookup"><span data-stu-id="ea3ba-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="ea3ba-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea3ba-151">-Confirm</span></span>
<span data-ttu-id="ea3ba-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea3ba-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea3ba-153">-WhatIf</span></span>
<span data-ttu-id="ea3ba-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea3ba-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea3ba-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3ba-156">CommonParameters</span></span>
<span data-ttu-id="ea3ba-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3ba-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3ba-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3ba-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3ba-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea3ba-159">INPUTS</span></span>

### <span data-ttu-id="ea3ba-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ea3ba-160">System.String</span></span>

### <span data-ttu-id="ea3ba-161">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="ea3ba-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="ea3ba-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ea3ba-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="ea3ba-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ea3ba-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="ea3ba-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea3ba-164">OUTPUTS</span></span>

### <span data-ttu-id="ea3ba-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea3ba-165">System.Boolean</span></span>

## <span data-ttu-id="ea3ba-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea3ba-166">NOTES</span></span>

## <span data-ttu-id="ea3ba-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea3ba-167">RELATED LINKS</span></span>
