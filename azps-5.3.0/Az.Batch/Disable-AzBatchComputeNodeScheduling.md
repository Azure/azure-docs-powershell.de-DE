---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471216"
---
# <span data-ttu-id="e6bb3-101">Disable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="e6bb3-101">Disable-AzBatchComputeNodeScheduling</span></span>

## <span data-ttu-id="e6bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bb3-103">Deaktiviert die Vorgangsplanung für den angegebenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-103">Disables task scheduling on the specified compute node.</span></span>

## <span data-ttu-id="e6bb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6bb3-104">SYNTAX</span></span>

### <span data-ttu-id="e6bb3-105">ID (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6bb3-105">Id (Default)</span></span>
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6bb3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e6bb3-106">InputObject</span></span>
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6bb3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6bb3-107">DESCRIPTION</span></span>
<span data-ttu-id="e6bb3-108">Das **Cmdlet "Disable-AzBatchComputeNodeScheduling"** deaktiviert die Aufgabenplanung für den angegebenen Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-108">The **Disable-AzBatchComputeNodeScheduling** cmdlet disables task scheduling on the specified compute node.</span></span>
<span data-ttu-id="e6bb3-109">Ein Rechenknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-109">A compute node is an Azure virtual machine dedicated to a specific application workload.</span></span>
<span data-ttu-id="e6bb3-110">Wenn Sie die Aufgabenplanung für einen Rechenknoten deaktivieren, haben Sie auch die Möglichkeit zu bestimmen, was mit Aufträgen zu tun ist, die sich aktuell in der Aufgabenwarteschlange des Knotens befinden.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-110">When you disable task scheduling on a compute node you will also have the option of determining what to do about jobs currently in the node's task queue.</span></span>
<span data-ttu-id="e6bb3-111">**Disable-AzBatchComputeNodeScheduling** ermöglicht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e6bb3-111">**Disable-AzBatchComputeNodeScheduling** lets you do the following:</span></span> 
- <span data-ttu-id="e6bb3-112">Beenden Sie die Aufgaben, und setzen Sie sie wieder in die Auftragswarteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-112">Terminate the tasks and put them back in the job queue.</span></span>
<span data-ttu-id="e6bb3-113">Dadurch können diese Aufgaben auf einem anderen Rechenknoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-113">This enables those tasks to be rescheduled on another compute node.</span></span> 
- <span data-ttu-id="e6bb3-114">Beenden Sie die Aufgaben, und entfernen Sie sie aus der Auftragswarteschlange.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-114">Terminate the tasks and remove them from the job queue.</span></span>
<span data-ttu-id="e6bb3-115">Auf diese Weise beendete Vorgänge werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-115">Tasks stopped in this manner will not be rescheduled.</span></span> 
- <span data-ttu-id="e6bb3-116">Warten Sie, bis alle derzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung für den Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-116">Wait for all the tasks currently being executed to complete and then disable task scheduling on the compute node.</span></span> 
- <span data-ttu-id="e6bb3-117">Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Aufbewahrungszeiträume für Daten ablaufen, und deaktivieren Sie dann die Aufgabenplanung für den Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-117">Wait for all the running tasks to complete and all the data retention periods to expire, and then disable task scheduling on the compute node.</span></span>

## <span data-ttu-id="e6bb3-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6bb3-118">EXAMPLES</span></span>

### <span data-ttu-id="e6bb3-119">Beispiel 1: Deaktivieren der Vorgangsplanung für einen Rechenknoten</span><span class="sxs-lookup"><span data-stu-id="e6bb3-119">Example 1: Disable task scheduling on a compute node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

<span data-ttu-id="e6bb3-120">Mit diesen Befehlen wird der Aufgabenzeitplan auf dem berechneten Knoten "tvm-1783593343_34-20151117t222514z" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-120">These commands disable task schedule on the compute node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="e6bb3-121">Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto "contosobatchaccount".</span><span class="sxs-lookup"><span data-stu-id="e6bb3-121">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="e6bb3-122">Dieser Objektverweis wird in einer Variablen namens "$context.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-122">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="e6bb3-123">Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Disable-AzBatchComputeNodeScheduling",** um eine Verbindung mit dem Pool "myPool" herzustellen und die Aufgabenplanung auf node tvm-1783593343_34-20151117t222514z zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-123">The second command then uses this object reference and the **Disable-AzBatchComputeNodeScheduling** cmdlet to connect to the pool myPool and disable task scheduling on node tvm-1783593343_34-20151117t222514z.</span></span>
<span data-ttu-id="e6bb3-124">Da der *Parameter "DisableComputeNodeSchedulingOptions"* nicht enthalten war, werden alle derzeit auf dem Rechenknoten ausgeführten Aufgaben neu ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-124">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute node will be requeued.</span></span>

### <span data-ttu-id="e6bb3-125">Beispiel 2: Deaktivieren der Vorgangsplanung für alle Rechenknoten in einem Pool</span><span class="sxs-lookup"><span data-stu-id="e6bb3-125">Example 2: Disable task scheduling on all compute nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

<span data-ttu-id="e6bb3-126">Mit diesen Befehlen wird die Aufgabenplanung für alle Computerknoten im Batchpoolpool06 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-126">These commands disable task scheduling on all the computer nodes in the batch pool Pool06.</span></span>
<span data-ttu-id="e6bb3-127">Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto "contosobatchaccount".</span><span class="sxs-lookup"><span data-stu-id="e6bb3-127">To perform this task, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="e6bb3-128">Dieser Objektverweis wird in einer Variablen namens "$context.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-128">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="e6bb3-129">Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **"Get-AzBatchComputeNode",** um eine Sammlung aller In Pool06 gefundenen Berechnungsknoten zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-129">The second command in the example then uses this object reference and **Get-AzBatchComputeNode** to return a collection of all the compute nodes found in Pool06.</span></span>
<span data-ttu-id="e6bb3-130">Diese Sammlung wird dann an das Cmdlet **"Disable-AzBatchComputeNodeScheduling"** weiterverteilt, um die Aufgabenplanung für jeden Rechenknoten in der Sammlung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-130">That collection is then piped to then **Disable-AzBatchComputeNodeScheduling** cmdlet to disable task scheduling on each compute node in the collection.</span></span>
<span data-ttu-id="e6bb3-131">Da der *Parameter "DisableComputeNodeSchedulingOptions"* nicht enthalten war, werden die derzeit für die Berechnungsknoten ausgeführten Aufgaben neu ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-131">Because the *DisableComputeNodeSchedulingOptions* parameter was not included any tasks currently running on the compute nodes will be requeued.</span></span>

## <span data-ttu-id="e6bb3-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6bb3-132">PARAMETERS</span></span>

### <span data-ttu-id="e6bb3-133">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e6bb3-133">-BatchContext</span></span>
<span data-ttu-id="e6bb3-134">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-134">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e6bb3-135">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-135">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e6bb3-136">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-136">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e6bb3-137">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-137">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e6bb3-138">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-138">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e6bb3-139">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="e6bb3-139">-ComputeNode</span></span>
<span data-ttu-id="e6bb3-140">Gibt einen Objektverweis auf den Rechenknoten an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-140">Specifies an object reference to the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="e6bb3-141">Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchComputeNode erstellt und das zurückgegebene Rechenknotenobjekt in einer Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-141">This object reference is created by using the Get-AzBatchComputeNode cmdlet and storing the returned compute node object in a variable.</span></span>

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

### <span data-ttu-id="e6bb3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bb3-142">-DefaultProfile</span></span>
<span data-ttu-id="e6bb3-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6bb3-144">-DisableSchedulingOption</span><span class="sxs-lookup"><span data-stu-id="e6bb3-144">-DisableSchedulingOption</span></span>
<span data-ttu-id="e6bb3-145">Gibt an, wie dieses Cmdlet mit aufgaben behandelt wird, die derzeit auf dem Computerknoten ausgeführt werden, in dem die Planung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-145">Specifies how this cmdlet deals with any tasks currently running on the computer node where scheduling is being disabled.</span></span>
<span data-ttu-id="e6bb3-146">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="e6bb3-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6bb3-147">Requeue.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-147">Requeue.</span></span>
<span data-ttu-id="e6bb3-148">Aufgaben werden sofort beendet und an die Auftragswarteschlange zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-148">Tasks are stopped immediately and returned to the job queue.</span></span>
<span data-ttu-id="e6bb3-149">Dadurch können die Aufgaben auf einem anderen Rechenknoten neu geplant werden.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-149">This enables the tasks to be rescheduled on another compute node.</span></span>
<span data-ttu-id="e6bb3-150">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-150">This is the default value.</span></span> 
- <span data-ttu-id="e6bb3-151">"Beenden" aus.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-151">Terminate.</span></span>
<span data-ttu-id="e6bb3-152">Aufgaben werden sofort beendet und aus der Auftragswarteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-152">Tasks are stopped immediately and removed from the job queue.</span></span>
<span data-ttu-id="e6bb3-153">Diese Vorgänge werden nicht neu geplant.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-153">These tasks will not be rescheduled.</span></span> 
- <span data-ttu-id="e6bb3-154">TaskCompletion.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-154">TaskCompletion.</span></span>
<span data-ttu-id="e6bb3-155">Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Aufgabenplanung auf dem Rechenknoten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-155">Currently running tasks will be able to complete before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="e6bb3-156">Für diesen Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-156">No new tasks will be scheduled on this node.</span></span> 
- <span data-ttu-id="e6bb3-157">RetainedData.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-157">RetainedData.</span></span>
<span data-ttu-id="e6bb3-158">Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung für den Rechenknoten deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-158">Currently running tasks will be able to complete and data retention periods will be able to expire before task scheduling is disabled on the compute node.</span></span>
<span data-ttu-id="e6bb3-159">Für diesen Knoten werden keine neuen Aufgaben geplant.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-159">No new tasks will be scheduled on this node.</span></span>

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

### <span data-ttu-id="e6bb3-160">-ID</span><span class="sxs-lookup"><span data-stu-id="e6bb3-160">-Id</span></span>
<span data-ttu-id="e6bb3-161">Gibt die ID des Rechenknotens an, in dem die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-161">Specifies the ID of the compute node where task scheduling is disabled.</span></span>

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

### <span data-ttu-id="e6bb3-162">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e6bb3-162">-PoolId</span></span>
<span data-ttu-id="e6bb3-163">Gibt die ID des Batchpools an, der den Rechenknoten enthält, für den die Aufgabenplanung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-163">Specifies the ID of the batch pool that contains the compute node where task scheduling is disabled.</span></span>
<span data-ttu-id="e6bb3-164">Wenn Sie den Parameter *"PoolId"* verwenden, verwenden Sie den Parameter *"ComputeNode"* nicht in demselben Befehl.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-164">If you use the *PoolId* parameter, do not use the *ComputeNode* parameter in that same command.</span></span>

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

### <span data-ttu-id="e6bb3-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bb3-165">CommonParameters</span></span>
<span data-ttu-id="e6bb3-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bb3-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bb3-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6bb3-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bb3-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6bb3-168">INPUTS</span></span>

### <span data-ttu-id="e6bb3-169">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e6bb3-169">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="e6bb3-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e6bb3-170">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e6bb3-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6bb3-171">OUTPUTS</span></span>

### <span data-ttu-id="e6bb3-172">System.Void</span><span class="sxs-lookup"><span data-stu-id="e6bb3-172">System.Void</span></span>

## <span data-ttu-id="e6bb3-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6bb3-173">NOTES</span></span>

## <span data-ttu-id="e6bb3-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6bb3-174">RELATED LINKS</span></span>

[<span data-ttu-id="e6bb3-175">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6bb3-175">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e6bb3-176">Enable-AzBatchComputeNodeScheduling</span><span class="sxs-lookup"><span data-stu-id="e6bb3-176">Enable-AzBatchComputeNodeScheduling</span></span>](./Enable-AzBatchComputeNodeScheduling.md)


