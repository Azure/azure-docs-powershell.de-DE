---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: 8f5f1ae36355f1f8d76476e5eee69f63187847ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939563"
---
# <span data-ttu-id="ba075-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ba075-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="ba075-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba075-102">SYNOPSIS</span></span>
<span data-ttu-id="ba075-103">Löscht die angegebene Consumergruppe Ereignishubs.</span><span class="sxs-lookup"><span data-stu-id="ba075-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="ba075-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba075-104">SYNTAX</span></span>

### <span data-ttu-id="ba075-105">ConsumergroupPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba075-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba075-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ba075-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba075-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba075-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba075-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba075-108">DESCRIPTION</span></span>
<span data-ttu-id="ba075-109">Das Remove-AzEventHubConsumerGroup-Cmdlet entfernt und löscht die angegebene Consumergruppe aus dem angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="ba075-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="ba075-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba075-110">EXAMPLES</span></span>

### <span data-ttu-id="ba075-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba075-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="ba075-112">Löscht die Consumergruppe \` MyConsumerGroupName aus dem \` Ereignishub \` MyEventHubName , der auf \` den \` MyNamespaceName-Namespace \` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ba075-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="ba075-113">Beispiel 2: InputObject – Verwenden von Variablen</span><span class="sxs-lookup"><span data-stu-id="ba075-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="ba075-114">Beispiel 3: InputObject – Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="ba075-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="ba075-115">Beispiel 4: ResourceId Using Variable</span><span class="sxs-lookup"><span data-stu-id="ba075-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="ba075-116">Beispiel 5: ResourceId Using string</span><span class="sxs-lookup"><span data-stu-id="ba075-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="ba075-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ba075-117">PARAMETERS</span></span>

### <span data-ttu-id="ba075-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba075-118">-AsJob</span></span>
<span data-ttu-id="ba075-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ba075-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba075-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba075-120">-DefaultProfile</span></span>
<span data-ttu-id="ba075-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba075-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba075-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ba075-122">-EventHub</span></span>
<span data-ttu-id="ba075-123">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="ba075-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba075-124">-InputObject</span></span>
<span data-ttu-id="ba075-125">ConsumerGroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="ba075-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ba075-126">-Name</span></span>
<span data-ttu-id="ba075-127">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="ba075-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba075-128">-Namespace</span></span>
<span data-ttu-id="ba075-129">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ba075-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba075-130">-PassThru</span></span>
<span data-ttu-id="ba075-131">Wenn der Befehl erfolgreich war, gibt die Angabe "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="ba075-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ba075-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba075-132">-ResourceGroupName</span></span>
<span data-ttu-id="ba075-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ba075-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba075-134">-ResourceId</span></span>
<span data-ttu-id="ba075-135">ConsumerGroup Resource Id</span><span class="sxs-lookup"><span data-stu-id="ba075-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba075-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ba075-136">-Confirm</span></span>
<span data-ttu-id="ba075-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba075-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba075-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba075-138">-WhatIf</span></span>
<span data-ttu-id="ba075-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba075-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba075-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba075-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba075-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba075-141">CommonParameters</span></span>
<span data-ttu-id="ba075-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba075-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba075-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba075-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba075-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba075-144">INPUTS</span></span>

### <span data-ttu-id="ba075-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ba075-145">System.String</span></span>

### <span data-ttu-id="ba075-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="ba075-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="ba075-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba075-147">OUTPUTS</span></span>

### <span data-ttu-id="ba075-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba075-148">System.Void</span></span>

## <span data-ttu-id="ba075-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ba075-149">NOTES</span></span>

## <span data-ttu-id="ba075-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ba075-150">RELATED LINKS</span></span>
