---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 7e2b2bca042573ec96fefdf85e5077ec1138d1da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920627"
---
# <span data-ttu-id="b2cb0-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b2cb0-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="b2cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cb0-103">Entfernt Computeknoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="b2cb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2cb0-104">SYNTAX</span></span>

### <span data-ttu-id="b2cb0-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2cb0-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2cb0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b2cb0-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2cb0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="b2cb0-108">Das **Cmdlet Remove-AzBatchComputeNode** entfernt Azure Batch-Computeknoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="b2cb0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2cb0-109">EXAMPLES</span></span>

### <span data-ttu-id="b2cb0-110">Beispiel 1: Entfernen eines Computeknotens</span><span class="sxs-lookup"><span data-stu-id="b2cb0-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="b2cb0-111">Mit diesem Befehl wird der Computeknoten entfernt, der die angegebene ID aus dem Pool mit dem ID-Pool07 hat.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="b2cb0-112">Der Befehl gibt die Option Deallocation beenden an.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="b2cb0-113">Das Zeitfenster für die Größenänderung beträgt 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="b2cb0-114">Beispiel 2: Entfernen eines Computeknotens mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b2cb0-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="b2cb0-115">Dieser Befehl ruft den Computeknoten ab, der über die angegebene ID aus dem Pool verfügt, der über den ID-Pool07 verfügt, indem er das cmdlet Get-AzBatchComputeNode verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="b2cb0-116">Der Befehl übergibt diesen Knoten mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="b2cb0-117">Das aktuelle Cmdlet entfernt den Computeknoten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="b2cb0-118">Der Befehl gibt den Parameter *"Erzwingen"* an.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b2cb0-119">Daher werden Sie mit dem Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="b2cb0-120">Beispiel 3: Entfernen mehrerer Knoten</span><span class="sxs-lookup"><span data-stu-id="b2cb0-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="b2cb0-121">Mit diesem Befehl werden zwei Rechenknoten aus dem Pool entfernt, der über den ID-Pool07 verfügt.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="b2cb0-122">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b2cb0-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2cb0-123">PARAMETERS</span></span>

### <span data-ttu-id="b2cb0-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b2cb0-124">-BatchContext</span></span>
<span data-ttu-id="b2cb0-125">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b2cb0-126">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b2cb0-127">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b2cb0-128">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b2cb0-129">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="b2cb0-130">-ComputeNode</span></span>
<span data-ttu-id="b2cb0-131">Gibt das **PSComputeNode-Objekt** an, das den von diesem Cmdlet entfernten Computeknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="b2cb0-132">-DeallocationOption</span></span>
<span data-ttu-id="b2cb0-133">Gibt eine Deallocation-Option für den Entfernungsvorgang an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="b2cb0-134">Der Standardwert ist Requeue.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cb0-135">-DefaultProfile</span></span>
<span data-ttu-id="b2cb0-136">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cb0-137">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b2cb0-137">-Force</span></span>
<span data-ttu-id="b2cb0-138">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b2cb0-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="b2cb0-139">-Ids</span></span>
<span data-ttu-id="b2cb0-140">Gibt ein Array von IDs von Computeknoten an, das von diesem Cmdlet aus dem Pool entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b2cb0-141">-PoolId</span></span>
<span data-ttu-id="b2cb0-142">Gibt die ID des Pools an, der die von diesem Cmdlet entfernten Computeknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="b2cb0-143">-ResizeTimeout</span></span>
<span data-ttu-id="b2cb0-144">Gibt das Zeitintervall für das Entfernen der Computeknoten aus dem Pool an.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="b2cb0-145">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="b2cb0-146">Der Mindestwert beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2cb0-147">-Confirm</span></span>
<span data-ttu-id="b2cb0-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2cb0-149">-WhatIf</span></span>
<span data-ttu-id="b2cb0-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2cb0-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cb0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cb0-152">CommonParameters</span></span>
<span data-ttu-id="b2cb0-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cb0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cb0-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2cb0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cb0-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cb0-155">INPUTS</span></span>

### <span data-ttu-id="b2cb0-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="b2cb0-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="b2cb0-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2cb0-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b2cb0-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cb0-158">OUTPUTS</span></span>

### <span data-ttu-id="b2cb0-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="b2cb0-159">System.Void</span></span>

## <span data-ttu-id="b2cb0-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2cb0-160">NOTES</span></span>

## <span data-ttu-id="b2cb0-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2cb0-161">RELATED LINKS</span></span>

[<span data-ttu-id="b2cb0-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b2cb0-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b2cb0-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b2cb0-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="b2cb0-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="b2cb0-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


