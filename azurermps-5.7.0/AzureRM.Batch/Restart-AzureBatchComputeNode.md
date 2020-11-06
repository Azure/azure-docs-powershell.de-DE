---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/restart-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: 5f32963630769dc25ed62f47d93fe47e56abda91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483157"
---
# <span data-ttu-id="98da6-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="98da6-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="98da6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98da6-102">SYNOPSIS</span></span>
<span data-ttu-id="98da6-103">Startet den angegebenen Compute-Knoten neu.</span><span class="sxs-lookup"><span data-stu-id="98da6-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98da6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98da6-104">SYNTAX</span></span>

### <span data-ttu-id="98da6-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="98da6-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98da6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98da6-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98da6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98da6-107">DESCRIPTION</span></span>
<span data-ttu-id="98da6-108">Mit dem Cmdlet " **Restart-AzureBatchComputeNode** " wird der angegebene Compute-Knoten neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="98da6-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="98da6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98da6-109">EXAMPLES</span></span>

### <span data-ttu-id="98da6-110">Beispiel 1: Erneutes Starten eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="98da6-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="98da6-111">Mit diesem Befehl wird der Compute-Knoten mit der ID "TVM-3257026573_2-20150813t200938z" im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="98da6-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="98da6-112">Beispiel 2: Neustarten aller Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="98da6-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="98da6-113">Mit diesem Befehl wird jeder Compute-Knoten im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="98da6-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="98da6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="98da6-114">PARAMETERS</span></span>

### <span data-ttu-id="98da6-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="98da6-115">-BatchContext</span></span>
<span data-ttu-id="98da6-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="98da6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98da6-117">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="98da6-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="98da6-118">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="98da6-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="98da6-119">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="98da6-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="98da6-120">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="98da6-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="98da6-121">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="98da6-121">-ComputeNode</span></span>
<span data-ttu-id="98da6-122">Gibt das **PSComputeNode** -Objekt an, das den neu zu ladenden Compute-Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="98da6-122">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="98da6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98da6-123">-DefaultProfile</span></span>
<span data-ttu-id="98da6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98da6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98da6-125">-ID</span><span class="sxs-lookup"><span data-stu-id="98da6-125">-Id</span></span>
<span data-ttu-id="98da6-126">Gibt die ID des Compute-Knotens an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98da6-126">Specifies the ID of the compute node to reboot.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98da6-127">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="98da6-127">-PoolId</span></span>
<span data-ttu-id="98da6-128">Gibt die ID des Pools an, der den Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="98da6-128">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="98da6-129">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="98da6-129">-RebootOption</span></span>
<span data-ttu-id="98da6-130">Gibt an, wann der Knoten neu gestartet wird und was mit aktuell ausgeführten Aufgaben geschieht.</span><span class="sxs-lookup"><span data-stu-id="98da6-130">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="98da6-131">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="98da6-131">The default is Requeue.</span></span>

```yaml
Type: ComputeNodeRebootOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98da6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98da6-132">CommonParameters</span></span>
<span data-ttu-id="98da6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98da6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98da6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98da6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98da6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98da6-135">INPUTS</span></span>

### <span data-ttu-id="98da6-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98da6-136">BatchAccountContext</span></span>
<span data-ttu-id="98da6-137">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="98da6-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="98da6-138">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="98da6-138">PSComputeNode</span></span>
<span data-ttu-id="98da6-139">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="98da6-139">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="98da6-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98da6-140">OUTPUTS</span></span>

## <span data-ttu-id="98da6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="98da6-141">NOTES</span></span>

## <span data-ttu-id="98da6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98da6-142">RELATED LINKS</span></span>

[<span data-ttu-id="98da6-143">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="98da6-143">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="98da6-144">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="98da6-144">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="98da6-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98da6-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


