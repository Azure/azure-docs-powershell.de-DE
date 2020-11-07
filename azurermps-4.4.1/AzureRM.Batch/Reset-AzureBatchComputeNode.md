---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A202537B-D292-4822-A0B9-27A6A20621D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Reset-AzureBatchComputeNode.md
ms.openlocfilehash: b90a70bb6b4a8104597056715c75f5699db5a24e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663088"
---
# <span data-ttu-id="0e375-101">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0e375-101">Reset-AzureBatchComputeNode</span></span>

## <span data-ttu-id="0e375-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e375-102">SYNOPSIS</span></span>
<span data-ttu-id="0e375-103">Neuinstallation des Betriebssystems auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="0e375-103">Reinstalls the operating system on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e375-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e375-104">SYNTAX</span></span>

### <span data-ttu-id="0e375-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e375-105">Id (Default)</span></span>
```
Reset-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e375-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e375-106">InputObject</span></span>
```
Reset-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [-ReimageOption <ComputeNodeReimageOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e375-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e375-107">DESCRIPTION</span></span>
<span data-ttu-id="0e375-108">Mit dem Cmdlet **Reset-AzureBatchComputeNode** wird das Betriebssystem auf dem angegebenen Compute-Knoten neu installiert.</span><span class="sxs-lookup"><span data-stu-id="0e375-108">The **Reset-AzureBatchComputeNode** cmdlet reinstalls the operating system on the specified compute node.</span></span>

## <span data-ttu-id="0e375-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e375-109">EXAMPLES</span></span>

### <span data-ttu-id="0e375-110">Beispiel 1: umbilden eines Knotens</span><span class="sxs-lookup"><span data-stu-id="0e375-110">Example 1: Reimage a node</span></span>
```
PS C:\>Reset-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="0e375-111">Mit diesem Befehl wird der Compute-Knoten mit der ID "TVM-3257026573_2-20150813t200938z" im Pool mit dem Namen MyPool neu abbildet.</span><span class="sxs-lookup"><span data-stu-id="0e375-111">This command reimages the compute node with ID "tvm-3257026573_2-20150813t200938z" in the pool named MyPool.</span></span>
<span data-ttu-id="0e375-112">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0e375-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0e375-113">Beispiel 2: umbilden aller Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="0e375-113">Example 2: Reimage all nodes in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Reset-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="0e375-114">Mit diesem Befehl wird jeder Compute-Knoten im Pool mit dem Namen MyPool neu abbildet.</span><span class="sxs-lookup"><span data-stu-id="0e375-114">This command reimages every compute node in the pool named MyPool.</span></span>

## <span data-ttu-id="0e375-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e375-115">PARAMETERS</span></span>

### <span data-ttu-id="0e375-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="0e375-116">-BatchContext</span></span>
<span data-ttu-id="0e375-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e375-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0e375-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e375-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0e375-119">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="0e375-119">-ComputeNode</span></span>
<span data-ttu-id="0e375-120">Gibt das **PSComputeNode** -Objekt an, das den Compute-Knoten für das neubild darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e375-120">Specifies the **PSComputeNode** object that represents the compute node to reimage.</span></span>

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

### <span data-ttu-id="0e375-121">-ID</span><span class="sxs-lookup"><span data-stu-id="0e375-121">-Id</span></span>
<span data-ttu-id="0e375-122">Gibt die ID des zu rebildenden Compute-Knotens an.</span><span class="sxs-lookup"><span data-stu-id="0e375-122">Specifies the ID of the compute node to reimage.</span></span>

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

### <span data-ttu-id="0e375-123">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="0e375-123">-PoolId</span></span>
<span data-ttu-id="0e375-124">Gibt die ID des Pools an, der den Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="0e375-124">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="0e375-125">-ReimageOption</span><span class="sxs-lookup"><span data-stu-id="0e375-125">-ReimageOption</span></span>
<span data-ttu-id="0e375-126">Gibt an, wann der Knoten erneut dargestellt werden soll und was mit aktuell ausgeführten Aufgaben geschieht.</span><span class="sxs-lookup"><span data-stu-id="0e375-126">Specifies when to reimage the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="0e375-127">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="0e375-127">The default is Requeue.</span></span>

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

### <span data-ttu-id="0e375-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e375-128">-DefaultProfile</span></span>
<span data-ttu-id="0e375-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e375-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e375-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e375-130">CommonParameters</span></span>
<span data-ttu-id="0e375-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e375-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e375-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e375-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e375-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e375-133">INPUTS</span></span>

### <span data-ttu-id="0e375-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0e375-134">BatchAccountContext</span></span>
<span data-ttu-id="0e375-135">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e375-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="0e375-136">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="0e375-136">PSComputeNode</span></span>
<span data-ttu-id="0e375-137">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0e375-137">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="0e375-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e375-138">OUTPUTS</span></span>

## <span data-ttu-id="0e375-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e375-139">NOTES</span></span>

## <span data-ttu-id="0e375-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e375-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e375-141">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0e375-141">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="0e375-142">Neustart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="0e375-142">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="0e375-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0e375-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


