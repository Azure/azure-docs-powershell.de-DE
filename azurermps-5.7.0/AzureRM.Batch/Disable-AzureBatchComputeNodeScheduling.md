---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchComputeNodeScheduling.md
ms.openlocfilehash: 40eb6d3cfd3961c876a5da07ced1ebcf383166e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505798"
---
# <span data-ttu-id="79c1d-101">Disable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="79c1d-101">Disable-AzureBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="79c1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="79c1d-103">Deaktiviert die Vorgangsplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="79c1d-103">Disables task scheduling on the specified compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c1d-104">SYNTAX</span></span>

### <span data-ttu-id="79c1d-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="79c1d-105">Id (Default)</span></span>
```
Disable-AzureBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79c1d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="79c1d-106">InputObject</span></span>
```
Disable-AzureBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c1d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="79c1d-108">Das Cmdlet **Disable-AzureBatchComputeNodeScheduling** deaktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="79c1d-108">The **Disable-AzureBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="79c1d-109">Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="79c1d-110">Wenn Sie die Vorgangsplanung auf einem Compute-Knoten deaktivieren, können Sie auch bestimmen, was zu den Aufträgen aktuell in der Aufgabenwarteschlange des Knotens zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="79c1d-111">Mit **Disable-AzureBatchComputeNodeScheduling** können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="79c1d-111">**Disable-AzureBatchComputeNodeScheduling** lets you do the following:</span></span> 

- <span data-ttu-id="79c1d-112">Kündigen Sie die Aufgaben, und setzen Sie Sie wieder in die Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="79c1d-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="79c1d-113">Dadurch können diese Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="79c1d-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="79c1d-114">Kündigen Sie die Aufgaben, und entfernen Sie Sie aus der Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="79c1d-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="79c1d-115">Auf diese Weise gestoppte Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="79c1d-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="79c1d-116">Warten Sie, bis alle zurzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="79c1d-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="79c1d-117">Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Datenaufbewahrungszeiträume abgelaufen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="79c1d-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="79c1d-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c1d-118">EXAMPLES</span></span>

### <span data-ttu-id="79c1d-119">Beispiel 1: Deaktivieren der Vorgangsplanung auf einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="79c1d-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Disable-AzureBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="79c1d-120">Diese Befehle deaktivieren den Aufgabenplan auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="79c1d-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="79c1d-121">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="79c1d-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="79c1d-122">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79c1d-122">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="79c1d-123">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **Disable-AzureBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf dem Knoten TVM-1783593343_34-20151117t222514z zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79c1d-123">The second command then uses this object reference and the **Disable-AzureBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>

<span data-ttu-id="79c1d-124">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle zurzeit auf dem Compute-Knoten ausgeführten Aufgaben erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="79c1d-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="79c1d-125">Beispiel 2: Deaktivieren der Vorgangsplanung für alle Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="79c1d-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzureBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="79c1d-126">Diese Befehle deaktivieren die Aufgabenplanung auf allen Computerknoten im Batch Pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="79c1d-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="79c1d-127">Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für die contosobatchaccount des Batch Kontos.</span><span class="sxs-lookup"><span data-stu-id="79c1d-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="79c1d-128">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79c1d-128">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="79c1d-129">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzureBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="79c1d-129">The second command in the example then uses this object reference and **Get-AzureBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="79c1d-130">Diese Sammlung wird dann an das Cmdlet **Disable-AzureBatchComputeNodeScheduling** umgeleitet, um die Aufgabenplanung für jeden Compute-Knoten in der Sammlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79c1d-130">That collection is then piped to then **Disable-AzureBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>

<span data-ttu-id="79c1d-131">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle Aufgaben, die derzeit auf den Compute-Knoten ausgeführt werden, erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="79c1d-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="79c1d-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c1d-132">PARAMETERS</span></span>

### <span data-ttu-id="79c1d-133">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="79c1d-133">-BatchContext</span></span>
<span data-ttu-id="79c1d-134">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="79c1d-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79c1d-135">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="79c1d-135">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79c1d-136">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="79c1d-136">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79c1d-137">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="79c1d-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79c1d-138">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="79c1d-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79c1d-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="79c1d-139">-ComputeNode</span></span>
<span data-ttu-id="79c1d-140">Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="79c1d-141">Dieser Objektverweis wird mithilfe des Get-AzureBatchComputeNode-Cmdlets erstellt und speichert das zurückgegebene Compute-Knotenobjekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="79c1d-141">This object reference is created by using the Get-AzureBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="79c1d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c1d-142">-DefaultProfile</span></span>
<span data-ttu-id="79c1d-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79c1d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c1d-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="79c1d-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="79c1d-145">Gibt an, wie sich dieses Cmdlet auf alle Aufgaben bezieht, die derzeit auf dem Computerknoten ausgeführt werden, auf dem die Planung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="79c1d-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79c1d-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79c1d-147">Erneute Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="79c1d-147">Requeue.</span></span>
<span data-ttu-id="79c1d-148">Aufgaben werden sofort angehalten und an die Job-Warteschlange zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="79c1d-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="79c1d-149">Dadurch können die Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="79c1d-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="79c1d-150">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="79c1d-150">This is the default value.</span></span> 
- <span data-ttu-id="79c1d-151">Beenden.</span><span class="sxs-lookup"><span data-stu-id="79c1d-151">Terminate.</span></span>
<span data-ttu-id="79c1d-152">Aufgaben werden sofort angehalten und aus der Job-Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="79c1d-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="79c1d-153">Diese Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="79c1d-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="79c1d-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="79c1d-154">TaskCompletion.</span></span>
<span data-ttu-id="79c1d-155">Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Vorgangsplanung auf dem Compute-Knoten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="79c1d-156">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="79c1d-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="79c1d-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="79c1d-157">RetainedData.</span></span>
<span data-ttu-id="79c1d-158">Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung auf dem Compute-Knoten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="79c1d-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="79c1d-159">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="79c1d-159">No new tasks will be scheduled on this node.</span></span>

```yaml
Type: DisableComputeNodeSchedulingOption
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c1d-160">-ID</span><span class="sxs-lookup"><span data-stu-id="79c1d-160">-Id</span></span>
<span data-ttu-id="79c1d-161">Gibt die ID des Compute-Knotens an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="79c1d-162">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="79c1d-162">-PoolId</span></span>
<span data-ttu-id="79c1d-163">Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="79c1d-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>

<span data-ttu-id="79c1d-164">Wenn Sie den *Pool* -Parameter verwenden, verwenden Sie den *ComputeNode* -Parameter nicht in demselben Befehl.</span><span class="sxs-lookup"><span data-stu-id="79c1d-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="79c1d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c1d-165">CommonParameters</span></span>
<span data-ttu-id="79c1d-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c1d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c1d-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c1d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c1d-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c1d-168">INPUTS</span></span>

### <span data-ttu-id="79c1d-169">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79c1d-169">BatchAccountContext</span></span>
<span data-ttu-id="79c1d-170">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="79c1d-170">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="79c1d-171">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="79c1d-171">PSComputeNode</span></span>
<span data-ttu-id="79c1d-172">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="79c1d-172">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="79c1d-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c1d-173">OUTPUTS</span></span>

## <span data-ttu-id="79c1d-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c1d-174">NOTES</span></span>

## <span data-ttu-id="79c1d-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c1d-175">RELATED LINKS</span></span>

[<span data-ttu-id="79c1d-176">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="79c1d-176">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="79c1d-177">Enable-AzureBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="79c1d-177">Enable-AzureBatchComputeNodeScheduling</span></span>](./Enable-AzureBatchComputeNodeScheduling.md)


