---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308096"
---
# <span data-ttu-id="8e63b-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e63b-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="8e63b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e63b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e63b-103">Entfernt Berechnungsknoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="8e63b-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="8e63b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e63b-104">SYNTAX</span></span>

### <span data-ttu-id="8e63b-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e63b-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e63b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e63b-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e63b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e63b-107">DESCRIPTION</span></span>
<span data-ttu-id="8e63b-108">Das **Cmdlet "Remove-AzBatchComputeNode"** entfernt Azure Batch-Berechnungsknoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="8e63b-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8e63b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e63b-109">EXAMPLES</span></span>

### <span data-ttu-id="8e63b-110">Beispiel 1: Entfernen eines Rechenknotens</span><span class="sxs-lookup"><span data-stu-id="8e63b-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="8e63b-111">Mit diesem Befehl wird der Rechenknoten entfernt, der die angegebene ID aus dem Pool mit dem ID Pool07 hat.</span><span class="sxs-lookup"><span data-stu-id="8e63b-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="8e63b-112">Der Befehl gibt die Option "Deallocation beenden" an.</span><span class="sxs-lookup"><span data-stu-id="8e63b-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="8e63b-113">Das Zeitfenster für die Größenänderung beträgt 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8e63b-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="8e63b-114">Beispiel 2: Entfernen eines Rechenknotens mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8e63b-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="8e63b-115">Mit diesem Befehl wird mithilfe des cmdlets "Get-AzBatchComputeNode" der Rechenknoten mit der angegebenen ID aus dem Pool mit dem ID Pool07 ruft.</span><span class="sxs-lookup"><span data-stu-id="8e63b-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="8e63b-116">Der Befehl übergibt diesen Knoten mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e63b-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="8e63b-117">Das aktuelle Cmdlet entfernt den Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="8e63b-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="8e63b-118">Der Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="8e63b-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8e63b-119">Daher fordert Sie der Befehl nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="8e63b-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8e63b-120">Beispiel 3: Entfernen mehrerer Knoten</span><span class="sxs-lookup"><span data-stu-id="8e63b-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="8e63b-121">Mit diesem Befehl werden zwei Berechnungsknoten aus dem Pool entfernt, der den ID Pool07 enthält.</span><span class="sxs-lookup"><span data-stu-id="8e63b-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="8e63b-122">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="8e63b-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e63b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e63b-123">PARAMETERS</span></span>

### <span data-ttu-id="8e63b-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8e63b-124">-BatchContext</span></span>
<span data-ttu-id="8e63b-125">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e63b-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8e63b-126">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e63b-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8e63b-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8e63b-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8e63b-128">Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e63b-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8e63b-129">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e63b-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8e63b-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e63b-130">-ComputeNode</span></span>
<span data-ttu-id="8e63b-131">Gibt das **PSComputeNode-Objekt** an, das den von diesem Cmdlet entfernten Rechenknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="8e63b-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e63b-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="8e63b-132">-DeallocationOption</span></span>
<span data-ttu-id="8e63b-133">Gibt eine Deallocationoption für den Entfernungsvorgang an, der mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="8e63b-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="8e63b-134">Der Standardwert ist "Requeue".</span><span class="sxs-lookup"><span data-stu-id="8e63b-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="8e63b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e63b-135">-DefaultProfile</span></span>
<span data-ttu-id="8e63b-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e63b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e63b-137">-Force</span><span class="sxs-lookup"><span data-stu-id="8e63b-137">-Force</span></span>
<span data-ttu-id="8e63b-138">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="8e63b-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e63b-139">-Ids</span><span class="sxs-lookup"><span data-stu-id="8e63b-139">-Ids</span></span>
<span data-ttu-id="8e63b-140">Gibt ein Array von IDs von Rechenknoten an, das von diesem Cmdlet aus dem Pool entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8e63b-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="8e63b-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="8e63b-141">-PoolId</span></span>
<span data-ttu-id="8e63b-142">Gibt die ID des Pools an, der die von diesem Cmdlet entfernten Rechenknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="8e63b-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e63b-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8e63b-143">-ResizeTimeout</span></span>
<span data-ttu-id="8e63b-144">Gibt das Zeitintervall für das Entfernen der Berechnungsknoten aus dem Pool an.</span><span class="sxs-lookup"><span data-stu-id="8e63b-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="8e63b-145">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8e63b-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="8e63b-146">Der Mindestwert beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8e63b-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="8e63b-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e63b-147">-Confirm</span></span>
<span data-ttu-id="8e63b-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e63b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e63b-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e63b-149">-WhatIf</span></span>
<span data-ttu-id="8e63b-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e63b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e63b-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e63b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e63b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e63b-152">CommonParameters</span></span>
<span data-ttu-id="8e63b-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e63b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e63b-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e63b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e63b-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-155">INPUTS</span></span>

### <span data-ttu-id="8e63b-156">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e63b-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="8e63b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e63b-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e63b-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-158">OUTPUTS</span></span>

### <span data-ttu-id="8e63b-159">System.Void</span><span class="sxs-lookup"><span data-stu-id="8e63b-159">System.Void</span></span>

## <span data-ttu-id="8e63b-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e63b-160">NOTES</span></span>

## <span data-ttu-id="8e63b-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-161">RELATED LINKS</span></span>

[<span data-ttu-id="8e63b-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="8e63b-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="8e63b-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e63b-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="8e63b-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8e63b-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


