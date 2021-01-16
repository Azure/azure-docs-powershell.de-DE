---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: ff8c758b5e384fbab8f690030eb8a7fbe35c79f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294634"
---
# <span data-ttu-id="1476b-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1476b-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="1476b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1476b-102">SYNOPSIS</span></span>
<span data-ttu-id="1476b-103">Installiert das Betriebssystem erneut auf dem angegebenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="1476b-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="1476b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1476b-104">SYNTAX</span></span>

### <span data-ttu-id="1476b-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="1476b-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1476b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1476b-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1476b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1476b-107">DESCRIPTION</span></span>
<span data-ttu-id="1476b-108">Das **Cmdlet "Reset-AzBatchComputeNode"** installiert das Betriebssystem auf dem angegebenen Rechenknoten erneut.</span><span class="sxs-lookup"><span data-stu-id="1476b-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="1476b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1476b-109">EXAMPLES</span></span>

### <span data-ttu-id="1476b-110">Beispiel 1: Erneutes Abbilden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="1476b-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="1476b-111">Dieser Befehl reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span><span class="sxs-lookup"><span data-stu-id="1476b-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="1476b-112">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1476b-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1476b-113">Beispiel 2: Erneutes Abbilden aller Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="1476b-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="1476b-114">Dieser Befehl reimages jeden Rechenknoten im Pool namens "MyPool".</span><span class="sxs-lookup"><span data-stu-id="1476b-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="1476b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1476b-115">PARAMETERS</span></span>

### <span data-ttu-id="1476b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1476b-116">-BatchContext</span></span>
<span data-ttu-id="1476b-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1476b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1476b-118">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1476b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1476b-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1476b-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1476b-120">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1476b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1476b-121">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1476b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1476b-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1476b-122">-ComputeNode</span></span>
<span data-ttu-id="1476b-123">Gibt das **PSComputeNode-Objekt** an, das den zu reimagedenden Computeknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="1476b-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="1476b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1476b-124">-DefaultProfile</span></span>
<span data-ttu-id="1476b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1476b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1476b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1476b-126">-Id</span></span>
<span data-ttu-id="1476b-127">Gibt die ID des zu reimagedenden Computeknotens an.</span><span class="sxs-lookup"><span data-stu-id="1476b-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="1476b-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1476b-128">-PoolId</span></span>
<span data-ttu-id="1476b-129">Gibt die ID des Pools an, der den Rechenknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="1476b-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="1476b-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="1476b-130">-ReimageOption</span></span>
<span data-ttu-id="1476b-131">Gibt an, wann der Knoten neu nachbebildert werden soll und was mit derzeit ausgeführten Aufgaben zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="1476b-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="1476b-132">Die Standardeinstellung ist "Erneut festlegen".</span><span class="sxs-lookup"><span data-stu-id="1476b-132">The default is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeReimageOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1476b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1476b-133">CommonParameters</span></span>
<span data-ttu-id="1476b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1476b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1476b-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1476b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1476b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1476b-136">INPUTS</span></span>

### <span data-ttu-id="1476b-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1476b-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="1476b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1476b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1476b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1476b-139">OUTPUTS</span></span>

### <span data-ttu-id="1476b-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="1476b-140">System.Void</span></span>

## <span data-ttu-id="1476b-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1476b-141">NOTES</span></span>

## <span data-ttu-id="1476b-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1476b-142">RELATED LINKS</span></span>

[<span data-ttu-id="1476b-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1476b-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="1476b-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1476b-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="1476b-145">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1476b-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
