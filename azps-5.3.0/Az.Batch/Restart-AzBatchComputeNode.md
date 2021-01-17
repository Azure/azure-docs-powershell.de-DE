---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471111"
---
# <span data-ttu-id="e9bc4-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9bc4-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="e9bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bc4-103">Der angegebene Rechenknoten wird neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="e9bc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9bc4-104">SYNTAX</span></span>

### <span data-ttu-id="e9bc4-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9bc4-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9bc4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e9bc4-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9bc4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bc4-108">Das **Cmdlet "Restart-AzBatchComputeNode"** startet den angegebenen Rechenknoten neu.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="e9bc4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="e9bc4-110">Beispiel 1: Neustarten eines Rechenknotens</span><span class="sxs-lookup"><span data-stu-id="e9bc4-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="e9bc4-111">Dieser Befehl startet den Rechenknoten mit der ID "tvm-3257026573_2-20150813t200938z" im MyPool-Pool neu.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="e9bc4-112">Beispiel 2: Neustarten aller Rechenknoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="e9bc4-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="e9bc4-113">Mit diesem Befehl wird jeder Rechenknoten im MyPool-Pool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="e9bc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9bc4-114">PARAMETERS</span></span>

### <span data-ttu-id="e9bc4-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e9bc4-115">-BatchContext</span></span>
<span data-ttu-id="e9bc4-116">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e9bc4-117">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e9bc4-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e9bc4-119">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e9bc4-120">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e9bc4-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9bc4-121">-ComputeNode</span></span>
<span data-ttu-id="e9bc4-122">Gibt das **PSComputeNode-Objekt** an, das den neu zu startenden Computeknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="e9bc4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bc4-123">-DefaultProfile</span></span>
<span data-ttu-id="e9bc4-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9bc4-125">-ID</span><span class="sxs-lookup"><span data-stu-id="e9bc4-125">-Id</span></span>
<span data-ttu-id="e9bc4-126">Gibt die ID des neu zu startenden Rechenknotens an.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-126">Specifies the ID of the compute node to reboot.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc4-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e9bc4-127">-PoolId</span></span>
<span data-ttu-id="e9bc4-128">Gibt die ID des Pools an, der den Rechenknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="e9bc4-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="e9bc4-129">-RebootOption</span></span>
<span data-ttu-id="e9bc4-130">Gibt an, wann der Knoten neu gestartet werden soll und was mit den derzeit ausgeführten Aufgaben zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="e9bc4-131">Die Standardeinstellung ist "Erneut festlegen".</span><span class="sxs-lookup"><span data-stu-id="e9bc4-131">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeRebootOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bc4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bc4-132">CommonParameters</span></span>
<span data-ttu-id="e9bc4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bc4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bc4-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9bc4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bc4-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9bc4-135">INPUTS</span></span>

### <span data-ttu-id="e9bc4-136">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9bc4-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="e9bc4-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e9bc4-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e9bc4-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9bc4-138">OUTPUTS</span></span>

### <span data-ttu-id="e9bc4-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="e9bc4-139">System.Void</span></span>

## <span data-ttu-id="e9bc4-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9bc4-140">NOTES</span></span>

## <span data-ttu-id="e9bc4-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9bc4-141">RELATED LINKS</span></span>

[<span data-ttu-id="e9bc4-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9bc4-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="e9bc4-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e9bc4-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="e9bc4-144">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e9bc4-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
