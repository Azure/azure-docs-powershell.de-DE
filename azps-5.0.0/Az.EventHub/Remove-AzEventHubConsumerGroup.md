---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179281"
---
# <span data-ttu-id="74a82-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="74a82-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="74a82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74a82-102">SYNOPSIS</span></span>
<span data-ttu-id="74a82-103">Löscht die angegebene Event Hubs-Verbrauchergruppe.</span><span class="sxs-lookup"><span data-stu-id="74a82-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="74a82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74a82-104">SYNTAX</span></span>

### <span data-ttu-id="74a82-105">ConsumergroupPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="74a82-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74a82-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74a82-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74a82-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74a82-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a82-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74a82-108">DESCRIPTION</span></span>
<span data-ttu-id="74a82-109">Das Remove-AzEventHubConsumerGroup-Cmdlet entfernt die angegebene Consumer-Gruppe aus dem angegebenen Ereignis-Hub und löscht sie.</span><span class="sxs-lookup"><span data-stu-id="74a82-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="74a82-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74a82-110">EXAMPLES</span></span>

### <span data-ttu-id="74a82-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74a82-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="74a82-112">Löscht die Consumer \` -Gruppen \` -MyConsumerGroupName aus dem \` Event \` -Hub-MyEventHubName, der auf den \` mynamespacename-Namespace beschränkt ist \` .</span><span class="sxs-lookup"><span data-stu-id="74a82-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="74a82-113">Beispiel 2: Inputobject – using-Variable</span><span class="sxs-lookup"><span data-stu-id="74a82-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="74a82-114">Beispiel 3: Inputobject-using Piping</span><span class="sxs-lookup"><span data-stu-id="74a82-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="74a82-115">Beispiel 4: resourcecode mit Variable</span><span class="sxs-lookup"><span data-stu-id="74a82-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="74a82-116">Beispiel 5: Resourcen-unter Verwendung einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="74a82-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="74a82-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="74a82-117">PARAMETERS</span></span>

### <span data-ttu-id="74a82-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a82-118">-AsJob</span></span>
<span data-ttu-id="74a82-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74a82-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74a82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a82-120">-DefaultProfile</span></span>
<span data-ttu-id="74a82-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74a82-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a82-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="74a82-122">-EventHub</span></span>
<span data-ttu-id="74a82-123">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="74a82-123">EventHub Name</span></span>

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

### <span data-ttu-id="74a82-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74a82-124">-InputObject</span></span>
<span data-ttu-id="74a82-125">Consumergroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="74a82-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="74a82-126">-Name</span><span class="sxs-lookup"><span data-stu-id="74a82-126">-Name</span></span>
<span data-ttu-id="74a82-127">Consumergroup-Name</span><span class="sxs-lookup"><span data-stu-id="74a82-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="74a82-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="74a82-128">-Namespace</span></span>
<span data-ttu-id="74a82-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="74a82-129">Namespace Name</span></span>

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

### <span data-ttu-id="74a82-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74a82-130">-PassThru</span></span>
<span data-ttu-id="74a82-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="74a82-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="74a82-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a82-132">-ResourceGroupName</span></span>
<span data-ttu-id="74a82-133">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="74a82-133">Resource Group Name</span></span>

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

### <span data-ttu-id="74a82-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="74a82-134">-ResourceId</span></span>
<span data-ttu-id="74a82-135">Consumergroup-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="74a82-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="74a82-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74a82-136">-Confirm</span></span>
<span data-ttu-id="74a82-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74a82-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a82-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a82-138">-WhatIf</span></span>
<span data-ttu-id="74a82-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74a82-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a82-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74a82-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a82-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a82-141">CommonParameters</span></span>
<span data-ttu-id="74a82-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a82-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a82-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a82-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a82-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74a82-144">INPUTS</span></span>

### <span data-ttu-id="74a82-145">System. String</span><span class="sxs-lookup"><span data-stu-id="74a82-145">System.String</span></span>

### <span data-ttu-id="74a82-146">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="74a82-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="74a82-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74a82-147">OUTPUTS</span></span>

### <span data-ttu-id="74a82-148">System. void</span><span class="sxs-lookup"><span data-stu-id="74a82-148">System.Void</span></span>

## <span data-ttu-id="74a82-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="74a82-149">NOTES</span></span>

## <span data-ttu-id="74a82-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74a82-150">RELATED LINKS</span></span>
