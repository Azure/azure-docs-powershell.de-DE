---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179429"
---
# <span data-ttu-id="7f1ab-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7f1ab-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="7f1ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1ab-103">Beginnt, die Größe eines Pools zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="7f1ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f1ab-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f1ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="7f1ab-106">Das Cmdlet **Start-AzBatchPoolResize** startet eine Azure Batch-Größenänderung in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="7f1ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f1ab-107">EXAMPLES</span></span>

### <span data-ttu-id="7f1ab-108">Beispiel 1: Ändern der Größe eines Pools auf 12 Knoten</span><span class="sxs-lookup"><span data-stu-id="7f1ab-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="7f1ab-109">Mit diesem Befehl wird ein Größen Änderungsvorgang für den Pool mit der ID ContosoPool06 gestartet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="7f1ab-110">Das Ziel des Vorgangs ist 12 dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="7f1ab-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7f1ab-112">Beispiel 2: Ändern der Größe eines Pools mithilfe einer Option für die Freigabe</span><span class="sxs-lookup"><span data-stu-id="7f1ab-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="7f1ab-113">Dieses Cmdlet ändert die Größe eines Pools auf fünf dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="7f1ab-114">Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="7f1ab-115">Der Befehl übergibt das Pool-Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7f1ab-116">Mit dem Befehl wird ein Größen Änderungsvorgang für den Pool gestartet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="7f1ab-117">Das Ziel sind fünf dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="7f1ab-118">Der Befehl gibt einen Timeoutzeitraum von einer Stunde an.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="7f1ab-119">Der Befehl gibt eine Option zum Aufheben der Zuweisung von Terminate an.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="7f1ab-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f1ab-120">PARAMETERS</span></span>

### <span data-ttu-id="7f1ab-121">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="7f1ab-121">-BatchContext</span></span>
<span data-ttu-id="7f1ab-122">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7f1ab-123">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7f1ab-124">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7f1ab-125">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7f1ab-126">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7f1ab-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="7f1ab-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="7f1ab-128">Gibt eine Option für die Freigabe für die Größenänderung an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1ab-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1ab-129">-DefaultProfile</span></span>
<span data-ttu-id="7f1ab-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f1ab-131">-ID</span><span class="sxs-lookup"><span data-stu-id="7f1ab-131">-Id</span></span>
<span data-ttu-id="7f1ab-132">Gibt die ID des Pools an, in dem dieses Cmdlet die Größe ändert.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f1ab-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="7f1ab-133">-ResizeTimeout</span></span>
<span data-ttu-id="7f1ab-134">Gibt einen Timeoutzeitraum für den Größen Änderungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="7f1ab-135">Wenn der Pool bis zu diesem Zeitpunkt nicht die Zielgröße erreicht, wird der Vorgang zum Ändern der Größe angehalten.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1ab-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7f1ab-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="7f1ab-137">Die Anzahl der Ziel dedizierten Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-137">The number of target dedicated compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1ab-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7f1ab-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="7f1ab-139">Die Anzahl der Ziel-Compute-Knoten mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-139">The number of target low-priority compute nodes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f1ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1ab-140">CommonParameters</span></span>
<span data-ttu-id="7f1ab-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1ab-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f1ab-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1ab-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f1ab-143">INPUTS</span></span>

### <span data-ttu-id="7f1ab-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7f1ab-144">System.String</span></span>

### <span data-ttu-id="7f1ab-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7f1ab-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7f1ab-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f1ab-146">OUTPUTS</span></span>

### <span data-ttu-id="7f1ab-147">System. void</span><span class="sxs-lookup"><span data-stu-id="7f1ab-147">System.Void</span></span>

## <span data-ttu-id="7f1ab-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f1ab-148">NOTES</span></span>

## <span data-ttu-id="7f1ab-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f1ab-149">RELATED LINKS</span></span>

[<span data-ttu-id="7f1ab-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7f1ab-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7f1ab-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="7f1ab-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="7f1ab-152">Stopp-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="7f1ab-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="7f1ab-153">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7f1ab-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
