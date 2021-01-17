---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306539"
---
# <span data-ttu-id="6c4ce-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6c4ce-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="6c4ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4ce-103">Löscht die angegebene Consumergruppe "Ereignishubs".</span><span class="sxs-lookup"><span data-stu-id="6c4ce-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="6c4ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c4ce-104">SYNTAX</span></span>

### <span data-ttu-id="6c4ce-105">ConsumergroupPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c4ce-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6c4ce-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c4ce-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4ce-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c4ce-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c4ce-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4ce-109">Das Remove-AzEventHubConsumerGroup cmdlet entfernt und löscht die angegebene Consumergruppe aus dem angegebenen Ereignishub.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="6c4ce-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c4ce-110">EXAMPLES</span></span>

### <span data-ttu-id="6c4ce-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c4ce-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="6c4ce-112">Löscht die Consumergruppe \` "MyConsumerGroupName" aus dem \` Ereignishub \` "MyEventHubName", der auf den \` \` Namespace "MyNamespaceName" \` begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="6c4ce-113">Beispiel 2: InputObject – Verwenden einer Variablen</span><span class="sxs-lookup"><span data-stu-id="6c4ce-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="6c4ce-114">Beispiel 3: InputObject – Verwenden der Piping</span><span class="sxs-lookup"><span data-stu-id="6c4ce-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="6c4ce-115">Beispiel 4: ResourceId mit Variable</span><span class="sxs-lookup"><span data-stu-id="6c4ce-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="6c4ce-116">Beispiel 5: ResourceId mithilfe der Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6c4ce-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="6c4ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c4ce-117">PARAMETERS</span></span>

### <span data-ttu-id="6c4ce-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c4ce-118">-AsJob</span></span>
<span data-ttu-id="6c4ce-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c4ce-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c4ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4ce-120">-DefaultProfile</span></span>
<span data-ttu-id="6c4ce-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4ce-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6c4ce-122">-EventHub</span></span>
<span data-ttu-id="6c4ce-123">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="6c4ce-123">EventHub Name</span></span>

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

### <span data-ttu-id="6c4ce-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c4ce-124">-InputObject</span></span>
<span data-ttu-id="6c4ce-125">ConsumerGroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="6c4ce-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="6c4ce-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6c4ce-126">-Name</span></span>
<span data-ttu-id="6c4ce-127">ConsumerGroup Name</span><span class="sxs-lookup"><span data-stu-id="6c4ce-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="6c4ce-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6c4ce-128">-Namespace</span></span>
<span data-ttu-id="6c4ce-129">Namespacename</span><span class="sxs-lookup"><span data-stu-id="6c4ce-129">Namespace Name</span></span>

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

### <span data-ttu-id="6c4ce-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c4ce-130">-PassThru</span></span>
<span data-ttu-id="6c4ce-131">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6c4ce-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4ce-132">-ResourceGroupName</span></span>
<span data-ttu-id="6c4ce-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6c4ce-133">Resource Group Name</span></span>

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

### <span data-ttu-id="6c4ce-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4ce-134">-ResourceId</span></span>
<span data-ttu-id="6c4ce-135">ConsumerGroup Resource Id</span><span class="sxs-lookup"><span data-stu-id="6c4ce-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="6c4ce-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c4ce-136">-Confirm</span></span>
<span data-ttu-id="6c4ce-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4ce-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6c4ce-138">-WhatIf</span></span>
<span data-ttu-id="6c4ce-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4ce-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4ce-141">CommonParameters</span></span>
<span data-ttu-id="6c4ce-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4ce-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c4ce-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4ce-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c4ce-144">INPUTS</span></span>

### <span data-ttu-id="6c4ce-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6c4ce-145">System.String</span></span>

### <span data-ttu-id="6c4ce-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="6c4ce-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="6c4ce-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c4ce-147">OUTPUTS</span></span>

### <span data-ttu-id="6c4ce-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="6c4ce-148">System.Void</span></span>

## <span data-ttu-id="6c4ce-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6c4ce-149">NOTES</span></span>

## <span data-ttu-id="6c4ce-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6c4ce-150">RELATED LINKS</span></span>
