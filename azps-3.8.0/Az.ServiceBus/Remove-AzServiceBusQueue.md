---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: 6a2ba59acb8148cc3640582b57772a68014177ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995994"
---
# <span data-ttu-id="0f1c2-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0f1c2-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="0f1c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f1c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1c2-103">Entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0f1c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f1c2-104">SYNTAX</span></span>

### <span data-ttu-id="0f1c2-105">QueuePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f1c2-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f1c2-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0f1c2-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f1c2-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0f1c2-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f1c2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f1c2-108">DESCRIPTION</span></span>
<span data-ttu-id="0f1c2-109">Das Cmdlet **Remove-AzServiceBusQueue** entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0f1c2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f1c2-110">EXAMPLES</span></span>

### <span data-ttu-id="0f1c2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f1c2-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="0f1c2-112">Entfernt die ServiceBus-Warteschlange `SB-Queue_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0f1c2-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="0f1c2-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="0f1c2-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="0f1c2-114">Entfernt die Service Bus-Warteschlange, die im $Inputobject für-Inputobject-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="0f1c2-115">Beispiel 2,1-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="0f1c2-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="0f1c2-116">Beispiel 3,1-Resourcen-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="0f1c2-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="0f1c2-117">Entfernt die ServiceBus-Warteschlange, die in der Arm-ID in $ResourceId/String for-Resourcen-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="0f1c2-118">Beispiel 3,2-resourcel-als Zeichenfolge übergeben:</span><span class="sxs-lookup"><span data-stu-id="0f1c2-118">Example 3.2 - ResourceId - passing as string:</span></span>
```
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="0f1c2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f1c2-119">PARAMETERS</span></span>

### <span data-ttu-id="0f1c2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f1c2-120">-AsJob</span></span>
<span data-ttu-id="0f1c2-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0f1c2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f1c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f1c2-122">-DefaultProfile</span></span>
<span data-ttu-id="0f1c2-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f1c2-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0f1c2-124">-InputObject</span></span>
<span data-ttu-id="0f1c2-125">ServiceBus-Warteschlangenobjekt</span><span class="sxs-lookup"><span data-stu-id="0f1c2-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1c2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0f1c2-126">-Name</span></span>
<span data-ttu-id="0f1c2-127">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="0f1c2-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1c2-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0f1c2-128">-Namespace</span></span>
<span data-ttu-id="0f1c2-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="0f1c2-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1c2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f1c2-130">-PassThru</span></span>
<span data-ttu-id="0f1c2-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="0f1c2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f1c2-132">-ResourceGroupName</span></span>
<span data-ttu-id="0f1c2-133">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="0f1c2-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1c2-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f1c2-134">-ResourceId</span></span>
<span data-ttu-id="0f1c2-135">Service Bus-Warteschlangen-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0f1c2-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f1c2-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0f1c2-136">-Confirm</span></span>
<span data-ttu-id="0f1c2-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f1c2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f1c2-138">-WhatIf</span></span>
<span data-ttu-id="0f1c2-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f1c2-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f1c2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1c2-141">CommonParameters</span></span>
<span data-ttu-id="0f1c2-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1c2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1c2-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1c2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1c2-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f1c2-144">INPUTS</span></span>

### <span data-ttu-id="0f1c2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0f1c2-145">System.String</span></span>

### <span data-ttu-id="0f1c2-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="0f1c2-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="0f1c2-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f1c2-147">OUTPUTS</span></span>

### <span data-ttu-id="0f1c2-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f1c2-148">System.Boolean</span></span>

## <span data-ttu-id="0f1c2-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f1c2-149">NOTES</span></span>

## <span data-ttu-id="0f1c2-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f1c2-150">RELATED LINKS</span></span>
