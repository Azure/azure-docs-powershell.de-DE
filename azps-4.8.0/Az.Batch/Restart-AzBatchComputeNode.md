---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/restart-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Restart-AzBatchComputeNode.md
ms.openlocfilehash: 41c6ea8e069e03a759c04f39018e2fa3a4d16834
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009389"
---
# <span data-ttu-id="d0e3c-101">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0e3c-101">Restart-AzBatchComputeNode</span></span>

## <span data-ttu-id="d0e3c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e3c-103">Startet den angegebenen Compute-Knoten neu.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-103">Reboots the specified compute node.</span></span>

## <span data-ttu-id="d0e3c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0e3c-104">SYNTAX</span></span>

### <span data-ttu-id="d0e3c-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0e3c-105">Id (Default)</span></span>
```
Restart-AzBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0e3c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e3c-106">InputObject</span></span>
```
Restart-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e3c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0e3c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e3c-108">Mit dem Cmdlet " **Restart-AzBatchComputeNode** " wird der angegebene Compute-Knoten neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-108">The **Restart-AzBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="d0e3c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0e3c-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e3c-110">Beispiel 1: Erneutes Starten eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="d0e3c-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="d0e3c-111">Mit diesem Befehl wird der Compute-Knoten mit der ID "TVM-3257026573_2-20150813t200938z" im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="d0e3c-112">Beispiel 2: Neustarten aller Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="d0e3c-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="d0e3c-113">Mit diesem Befehl wird jeder Compute-Knoten im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="d0e3c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0e3c-114">PARAMETERS</span></span>

### <span data-ttu-id="d0e3c-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="d0e3c-115">-BatchContext</span></span>
<span data-ttu-id="d0e3c-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0e3c-117">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d0e3c-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d0e3c-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d0e3c-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d0e3c-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0e3c-121">-ComputeNode</span></span>
<span data-ttu-id="d0e3c-122">Gibt das **PSComputeNode** -Objekt an, das den neu zu ladenden Compute-Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="d0e3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e3c-123">-DefaultProfile</span></span>
<span data-ttu-id="d0e3c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e3c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="d0e3c-125">-Id</span></span>
<span data-ttu-id="d0e3c-126">Gibt die ID des Compute-Knotens an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-126">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="d0e3c-127">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="d0e3c-127">-PoolId</span></span>
<span data-ttu-id="d0e3c-128">Gibt die ID des Pools an, der den Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="d0e3c-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="d0e3c-129">-RebootOption</span></span>
<span data-ttu-id="d0e3c-130">Gibt an, wann der Knoten neu gestartet wird und was mit aktuell ausgeführten Aufgaben geschieht.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="d0e3c-131">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-131">The default is Requeue.</span></span>

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

### <span data-ttu-id="d0e3c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e3c-132">CommonParameters</span></span>
<span data-ttu-id="d0e3c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e3c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e3c-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0e3c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e3c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0e3c-135">INPUTS</span></span>

### <span data-ttu-id="d0e3c-136">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0e3c-136">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d0e3c-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d0e3c-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d0e3c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0e3c-138">OUTPUTS</span></span>

### <span data-ttu-id="d0e3c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="d0e3c-139">System.Void</span></span>

## <span data-ttu-id="d0e3c-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0e3c-140">NOTES</span></span>

## <span data-ttu-id="d0e3c-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0e3c-141">RELATED LINKS</span></span>

[<span data-ttu-id="d0e3c-142">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0e3c-142">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d0e3c-143">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d0e3c-143">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="d0e3c-144">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d0e3c-144">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
