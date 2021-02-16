---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168860"
---
# <span data-ttu-id="5cf2f-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="5cf2f-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="5cf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf2f-103">Entfernt die Warteschlange aus dem angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5cf2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cf2f-104">SYNTAX</span></span>

### <span data-ttu-id="5cf2f-105">QueuePropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cf2f-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf2f-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5cf2f-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf2f-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5cf2f-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cf2f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cf2f-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf2f-109">Das **Cmdlet "Remove-AzServiceBusQueue"** entfernt die Warteschlange aus dem angegebenen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5cf2f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cf2f-110">EXAMPLES</span></span>

### <span data-ttu-id="5cf2f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cf2f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="5cf2f-112">Entfernt die Service `SB-Queue_exampl1` Buswarteschlange aus dem `SB-Example1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="5cf2f-113">Beispiel 2: InputObject – Verwenden einer Variablen:</span><span class="sxs-lookup"><span data-stu-id="5cf2f-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="5cf2f-114">Entfernt die service bus-Warteschlange, die im Parameter $inputobject "-InputObject" bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="5cf2f-115">Beispiel 3: InputObject – Verwenden der Piping:</span><span class="sxs-lookup"><span data-stu-id="5cf2f-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="5cf2f-116">Beispiel 4: ResourceId – Verwenden einer Variablen:</span><span class="sxs-lookup"><span data-stu-id="5cf2f-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="5cf2f-117">Entfernt die Service Buswarteschlange, die in der ARM-ID in $resourceid/Zeichenfolge für den Parameter "-ResourceId" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="5cf2f-118">Beispiel 5: ResourceId – Übergeben als Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="5cf2f-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="5cf2f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cf2f-119">PARAMETERS</span></span>

### <span data-ttu-id="5cf2f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cf2f-120">-AsJob</span></span>
<span data-ttu-id="5cf2f-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5cf2f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cf2f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf2f-122">-DefaultProfile</span></span>
<span data-ttu-id="5cf2f-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf2f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cf2f-124">-InputObject</span></span>
<span data-ttu-id="5cf2f-125">Service Bus Queue Object</span><span class="sxs-lookup"><span data-stu-id="5cf2f-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="5cf2f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5cf2f-126">-Name</span></span>
<span data-ttu-id="5cf2f-127">Warteschlangenname</span><span class="sxs-lookup"><span data-stu-id="5cf2f-127">Queue Name</span></span>

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

### <span data-ttu-id="5cf2f-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5cf2f-128">-Namespace</span></span>
<span data-ttu-id="5cf2f-129">Namespacename</span><span class="sxs-lookup"><span data-stu-id="5cf2f-129">Namespace Name</span></span>

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

### <span data-ttu-id="5cf2f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cf2f-130">-PassThru</span></span>
<span data-ttu-id="5cf2f-131">Wenn Sie diese Angabe angeben, wird "true" zurückgeben, wenn der Befehl erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5cf2f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf2f-132">-ResourceGroupName</span></span>
<span data-ttu-id="5cf2f-133">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5cf2f-133">The name of the resource group</span></span>

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

### <span data-ttu-id="5cf2f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cf2f-134">-ResourceId</span></span>
<span data-ttu-id="5cf2f-135">Ressourcen-ID der Service Buswarteschlange</span><span class="sxs-lookup"><span data-stu-id="5cf2f-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="5cf2f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cf2f-136">-Confirm</span></span>
<span data-ttu-id="5cf2f-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf2f-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5cf2f-138">-WhatIf</span></span>
<span data-ttu-id="5cf2f-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf2f-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf2f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf2f-141">CommonParameters</span></span>
<span data-ttu-id="5cf2f-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf2f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf2f-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf2f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf2f-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cf2f-144">INPUTS</span></span>

### <span data-ttu-id="5cf2f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5cf2f-145">System.String</span></span>

### <span data-ttu-id="5cf2f-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="5cf2f-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="5cf2f-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cf2f-147">OUTPUTS</span></span>

### <span data-ttu-id="5cf2f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cf2f-148">System.Boolean</span></span>

## <span data-ttu-id="5cf2f-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cf2f-149">NOTES</span></span>

## <span data-ttu-id="5cf2f-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cf2f-150">RELATED LINKS</span></span>
