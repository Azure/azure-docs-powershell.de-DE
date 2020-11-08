---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165328"
---
# <span data-ttu-id="fbc75-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="fbc75-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="fbc75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbc75-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc75-103">Deaktiviert die Vorgangsplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="fbc75-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="fbc75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbc75-104">SYNTAX</span></span>

### <span data-ttu-id="fbc75-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbc75-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbc75-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fbc75-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbc75-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbc75-107">DESCRIPTION</span></span>
<span data-ttu-id="fbc75-108">Das Cmdlet **Disable-AzBatchComputeNodeScheduling** deaktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="fbc75-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="fbc75-109">Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="fbc75-110">Wenn Sie die Vorgangsplanung auf einem Compute-Knoten deaktivieren, können Sie auch bestimmen, was zu den Aufträgen aktuell in der Aufgabenwarteschlange des Knotens zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="fbc75-111">Mit **Disable-AzBatchComputeNodeScheduling** können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="fbc75-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="fbc75-112">Kündigen Sie die Aufgaben, und setzen Sie Sie wieder in die Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fbc75-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="fbc75-113">Dadurch können diese Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="fbc75-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="fbc75-114">Kündigen Sie die Aufgaben, und entfernen Sie Sie aus der Job-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fbc75-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="fbc75-115">Auf diese Weise gestoppte Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="fbc75-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="fbc75-116">Warten Sie, bis alle zurzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="fbc75-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="fbc75-117">Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Datenaufbewahrungszeiträume abgelaufen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="fbc75-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="fbc75-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbc75-118">EXAMPLES</span></span>

### <span data-ttu-id="fbc75-119">Beispiel 1: Deaktivieren der Vorgangsplanung auf einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="fbc75-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="fbc75-120">Diese Befehle deaktivieren den Aufgabenplan auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.</span><span class="sxs-lookup"><span data-stu-id="fbc75-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="fbc75-121">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="fbc75-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fbc75-122">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fbc75-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="fbc75-123">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **Disable-AzBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf dem Knoten TVM-1783593343_34-20151117t222514z zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fbc75-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="fbc75-124">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle zurzeit auf dem Compute-Knoten ausgeführten Aufgaben erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="fbc75-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="fbc75-125">Beispiel 2: Deaktivieren der Vorgangsplanung für alle Compute-Knoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="fbc75-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="fbc75-126">Diese Befehle deaktivieren die Aufgabenplanung auf allen Computerknoten im Batch Pool Pool06.</span><span class="sxs-lookup"><span data-stu-id="fbc75-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="fbc75-127">Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für die contosobatchaccount des Batch Kontos.</span><span class="sxs-lookup"><span data-stu-id="fbc75-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="fbc75-128">Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fbc75-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="fbc75-129">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fbc75-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="fbc75-130">Diese Sammlung wird dann an das Cmdlet **Disable-AzBatchComputeNodeScheduling** umgeleitet, um die Aufgabenplanung für jeden Compute-Knoten in der Sammlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fbc75-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="fbc75-131">Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle Aufgaben, die derzeit auf den Compute-Knoten ausgeführt werden, erneut in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="fbc75-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="fbc75-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbc75-132">PARAMETERS</span></span>

### <span data-ttu-id="fbc75-133">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="fbc75-133">-BatchContext</span></span>
<span data-ttu-id="fbc75-134">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbc75-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fbc75-135">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbc75-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fbc75-136">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fbc75-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fbc75-137">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbc75-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fbc75-138">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="fbc75-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fbc75-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="fbc75-139">-ComputeNode</span></span>
<span data-ttu-id="fbc75-140">Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="fbc75-141">Dieser Objektverweis wird mithilfe des Get-AzBatchComputeNode-Cmdlets erstellt und speichert das zurückgegebene Compute-Knotenobjekt in einer Variablen.</span><span class="sxs-lookup"><span data-stu-id="fbc75-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="fbc75-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc75-142">-DefaultProfile</span></span>
<span data-ttu-id="fbc75-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbc75-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbc75-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="fbc75-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="fbc75-145">Gibt an, wie sich dieses Cmdlet auf alle Aufgaben bezieht, die derzeit auf dem Computerknoten ausgeführt werden, auf dem die Planung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="fbc75-146">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fbc75-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fbc75-147">Erneute Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="fbc75-147">Requeue.</span></span>
<span data-ttu-id="fbc75-148">Aufgaben werden sofort angehalten und an die Job-Warteschlange zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fbc75-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="fbc75-149">Dadurch können die Aufgaben auf einem anderen Compute-Knoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="fbc75-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="fbc75-150">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="fbc75-150">This is the default value.</span></span> 
- <span data-ttu-id="fbc75-151">Beenden.</span><span class="sxs-lookup"><span data-stu-id="fbc75-151">Terminate.</span></span>
<span data-ttu-id="fbc75-152">Aufgaben werden sofort angehalten und aus der Job-Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="fbc75-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="fbc75-153">Diese Aufgaben werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="fbc75-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="fbc75-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="fbc75-154">TaskCompletion.</span></span>
<span data-ttu-id="fbc75-155">Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Vorgangsplanung auf dem Compute-Knoten deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="fbc75-156">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="fbc75-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="fbc75-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="fbc75-157">RetainedData.</span></span>
<span data-ttu-id="fbc75-158">Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung auf dem Compute-Knoten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="fbc75-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="fbc75-159">Auf diesem Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="fbc75-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="fbc75-160">-ID</span><span class="sxs-lookup"><span data-stu-id="fbc75-160">-Id</span></span>
<span data-ttu-id="fbc75-161">Gibt die ID des Compute-Knotens an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="fbc75-162">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="fbc75-162">-PoolId</span></span>
<span data-ttu-id="fbc75-163">Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fbc75-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="fbc75-164">Wenn Sie den *Pool* -Parameter verwenden, verwenden Sie den *ComputeNode* -Parameter nicht in demselben Befehl.</span><span class="sxs-lookup"><span data-stu-id="fbc75-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="fbc75-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc75-165">CommonParameters</span></span>
<span data-ttu-id="fbc75-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc75-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc75-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbc75-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc75-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbc75-168">INPUTS</span></span>

### <span data-ttu-id="fbc75-169">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="fbc75-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="fbc75-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fbc75-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="fbc75-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbc75-171">OUTPUTS</span></span>

### <span data-ttu-id="fbc75-172">System. void</span><span class="sxs-lookup"><span data-stu-id="fbc75-172">System.Void</span></span>

## <span data-ttu-id="fbc75-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbc75-173">NOTES</span></span>

## <span data-ttu-id="fbc75-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbc75-174">RELATED LINKS</span></span>

[<span data-ttu-id="fbc75-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="fbc75-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="fbc75-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="fbc75-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


