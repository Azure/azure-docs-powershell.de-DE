---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: https://docs.microsoft.com/powershell/module/az.batch/reset-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Reset-AzBatchComputeNode.md
ms.openlocfilehash: c6ad25e5c6ba327ddcd5b4877cbac39937ec4feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935363"
---
# <span data-ttu-id="a4c0b-101">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4c0b-101">Reset-AzBatchComputeNode</span></span>

## <span data-ttu-id="a4c0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c0b-103">Installiert das Betriebssystem auf dem angegebenen Computeknoten erneut.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-103">Reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a4c0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4c0b-104">SYNTAX</span></span>

### <span data-ttu-id="a4c0b-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4c0b-105">Id (Default)</span></span>
```
Reset-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4c0b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c0b-106">InputObject</span></span>
```
Reset-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4c0b-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c0b-108">Das **Cmdlet Reset-AzBatchComputeNode** installiert das Betriebssystem auf dem angegebenen Computeknoten erneut.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-108">The **Reset-AzBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="a4c0b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4c0b-109">EXAMPLES</span></span>

### <span data-ttu-id="a4c0b-110">Beispiel 1: Erneutes Abbilden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="a4c0b-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="a4c0b-111">Mit diesem Befehl wird der Computeknoten mit der ID "tvm-3257026573_2-20150813t200938z" im Pool mit dem Namen MyPool erneut nachgebildet.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="a4c0b-112">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a4c0b-113">Beispiel 2: Erneutes Abbilden aller Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="a4c0b-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="a4c0b-114">Mit diesem Befehl wird jeder Computeknoten im Pool mit dem Namen "MyPool" neu abbilden.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="a4c0b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4c0b-115">PARAMETERS</span></span>

### <span data-ttu-id="a4c0b-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a4c0b-116">-BatchContext</span></span>
<span data-ttu-id="a4c0b-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4c0b-118">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4c0b-119">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4c0b-120">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4c0b-121">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a4c0b-122">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4c0b-122">-ComputeNode</span></span>
<span data-ttu-id="a4c0b-123">Gibt das **PSComputeNode-Objekt** an, das den zu reimageden Computeknoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-123">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="a4c0b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c0b-124">-DefaultProfile</span></span>
<span data-ttu-id="a4c0b-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c0b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="a4c0b-126">-Id</span></span>
<span data-ttu-id="a4c0b-127">Gibt die ID des zu erstellenden Computeknotens an.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-127">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="a4c0b-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a4c0b-128">-PoolId</span></span>
<span data-ttu-id="a4c0b-129">Gibt die ID des Pools an, der den Computeknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-129">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="a4c0b-130">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="a4c0b-130">-ReimageOption</span></span>
<span data-ttu-id="a4c0b-131">Gibt an, wann der Knoten neu nachbilden soll und was mit aktuell ausgeführten Aufgaben zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-131">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="a4c0b-132">Die Standardeinstellung ist Requeue.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-132">The default is Requeue.</span></span>

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

### <span data-ttu-id="a4c0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c0b-133">CommonParameters</span></span>
<span data-ttu-id="a4c0b-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c0b-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4c0b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c0b-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4c0b-136">INPUTS</span></span>

### <span data-ttu-id="a4c0b-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4c0b-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a4c0b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4c0b-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a4c0b-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4c0b-139">OUTPUTS</span></span>

### <span data-ttu-id="a4c0b-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="a4c0b-140">System.Void</span></span>

## <span data-ttu-id="a4c0b-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4c0b-141">NOTES</span></span>

## <span data-ttu-id="a4c0b-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4c0b-142">RELATED LINKS</span></span>

[<span data-ttu-id="a4c0b-143">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4c0b-143">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a4c0b-144">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4c0b-144">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="a4c0b-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a4c0b-145">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
