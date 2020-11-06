---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/start-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: c635061ac19b0fcc9543222da176324f84bea3a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498401"
---
# <span data-ttu-id="3e02d-101">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="3e02d-101">Start-AzureBatchPoolResize</span></span>

## <span data-ttu-id="3e02d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e02d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e02d-103">Beginnt, die Größe eines Pools zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3e02d-103">Starts to resize a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e02d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e02d-104">SYNTAX</span></span>

```
Start-AzureBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e02d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e02d-105">DESCRIPTION</span></span>
<span data-ttu-id="3e02d-106">Das Cmdlet **Start-AzureBatchPoolResize** startet eine Azure Batch-Größenänderung in einem Pool.</span><span class="sxs-lookup"><span data-stu-id="3e02d-106">The **Start-AzureBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="3e02d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e02d-107">EXAMPLES</span></span>

### <span data-ttu-id="3e02d-108">Beispiel 1: Ändern der Größe eines Pools auf 12 Knoten</span><span class="sxs-lookup"><span data-stu-id="3e02d-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="3e02d-109">Mit diesem Befehl wird ein Größen Änderungsvorgang für den Pool mit der ID ContosoPool06 gestartet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="3e02d-110">Das Ziel des Vorgangs ist 12 dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="3e02d-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="3e02d-111">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="3e02d-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3e02d-112">Beispiel 2: Ändern der Größe eines Pools mithilfe einer Option für die Freigabe</span><span class="sxs-lookup"><span data-stu-id="3e02d-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="3e02d-113">Dieses Cmdlet ändert die Größe eines Pools auf fünf dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="3e02d-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="3e02d-114">Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzureBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e02d-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="3e02d-115">Der Befehl übergibt das Pool-Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3e02d-116">Mit dem Befehl wird ein Größen Änderungsvorgang für den Pool gestartet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="3e02d-117">Das Ziel sind fünf dedizierte Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="3e02d-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="3e02d-118">Der Befehl gibt einen Timeoutzeitraum von einer Stunde an.</span><span class="sxs-lookup"><span data-stu-id="3e02d-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="3e02d-119">Der Befehl gibt eine Option zum Aufheben der Zuweisung von Terminate an.</span><span class="sxs-lookup"><span data-stu-id="3e02d-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="3e02d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e02d-120">PARAMETERS</span></span>

### <span data-ttu-id="3e02d-121">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="3e02d-121">-BatchContext</span></span>
<span data-ttu-id="3e02d-122">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3e02d-123">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-123">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3e02d-124">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e02d-124">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3e02d-125">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e02d-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3e02d-126">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e02d-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3e02d-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="3e02d-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="3e02d-128">Gibt eine Option für die Freigabe für die Größenänderung an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3e02d-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3e02d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e02d-129">-DefaultProfile</span></span>
<span data-ttu-id="3e02d-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e02d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e02d-131">-ID</span><span class="sxs-lookup"><span data-stu-id="3e02d-131">-Id</span></span>
<span data-ttu-id="3e02d-132">Gibt die ID des Pools an, in dem dieses Cmdlet die Größe ändert.</span><span class="sxs-lookup"><span data-stu-id="3e02d-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="3e02d-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="3e02d-133">-ResizeTimeout</span></span>
<span data-ttu-id="3e02d-134">Gibt einen Timeoutzeitraum für den Größen Änderungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="3e02d-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="3e02d-135">Wenn der Pool bis zu diesem Zeitpunkt nicht die Zielgröße erreicht, wird der Vorgang zum Ändern der Größe angehalten.</span><span class="sxs-lookup"><span data-stu-id="3e02d-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="3e02d-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="3e02d-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="3e02d-137">Die Anzahl der Ziel dedizierten Compute-Knoten.</span><span class="sxs-lookup"><span data-stu-id="3e02d-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="3e02d-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="3e02d-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="3e02d-139">Die Anzahl der Ziel-Compute-Knoten mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="3e02d-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="3e02d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e02d-140">CommonParameters</span></span>
<span data-ttu-id="3e02d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e02d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e02d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e02d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e02d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e02d-143">INPUTS</span></span>

### <span data-ttu-id="3e02d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3e02d-144">System.String</span></span>

### <span data-ttu-id="3e02d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e02d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="3e02d-146">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3e02d-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="3e02d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e02d-147">OUTPUTS</span></span>

### <span data-ttu-id="3e02d-148">System. void</span><span class="sxs-lookup"><span data-stu-id="3e02d-148">System.Void</span></span>

## <span data-ttu-id="3e02d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e02d-149">NOTES</span></span>

## <span data-ttu-id="3e02d-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e02d-150">RELATED LINKS</span></span>

[<span data-ttu-id="3e02d-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3e02d-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="3e02d-152">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="3e02d-152">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="3e02d-153">Stopp-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="3e02d-153">Stop-AzureBatchPoolResize</span></span>](./Stop-AzureBatchPoolResize.md)

[<span data-ttu-id="3e02d-154">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3e02d-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


