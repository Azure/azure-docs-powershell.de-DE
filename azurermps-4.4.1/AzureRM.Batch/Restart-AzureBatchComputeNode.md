---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 029361F0-C4E9-4948-9EBA-BFBD1B029909
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Restart-AzureBatchComputeNode.md
ms.openlocfilehash: eff141494c2b34622f35b687dd1803c449e8b727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500942"
---
# <span data-ttu-id="cf7eb-101">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-101">Restart-AzureBatchComputeNode</span></span>

## <span data-ttu-id="cf7eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7eb-103">Startet den angegebenen Compute-Knoten neu.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-103">Reboots the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf7eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf7eb-104">SYNTAX</span></span>

### <span data-ttu-id="cf7eb-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf7eb-105">Id (Default)</span></span>
```
Restart-AzureBatchComputeNode [-PoolId] <String> [-Id] <String> [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf7eb-106">InputObject</span></span>
```
Restart-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>] [[-RebootOption] <ComputeNodeRebootOption>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf7eb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf7eb-107">DESCRIPTION</span></span>
<span data-ttu-id="cf7eb-108">Mit dem Cmdlet " **Restart-AzureBatchComputeNode** " wird der angegebene Compute-Knoten neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-108">The **Restart-AzureBatchComputeNode** cmdlet reboots the specified compute node.</span></span>

## <span data-ttu-id="cf7eb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf7eb-109">EXAMPLES</span></span>

### <span data-ttu-id="cf7eb-110">Beispiel 1: Erneutes Starten eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="cf7eb-110">Example 1: Restart a compute node</span></span>
```
PS C:\>Restart-AzureBatchComputeNode -PoolId "MyPool" -Id "tvm-3257026573_2-20150813t200938z" -BatchContext $Context
```

<span data-ttu-id="cf7eb-111">Mit diesem Befehl wird der Compute-Knoten mit der ID "TVM-3257026573_2-20150813t200938z" im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-111">This command reboots the compute node with the ID "tvm-3257026573_2-20150813t200938z" in the pool MyPool.</span></span>

### <span data-ttu-id="cf7eb-112">Beispiel 2: Neustarten aller Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="cf7eb-112">Example 2: Restart every compute node in a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "MyPool" -BatchContext $Context | Restart-AzureBatchComputeNode -BatchContext $Context
```

<span data-ttu-id="cf7eb-113">Mit diesem Befehl wird jeder Compute-Knoten im Pool MyPool neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-113">This command reboots every compute node in the pool MyPool.</span></span>

## <span data-ttu-id="cf7eb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf7eb-114">PARAMETERS</span></span>

### <span data-ttu-id="cf7eb-115">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="cf7eb-115">-BatchContext</span></span>
<span data-ttu-id="cf7eb-116">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf7eb-117">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="cf7eb-118">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-118">-ComputeNode</span></span>
<span data-ttu-id="cf7eb-119">Gibt das **PSComputeNode** -Objekt an, das den neu zu ladenden Compute-Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-119">Specifies the **PSComputeNode** object that represents the compute node to reboot.</span></span>

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

### <span data-ttu-id="cf7eb-120">-ID</span><span class="sxs-lookup"><span data-stu-id="cf7eb-120">-Id</span></span>
<span data-ttu-id="cf7eb-121">Gibt die ID des Compute-Knotens an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-121">Specifies the ID of the compute node to reboot.</span></span>

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

### <span data-ttu-id="cf7eb-122">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="cf7eb-122">-PoolId</span></span>
<span data-ttu-id="cf7eb-123">Gibt die ID des Pools an, der den Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-123">Specifies the ID of the pool that contains the compute node.</span></span>

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

### <span data-ttu-id="cf7eb-124">-RebootOption</span><span class="sxs-lookup"><span data-stu-id="cf7eb-124">-RebootOption</span></span>
<span data-ttu-id="cf7eb-125">Gibt an, wann der Knoten neu gestartet wird und was mit aktuell ausgeführten Aufgaben geschieht.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-125">Specifies when to reboot the node and what to do with currently running tasks.</span></span>
<span data-ttu-id="cf7eb-126">Der Standardwert ist requeue.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-126">The default is Requeue.</span></span>

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

### <span data-ttu-id="cf7eb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7eb-127">-DefaultProfile</span></span>
<span data-ttu-id="cf7eb-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf7eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7eb-129">CommonParameters</span></span>
<span data-ttu-id="cf7eb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7eb-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7eb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7eb-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf7eb-132">INPUTS</span></span>

### <span data-ttu-id="cf7eb-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf7eb-133">BatchAccountContext</span></span>
<span data-ttu-id="cf7eb-134">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="cf7eb-135">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-135">PSComputeNode</span></span>
<span data-ttu-id="cf7eb-136">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf7eb-136">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="cf7eb-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf7eb-137">OUTPUTS</span></span>

## <span data-ttu-id="cf7eb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf7eb-138">NOTES</span></span>

## <span data-ttu-id="cf7eb-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf7eb-139">RELATED LINKS</span></span>

[<span data-ttu-id="cf7eb-140">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-140">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="cf7eb-141">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cf7eb-141">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="cf7eb-142">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cf7eb-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


