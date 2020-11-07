---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: fd872830f82f1d75f0b3c5f60ba6b129d7edd6f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661072"
---
# <span data-ttu-id="43b1e-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="43b1e-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="43b1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="43b1e-103">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement.</span><span class="sxs-lookup"><span data-stu-id="43b1e-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="43b1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b1e-104">SYNTAX</span></span>

### <span data-ttu-id="43b1e-105">ResourceGroupNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43b1e-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b1e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="43b1e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b1e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43b1e-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b1e-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43b1e-108">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43b1e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43b1e-109">DESCRIPTION</span></span>
<span data-ttu-id="43b1e-110">Entfernt ein Azure-Ereignis Raster-Ereignisabonnement für ein Azure-Ereignis Raster Thema, eine Ressource, ein Azure-Abonnement oder eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43b1e-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="43b1e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43b1e-111">EXAMPLES</span></span>

### <span data-ttu-id="43b1e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43b1e-112">Example 1</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="43b1e-113">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Azure-Ereignis Raster Thema \` THEMA1 hat in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="43b1e-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="43b1e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43b1e-114">Example 2</span></span>
```
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="43b1e-115">Entfernt das Ereignisabonnement \` EventSubscription1 \` in eine Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="43b1e-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="43b1e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="43b1e-116">Example 3</span></span>
```
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="43b1e-117">Entfernt das Ereignisabonnement \` EventSubscription1 \` in das standardmäßige Azure-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43b1e-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="43b1e-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="43b1e-118">Example 4</span></span>
```
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="43b1e-119">Entfernt das Ereignisabonnement \` \` -EventSubscription1 in einen Event Hub-Namespace.</span><span class="sxs-lookup"><span data-stu-id="43b1e-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="43b1e-120">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="43b1e-120">Example 5</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="43b1e-121">Entfernt das Ereignisabonnement \` \` -EventSubscription1 zu einem Ereignis Raster Thema.</span><span class="sxs-lookup"><span data-stu-id="43b1e-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="43b1e-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b1e-122">PARAMETERS</span></span>

### <span data-ttu-id="43b1e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b1e-123">-DefaultProfile</span></span>
<span data-ttu-id="43b1e-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="43b1e-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43b1e-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="43b1e-125">-EventSubscriptionName</span></span>
<span data-ttu-id="43b1e-126">Der Name des Ereignisabonnements, das entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="43b1e-126">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b1e-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43b1e-127">-InputObject</span></span>
<span data-ttu-id="43b1e-128">EventGrid Topic-Objekt.</span><span class="sxs-lookup"><span data-stu-id="43b1e-128">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="43b1e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43b1e-129">-PassThru</span></span>
<span data-ttu-id="43b1e-130">Gibt den Status des Remove-Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="43b1e-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="43b1e-131">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="43b1e-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43b1e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b1e-132">-ResourceGroupName</span></span>
<span data-ttu-id="43b1e-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="43b1e-133">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43b1e-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="43b1e-134">-ResourceId</span></span>
<span data-ttu-id="43b1e-135">Der Bezeichner der Ressource, deren Ereignisabonnement entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="43b1e-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="43b1e-136">-Topicname</span><span class="sxs-lookup"><span data-stu-id="43b1e-136">-TopicName</span></span>
<span data-ttu-id="43b1e-137">Themen Name des Ereignis Rasters</span><span class="sxs-lookup"><span data-stu-id="43b1e-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="43b1e-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43b1e-138">-Confirm</span></span>
<span data-ttu-id="43b1e-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43b1e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b1e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b1e-140">-WhatIf</span></span>
<span data-ttu-id="43b1e-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43b1e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b1e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43b1e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b1e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b1e-143">CommonParameters</span></span>
<span data-ttu-id="43b1e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b1e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b1e-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b1e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b1e-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43b1e-146">INPUTS</span></span>

### <span data-ttu-id="43b1e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="43b1e-147">System.String</span></span>

### <span data-ttu-id="43b1e-148">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="43b1e-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="43b1e-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43b1e-149">OUTPUTS</span></span>

### <span data-ttu-id="43b1e-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43b1e-150">System.Boolean</span></span>

## <span data-ttu-id="43b1e-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="43b1e-151">NOTES</span></span>

## <span data-ttu-id="43b1e-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43b1e-152">RELATED LINKS</span></span>
