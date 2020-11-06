---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496210"
---
# <span data-ttu-id="badc1-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="badc1-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="badc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="badc1-102">SYNOPSIS</span></span>
<span data-ttu-id="badc1-103">Löscht die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="badc1-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="badc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="badc1-104">SYNTAX</span></span>

### <span data-ttu-id="badc1-105">ConsumergroupPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="badc1-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="badc1-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="badc1-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="badc1-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="badc1-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="badc1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="badc1-108">DESCRIPTION</span></span>
<span data-ttu-id="badc1-109">Das Remove-AzureRmEventHubConsumerGroup-Cmdlet entfernt die angegebene Consumer-Gruppe aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="badc1-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="badc1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="badc1-110">EXAMPLES</span></span>

### <span data-ttu-id="badc1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="badc1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="badc1-112">Löscht die Consumer \` -Gruppen \` -MyConsumerGroupName aus dem \` Event \` -Hub-MyEventHubName, der auf den \` mynamespacename-Namespace beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="badc1-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="badc1-113">Beispiel 2,1-Inputobject – using-Variable</span><span class="sxs-lookup"><span data-stu-id="badc1-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="badc1-114">Beispiel 2,2-Inputobject – Verwenden von Piping</span><span class="sxs-lookup"><span data-stu-id="badc1-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="badc1-115">Beispiel 3,1-resourcecode mithilfe von Vairable</span><span class="sxs-lookup"><span data-stu-id="badc1-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="badc1-116">Beispiel 3,2-resourcecode mithilfe einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="badc1-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="badc1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="badc1-117">PARAMETERS</span></span>

### <span data-ttu-id="badc1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="badc1-118">-AsJob</span></span>
<span data-ttu-id="badc1-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="badc1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="badc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badc1-120">-DefaultProfile</span></span>
<span data-ttu-id="badc1-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="badc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="badc1-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="badc1-122">-EventHub</span></span>
<span data-ttu-id="badc1-123">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="badc1-123">EventHub Name</span></span>

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

### <span data-ttu-id="badc1-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="badc1-124">-InputObject</span></span>
<span data-ttu-id="badc1-125">Consumergroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="badc1-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="badc1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="badc1-126">-Name</span></span>
<span data-ttu-id="badc1-127">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="badc1-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="badc1-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="badc1-128">-Namespace</span></span>
<span data-ttu-id="badc1-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="badc1-129">Namespace Name</span></span>

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

### <span data-ttu-id="badc1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="badc1-130">-PassThru</span></span>
<span data-ttu-id="badc1-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="badc1-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="badc1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="badc1-132">-ResourceGroupName</span></span>
<span data-ttu-id="badc1-133">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="badc1-133">Resource Group Name</span></span>

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

### <span data-ttu-id="badc1-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="badc1-134">-ResourceId</span></span>
<span data-ttu-id="badc1-135">Consumergroup-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="badc1-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="badc1-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="badc1-136">-Confirm</span></span>
<span data-ttu-id="badc1-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="badc1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="badc1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="badc1-138">-WhatIf</span></span>
<span data-ttu-id="badc1-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="badc1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="badc1-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="badc1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="badc1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badc1-141">CommonParameters</span></span>
<span data-ttu-id="badc1-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="badc1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badc1-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="badc1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badc1-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="badc1-144">INPUTS</span></span>

### <span data-ttu-id="badc1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="badc1-145">System.String</span></span>

### <span data-ttu-id="badc1-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="badc1-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="badc1-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="badc1-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="badc1-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="badc1-148">OUTPUTS</span></span>

### <span data-ttu-id="badc1-149">System. void</span><span class="sxs-lookup"><span data-stu-id="badc1-149">System.Void</span></span>

## <span data-ttu-id="badc1-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="badc1-150">NOTES</span></span>

## <span data-ttu-id="badc1-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="badc1-151">RELATED LINKS</span></span>
