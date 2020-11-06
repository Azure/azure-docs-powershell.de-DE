---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: ba59f19183cf49802240d7631b99b3e69a9bc6f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497329"
---
# <span data-ttu-id="7de9b-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="7de9b-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="7de9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7de9b-102">SYNOPSIS</span></span>
<span data-ttu-id="7de9b-103">Entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7de9b-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7de9b-104">SYNTAX</span></span>

### <span data-ttu-id="7de9b-105">QueuePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7de9b-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de9b-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7de9b-106">QueueInputObjectSet</span></span>
```
Remove-AzureRmServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de9b-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7de9b-107">QueueResourceIdSet</span></span>
```
Remove-AzureRmServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de9b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7de9b-108">DESCRIPTION</span></span>
<span data-ttu-id="7de9b-109">Das Cmdlet **Remove-AzureRmServiceBusQueue** entfernt die Warteschlange aus dem angegebenen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7de9b-109">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7de9b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7de9b-110">EXAMPLES</span></span>

### <span data-ttu-id="7de9b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7de9b-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="7de9b-112">Entfernt die ServiceBus-Warteschlange `SB-Queue_exampl1` aus dem Namespace `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7de9b-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="7de9b-113">Beispiel 2,1-Inputobject-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="7de9b-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="7de9b-114">Entfernt die Service Bus-Warteschlange, die im $Inputobject für-Inputobject-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7de9b-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="7de9b-115">Beispiel 2,1-Inputobject-using Piping:</span><span class="sxs-lookup"><span data-stu-id="7de9b-115">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\>  Get-AzureRmServiceBusQueue <params> | Remove-AzureRmServiceBusQueue
```

### <span data-ttu-id="7de9b-116">Beispiel 3,1-Resourcen-using-Variable:</span><span class="sxs-lookup"><span data-stu-id="7de9b-116">Example 3.1 - ResourceId - Using variable:</span></span>
```
PS c:\> $resourceid = Get-AzureRmServiceBusQueue <params>
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="7de9b-117">Entfernt die ServiceBus-Warteschlange, die in der Arm-ID in $ResourceId/String for-Resourcen-Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7de9b-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="7de9b-118">Beispiel 3,2-passign als Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="7de9b-118">Example 3.2 - ResourceId - passign as string:</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="7de9b-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="7de9b-119">PARAMETERS</span></span>

### <span data-ttu-id="7de9b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7de9b-120">-AsJob</span></span>
<span data-ttu-id="7de9b-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7de9b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7de9b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de9b-122">-DefaultProfile</span></span>
<span data-ttu-id="7de9b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7de9b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de9b-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7de9b-124">-InputObject</span></span>
<span data-ttu-id="7de9b-125">ServiceBus-Warteschlangenobjekt</span><span class="sxs-lookup"><span data-stu-id="7de9b-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="7de9b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7de9b-126">-Name</span></span>
<span data-ttu-id="7de9b-127">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="7de9b-127">Queue Name</span></span>

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

### <span data-ttu-id="7de9b-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7de9b-128">-Namespace</span></span>
<span data-ttu-id="7de9b-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7de9b-129">Namespace Name</span></span>

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

### <span data-ttu-id="7de9b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7de9b-130">-PassThru</span></span>
<span data-ttu-id="7de9b-131">Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7de9b-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7de9b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de9b-132">-ResourceGroupName</span></span>
<span data-ttu-id="7de9b-133">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7de9b-133">The name of the resource group</span></span>

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

### <span data-ttu-id="7de9b-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7de9b-134">-ResourceId</span></span>
<span data-ttu-id="7de9b-135">Service Bus-Warteschlangen-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7de9b-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="7de9b-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7de9b-136">-Confirm</span></span>
<span data-ttu-id="7de9b-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7de9b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de9b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de9b-138">-WhatIf</span></span>
<span data-ttu-id="7de9b-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7de9b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de9b-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7de9b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de9b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de9b-141">CommonParameters</span></span>
<span data-ttu-id="7de9b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de9b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de9b-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de9b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de9b-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7de9b-144">INPUTS</span></span>

### <span data-ttu-id="7de9b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7de9b-145">System.String</span></span>

### <span data-ttu-id="7de9b-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="7de9b-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>
<span data-ttu-id="7de9b-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7de9b-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7de9b-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7de9b-148">OUTPUTS</span></span>

### <span data-ttu-id="7de9b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7de9b-149">System.Boolean</span></span>

## <span data-ttu-id="7de9b-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="7de9b-150">NOTES</span></span>

## <span data-ttu-id="7de9b-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7de9b-151">RELATED LINKS</span></span>
