---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 778347394e9793b95434e1b308bbdb4e28fc0915
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502789"
---
# <span data-ttu-id="735b6-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="735b6-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="735b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="735b6-102">SYNOPSIS</span></span>
<span data-ttu-id="735b6-103">Deaktiviert die Vorgangsplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="735b6-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="735b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="735b6-104">SYNTAX</span></span>

### <span data-ttu-id="735b6-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="735b6-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="735b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="735b6-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735b6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="735b6-107">DESCRIPTION</span></span>
<span data-ttu-id="735b6-108">Das Cmdlet **Disable-AzureBatchComputeNodeScheduling** deaktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="735b6-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="735b6-109">Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="735b6-110">Wenn Sie die Vorgangsplanung auf einem Compute-Knoten deaktivieren, können Sie auch bestimmen, was zu den Aufträgen aktuell in der Aufgabenwarteschlange des Knotens zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="735b6-111">Mit **Disable-AzureBatchComputeNodeScheduling** können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="735b6-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="735b6-112">Kündigen Sie die Aufgaben, und setzen Sie Sie wieder in die Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="735b6-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="735b6-113">Dadurch können diese Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="735b6-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="735b6-114">Kündigen Sie die Aufgaben, und entfernen Sie Sie aus der Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="735b6-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="735b6-115">Auf diese Weise gestoppte Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="735b6-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="735b6-116">Warten Sie, bis alle zurzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="735b6-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="735b6-117">Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Datenaufbewahrungszeiträume abgelaufen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="735b6-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="735b6-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="735b6-118">EXAMPLES</span></span>

### <span data-ttu-id="735b6-119">Beispiel 1: Deaktivieren der Vorgangsplanung auf einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="735b6-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="735b6-120">Diese Befehle deaktivieren den Aufgabenplan auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="735b6-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="735b6-121">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="735b6-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="735b6-122">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="735b6-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="735b6-123">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **Disable-AzureBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf dem Knoten TVM-1783593343_34-20151117t222514z zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="735b6-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="735b6-124">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle zurzeit auf dem Compute-Knoten ausgeführten Aufgaben erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="735b6-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="735b6-125">Beispiel 2: Deaktivieren der Vorgangsplanung für alle Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="735b6-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="735b6-126">Diese Befehle deaktivieren die Aufgabenplanung auf allen Computerknoten im Batch Pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="735b6-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="735b6-127">Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für die contosobatchaccount des Batch Kontos.</span><span class="sxs-lookup"><span data-stu-id="735b6-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="735b6-128">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="735b6-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="735b6-129">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzureBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="735b6-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="735b6-130">Diese Sammlung wird dann an das Cmdlet **Disable-AzureBatchComputeNodeScheduling** umgeleitet, um die Aufgabenplanung für jeden Compute-Knoten in der Sammlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="735b6-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="735b6-131">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle Aufgaben, die derzeit auf den Compute-Knoten ausgeführt werden, erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="735b6-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="735b6-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="735b6-132">PARAMETERS</span></span>

### <span data-ttu-id="735b6-133">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="735b6-133">-BatchContext</span></span>
<span data-ttu-id="735b6-134">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="735b6-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="735b6-135">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="735b6-135">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="735b6-136">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="735b6-136">-ComputeNode</span></span>
<span data-ttu-id="735b6-137">Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-137">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="735b6-138">Dieser Objektverweis wird mithilfe des Get-AzureBatchComputeNode-Cmdlets erstellt und speichert das zurückgegebene Compute-Knotenobjekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="735b6-138">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="735b6-139">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="735b6-139">-DisableSchedulingOption</span></span>
<span data-ttu-id="735b6-140">Gibt an, wie sich dieses Cmdlet auf alle Aufgaben bezieht, die derzeit auf dem Computerknoten ausgeführt werden, auf dem die Planung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-140">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="735b6-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="735b6-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="735b6-142">Erneute Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="735b6-142">Requeue.</span></span>
<span data-ttu-id="735b6-143">Aufgaben werden sofort angehalten und an die Job-Warteschlange zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="735b6-143">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="735b6-144">Dadurch können die Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="735b6-144">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="735b6-145">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="735b6-145">This is the default value.</span></span> 
- <span data-ttu-id="735b6-146">Beenden.</span><span class="sxs-lookup"><span data-stu-id="735b6-146">Terminate.</span></span>
<span data-ttu-id="735b6-147">Aufgaben werden sofort angehalten und aus der Job-Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="735b6-147">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="735b6-148">Diese Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="735b6-148">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="735b6-149">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="735b6-149">TaskCompletion.</span></span>
<span data-ttu-id="735b6-150">Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Vorgangsplanung auf dem Compute-Knoten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-150">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="735b6-151">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="735b6-151">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="735b6-152">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="735b6-152">RetainedData.</span></span>
<span data-ttu-id="735b6-153">Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung auf dem Compute-Knoten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="735b6-153">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="735b6-154">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="735b6-154">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="735b6-155">-ID</span><span class="sxs-lookup"><span data-stu-id="735b6-155">-Id</span></span>
<span data-ttu-id="735b6-156">Gibt die ID des Compute-Knotens an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-156">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="735b6-157">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="735b6-157">-PoolId</span></span>
<span data-ttu-id="735b6-158">Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="735b6-158">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="735b6-159">Wenn Sie den *Pool* -Parameter verwenden, verwenden Sie den *ComputeNode* -Parameter nicht in demselben Befehl.</span><span class="sxs-lookup"><span data-stu-id="735b6-159">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="735b6-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735b6-160">-DefaultProfile</span></span>
<span data-ttu-id="735b6-161">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="735b6-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="735b6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735b6-162">CommonParameters</span></span>
<span data-ttu-id="735b6-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="735b6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735b6-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735b6-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735b6-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="735b6-165">INPUTS</span></span>

### <span data-ttu-id="735b6-166">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="735b6-166">BatchAccountContext</span></span>
<span data-ttu-id="735b6-167">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="735b6-167">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="735b6-168">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="735b6-168">PSComputeNode</span></span>
<span data-ttu-id="735b6-169">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="735b6-169">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="735b6-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="735b6-170">OUTPUTS</span></span>

## <span data-ttu-id="735b6-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="735b6-171">NOTES</span></span>

## <span data-ttu-id="735b6-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="735b6-172">RELATED LINKS</span></span>

[<span data-ttu-id="735b6-173">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="735b6-173">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="735b6-174">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="735b6-174">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


