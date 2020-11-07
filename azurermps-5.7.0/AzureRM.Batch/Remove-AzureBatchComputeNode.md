---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 6350505efe3f3e7c571fee6940cf678706c4fc7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664389"
---
# <span data-ttu-id="8f85f-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f85f-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="8f85f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f85f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f85f-103">Entfernt Compute-Knoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="8f85f-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f85f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f85f-104">SYNTAX</span></span>

### <span data-ttu-id="8f85f-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f85f-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f85f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8f85f-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f85f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f85f-107">DESCRIPTION</span></span>
<span data-ttu-id="8f85f-108">Das Cmdlet **Remove-AzureBatchComputeNode** entfernt Azure Batch Compute-Knoten aus einem Pool.</span><span class="sxs-lookup"><span data-stu-id="8f85f-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="8f85f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f85f-109">EXAMPLES</span></span>

### <span data-ttu-id="8f85f-110">Beispiel 1: Entfernen eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="8f85f-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="8f85f-111">Mit diesem Befehl wird Compute-Knoten mit der angegebenen ID aus Pool entfernt, die die ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="8f85f-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="8f85f-112">Der Befehl gibt die Option zum kündigen der Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="8f85f-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="8f85f-113">Die Größe des Timeouts beträgt 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8f85f-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="8f85f-114">Beispiel 2: Entfernen eines Compute-Knotens mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8f85f-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="8f85f-115">Dieser Befehl ruft den Compute-Knoten ab, der über die angegebene ID aus Pool verfügt, die über die ID-Pool07 mit dem Get-AzureBatchComputeNode-Cmdlet verfügt.</span><span class="sxs-lookup"><span data-stu-id="8f85f-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="8f85f-116">Der Befehl übergibt diesen Knoten mithilfe der Pipeline an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f85f-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="8f85f-117">Das aktuelle Cmdlet entfernt den Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="8f85f-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="8f85f-118">Der Befehl gibt den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="8f85f-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8f85f-119">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8f85f-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8f85f-120">Beispiel 3: Entfernen mehrerer Knoten</span><span class="sxs-lookup"><span data-stu-id="8f85f-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="8f85f-121">Mit diesem Befehl werden zwei Compute-Knoten aus dem Pool entfernt, die die ID Pool07.</span><span class="sxs-lookup"><span data-stu-id="8f85f-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="8f85f-122">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="8f85f-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8f85f-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f85f-123">PARAMETERS</span></span>

### <span data-ttu-id="8f85f-124">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="8f85f-124">-BatchContext</span></span>
<span data-ttu-id="8f85f-125">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f85f-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8f85f-126">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f85f-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8f85f-127">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f85f-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8f85f-128">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f85f-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8f85f-129">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="8f85f-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f85f-130">-ComputeNode</span></span>
<span data-ttu-id="8f85f-131">Gibt das **PSComputeNode** -Objekt an, das den Compute-Knoten darstellt, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="8f85f-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="8f85f-132">-DeallocationOption</span></span>
<span data-ttu-id="8f85f-133">Gibt eine Option für die Freigabe für den Löschvorgang an, den dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="8f85f-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="8f85f-134">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="8f85f-134">The default value is Requeue.</span></span>

```yaml
Type: ComputeNodeDeallocationOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f85f-135">-DefaultProfile</span></span>
<span data-ttu-id="8f85f-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f85f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-137">-Force</span><span class="sxs-lookup"><span data-stu-id="8f85f-137">-Force</span></span>
<span data-ttu-id="8f85f-138">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8f85f-138">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-139">-IDs</span><span class="sxs-lookup"><span data-stu-id="8f85f-139">-Ids</span></span>
<span data-ttu-id="8f85f-140">Gibt ein Array von IDs von Compute-Knoten an, die von diesem Cmdlet aus dem Pool entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8f85f-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-141">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="8f85f-141">-PoolId</span></span>
<span data-ttu-id="8f85f-142">Gibt die ID des Pools an, der die Compute-Knoten enthält, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8f85f-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8f85f-143">-ResizeTimeout</span></span>
<span data-ttu-id="8f85f-144">Gibt das Timeoutintervall für das Entfernen der Compute-Knoten aus dem Pool an.</span><span class="sxs-lookup"><span data-stu-id="8f85f-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="8f85f-145">Der Standardwert ist 10 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8f85f-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="8f85f-146">Der Mindestwert beträgt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="8f85f-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f85f-147">-Confirm</span></span>
<span data-ttu-id="8f85f-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f85f-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f85f-149">-WhatIf</span></span>
<span data-ttu-id="8f85f-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f85f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f85f-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f85f-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f85f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f85f-152">CommonParameters</span></span>
<span data-ttu-id="8f85f-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f85f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f85f-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f85f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f85f-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f85f-155">INPUTS</span></span>

### <span data-ttu-id="8f85f-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8f85f-156">BatchAccountContext</span></span>
<span data-ttu-id="8f85f-157">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f85f-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8f85f-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f85f-158">PSComputeNode</span></span>
<span data-ttu-id="8f85f-159">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f85f-159">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="8f85f-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f85f-160">OUTPUTS</span></span>

## <span data-ttu-id="8f85f-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f85f-161">NOTES</span></span>

## <span data-ttu-id="8f85f-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f85f-162">RELATED LINKS</span></span>

[<span data-ttu-id="8f85f-163">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f85f-163">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8f85f-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f85f-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="8f85f-165">Neustart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="8f85f-165">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


