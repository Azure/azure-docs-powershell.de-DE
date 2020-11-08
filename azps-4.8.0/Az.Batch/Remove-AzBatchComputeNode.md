---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010042"
---
# <span data-ttu-id="71ca9-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="71ca9-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="71ca9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="71ca9-103">Entfernt Compute-Knoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="71ca9-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="71ca9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ca9-104">SYNTAX</span></span>

### <span data-ttu-id="71ca9-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="71ca9-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71ca9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="71ca9-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71ca9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71ca9-107">DESCRIPTION</span></span>
<span data-ttu-id="71ca9-108">Das Cmdlet **Remove-AzBatchComputeNode** entfernt Azure Batch Compute-Knoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="71ca9-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="71ca9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71ca9-109">EXAMPLES</span></span>

### <span data-ttu-id="71ca9-110">Beispiel 1: Entfernen eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="71ca9-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="71ca9-111">Mit diesem Befehl wird Compute-Knoten mit der angegebenen ID aus Pool entfernt, die die ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="71ca9-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="71ca9-112">Der Befehl gibt die Option zum kündigen der Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="71ca9-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="71ca9-113">Die Größe des Timeouts beträgt 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="71ca9-114">Beispiel 2: Entfernen eines Compute-Knotens mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="71ca9-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="71ca9-115">Dieser Befehl ruft den Compute-Knoten ab, der über die angegebene ID aus Pool verfügt, die über die ID-Pool07 mit dem Get-AzBatchComputeNode-Cmdlet verfügt.</span><span class="sxs-lookup"><span data-stu-id="71ca9-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="71ca9-116">Der Befehl übergibt diesen Knoten mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71ca9-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="71ca9-117">Das aktuelle Cmdlet entfernt den Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="71ca9-118">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="71ca9-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="71ca9-119">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="71ca9-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="71ca9-120">Beispiel 3: Entfernen mehrerer Knoten</span><span class="sxs-lookup"><span data-stu-id="71ca9-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="71ca9-121">Mit diesem Befehl werden zwei Compute-Knoten aus dem Pool entfernt, die die ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="71ca9-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="71ca9-122">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="71ca9-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="71ca9-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="71ca9-123">PARAMETERS</span></span>

### <span data-ttu-id="71ca9-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="71ca9-124">-BatchContext</span></span>
<span data-ttu-id="71ca9-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="71ca9-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="71ca9-126">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="71ca9-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="71ca9-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="71ca9-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="71ca9-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="71ca9-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="71ca9-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="71ca9-130">-ComputeNode</span></span>
<span data-ttu-id="71ca9-131">Gibt das **PSComputeNode** -Objekt an, das den Compute-Knoten darstellt, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="71ca9-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71ca9-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="71ca9-132">-DeallocationOption</span></span>
<span data-ttu-id="71ca9-133">Gibt eine Option für die Freigabe für den Löschvorgang an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="71ca9-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="71ca9-134">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="71ca9-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="71ca9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ca9-135">-DefaultProfile</span></span>
<span data-ttu-id="71ca9-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71ca9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ca9-137">-Force</span><span class="sxs-lookup"><span data-stu-id="71ca9-137">-Force</span></span>
<span data-ttu-id="71ca9-138">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="71ca9-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71ca9-139">-IDs</span><span class="sxs-lookup"><span data-stu-id="71ca9-139">-Ids</span></span>
<span data-ttu-id="71ca9-140">Gibt ein Array von IDs von Compute-Knoten an, die von diesem Cmdlet aus dem Pool entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="71ca9-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="71ca9-141">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="71ca9-141">-PoolId</span></span>
<span data-ttu-id="71ca9-142">Gibt die ID des Pools an, der die Compute-Knoten enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="71ca9-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71ca9-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="71ca9-143">-ResizeTimeout</span></span>
<span data-ttu-id="71ca9-144">Gibt das Timeoutintervall für das Entfernen der Compute-Knoten aus dem Pool an.</span><span class="sxs-lookup"><span data-stu-id="71ca9-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="71ca9-145">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="71ca9-146">Der Mindestwert beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="71ca9-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71ca9-147">-Confirm</span></span>
<span data-ttu-id="71ca9-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ca9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ca9-149">-WhatIf</span></span>
<span data-ttu-id="71ca9-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71ca9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ca9-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71ca9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ca9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ca9-152">CommonParameters</span></span>
<span data-ttu-id="71ca9-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ca9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ca9-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71ca9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ca9-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71ca9-155">INPUTS</span></span>

### <span data-ttu-id="71ca9-156">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="71ca9-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="71ca9-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="71ca9-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="71ca9-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71ca9-158">OUTPUTS</span></span>

### <span data-ttu-id="71ca9-159">System. void</span><span class="sxs-lookup"><span data-stu-id="71ca9-159">System.Void</span></span>

## <span data-ttu-id="71ca9-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="71ca9-160">NOTES</span></span>

## <span data-ttu-id="71ca9-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71ca9-161">RELATED LINKS</span></span>

[<span data-ttu-id="71ca9-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="71ca9-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="71ca9-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="71ca9-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="71ca9-164">Neustart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="71ca9-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)


