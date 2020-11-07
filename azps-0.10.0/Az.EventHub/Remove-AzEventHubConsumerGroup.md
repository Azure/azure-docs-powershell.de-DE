---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: d4443cf25790d74617a02b048ce31296e451cf95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842295"
---
# <span data-ttu-id="316ad-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="316ad-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="316ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="316ad-102">SYNOPSIS</span></span>
<span data-ttu-id="316ad-103">Löscht die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="316ad-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="316ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="316ad-104">SYNTAX</span></span>

### <span data-ttu-id="316ad-105">ConsumergroupPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="316ad-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="316ad-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="316ad-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316ad-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="316ad-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316ad-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="316ad-108">DESCRIPTION</span></span>
<span data-ttu-id="316ad-109">Das Remove-AzEventHubConsumerGroup-Cmdlet entfernt die angegebene Consumer-Gruppe aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="316ad-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="316ad-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="316ad-110">EXAMPLES</span></span>

### <span data-ttu-id="316ad-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="316ad-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="316ad-112">Löscht die Consumer \` -Gruppen \` -MyConsumerGroupName aus dem \` Event \` -Hub-MyEventHubName, der auf den \` mynamespacename-Namespace beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="316ad-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="316ad-113">Beispiel 2,1-Inputobject – using-Variable</span><span class="sxs-lookup"><span data-stu-id="316ad-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="316ad-114">Beispiel 2,2-Inputobject – Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="316ad-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="316ad-115">Beispiel 3,1-Sourcecode mit Variable</span><span class="sxs-lookup"><span data-stu-id="316ad-115">Example 3.1 - ResourceId Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="316ad-116">Beispiel 3,2-resourcecode mithilfe einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="316ad-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="316ad-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="316ad-117">PARAMETERS</span></span>

### <span data-ttu-id="316ad-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="316ad-118">-AsJob</span></span>
<span data-ttu-id="316ad-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="316ad-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="316ad-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316ad-120">-DefaultProfile</span></span>
<span data-ttu-id="316ad-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="316ad-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316ad-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="316ad-122">-EventHub</span></span>
<span data-ttu-id="316ad-123">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="316ad-123">EventHub Name</span></span>

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

### <span data-ttu-id="316ad-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="316ad-124">-InputObject</span></span>
<span data-ttu-id="316ad-125">Consumergroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="316ad-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="316ad-126">-Name</span><span class="sxs-lookup"><span data-stu-id="316ad-126">-Name</span></span>
<span data-ttu-id="316ad-127">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="316ad-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="316ad-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="316ad-128">-Namespace</span></span>
<span data-ttu-id="316ad-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="316ad-129">Namespace Name</span></span>

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

### <span data-ttu-id="316ad-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="316ad-130">-PassThru</span></span>
<span data-ttu-id="316ad-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="316ad-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="316ad-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316ad-132">-ResourceGroupName</span></span>
<span data-ttu-id="316ad-133">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="316ad-133">Resource Group Name</span></span>

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

### <span data-ttu-id="316ad-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="316ad-134">-ResourceId</span></span>
<span data-ttu-id="316ad-135">Consumergroup-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="316ad-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="316ad-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="316ad-136">-Confirm</span></span>
<span data-ttu-id="316ad-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="316ad-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316ad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316ad-138">-WhatIf</span></span>
<span data-ttu-id="316ad-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="316ad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="316ad-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="316ad-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316ad-141">CommonParameters</span></span>
<span data-ttu-id="316ad-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="316ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316ad-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="316ad-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316ad-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="316ad-144">INPUTS</span></span>

### <span data-ttu-id="316ad-145">System. String</span><span class="sxs-lookup"><span data-stu-id="316ad-145">System.String</span></span>

### <span data-ttu-id="316ad-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="316ad-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="316ad-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="316ad-147">OUTPUTS</span></span>

### <span data-ttu-id="316ad-148">System. void</span><span class="sxs-lookup"><span data-stu-id="316ad-148">System.Void</span></span>

## <span data-ttu-id="316ad-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="316ad-149">NOTES</span></span>

## <span data-ttu-id="316ad-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="316ad-150">RELATED LINKS</span></span>
