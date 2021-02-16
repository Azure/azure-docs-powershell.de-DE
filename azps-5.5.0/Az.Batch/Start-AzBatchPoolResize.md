---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/start-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Start-AzBatchPoolResize.md
ms.openlocfilehash: d8b03aee736456e549a6c88a0aacfeac1d78744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149273"
---
# <span data-ttu-id="cf107-101">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cf107-101">Start-AzBatchPoolResize</span></span>

## <span data-ttu-id="cf107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf107-102">SYNOPSIS</span></span>
<span data-ttu-id="cf107-103">Beginnt mit dem Ändern der Größe eines Pools.</span><span class="sxs-lookup"><span data-stu-id="cf107-103">Starts to resize a pool.</span></span>

## <span data-ttu-id="cf107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf107-104">SYNTAX</span></span>

```
Start-AzBatchPoolResize [-Id] <String> [-TargetDedicatedComputeNodes <Int32>]
 [-TargetLowPriorityComputeNodes <Int32>] [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf107-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf107-105">DESCRIPTION</span></span>
<span data-ttu-id="cf107-106">Das **Cmdlet "Start-AzBatchPoolResize"** startet einen Azure Batch-Größenänderungsvorgang für einen Pool.</span><span class="sxs-lookup"><span data-stu-id="cf107-106">The **Start-AzBatchPoolResize** cmdlet starts an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="cf107-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf107-107">EXAMPLES</span></span>

### <span data-ttu-id="cf107-108">Beispiel 1: Ändern der Größe eines Pools auf 12 Knoten</span><span class="sxs-lookup"><span data-stu-id="cf107-108">Example 1: Resize a pool to 12 nodes</span></span>
```
PS C:\>Start-AzBatchPoolResize -Id "ContosoPool06" -TargetDedicatedComputeNodes 12 -BatchContext $Context
```

<span data-ttu-id="cf107-109">Dieser Befehl startet einen Größenänderungsvorgang für den Pool mit der ID ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="cf107-109">This command starts a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="cf107-110">Das Ziel für den Vorgang sind 12 dedizierte Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="cf107-110">The target for the operation is 12 dedicated compute nodes.</span></span>
<span data-ttu-id="cf107-111">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="cf107-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cf107-112">Beispiel 2: Ändern der Größe eines Pools mithilfe einer Deallocation-Option</span><span class="sxs-lookup"><span data-stu-id="cf107-112">Example 2: Resize a pool using a deallocation option</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzBatchPoolResize -TargetDedicatedComputeNodes 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

<span data-ttu-id="cf107-113">Mit diesem Cmdlet wird die Größe eines Pools auf fünf dedizierte Rechenknoten geändert.</span><span class="sxs-lookup"><span data-stu-id="cf107-113">This cmdlet resizes a pool to five dedicated compute nodes.</span></span>
<span data-ttu-id="cf107-114">Der Befehl ruft den Pool mit der ID "ContosoPool06" mithilfe des cmdlets Get-AzBatchPool ab.</span><span class="sxs-lookup"><span data-stu-id="cf107-114">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="cf107-115">Der Befehl übergibt dieses Poolobjekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf107-115">The command passes that pool object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cf107-116">Der Befehl startet einen Größenänderungsvorgang für den Pool.</span><span class="sxs-lookup"><span data-stu-id="cf107-116">The command starts a resize operation on the pool.</span></span>
<span data-ttu-id="cf107-117">Das Ziel sind fünf dedizierte Rechenknoten.</span><span class="sxs-lookup"><span data-stu-id="cf107-117">The target is five dedicated compute nodes.</span></span>
<span data-ttu-id="cf107-118">Der Befehl gibt einen Zeitraum von einer Stunde an.</span><span class="sxs-lookup"><span data-stu-id="cf107-118">The command specifies time-out period of one hour.</span></span>
<span data-ttu-id="cf107-119">Der Befehl gibt die Deallocationoption "Terminate" an.</span><span class="sxs-lookup"><span data-stu-id="cf107-119">The command specifies a deallocation option of Terminate.</span></span>

## <span data-ttu-id="cf107-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf107-120">PARAMETERS</span></span>

### <span data-ttu-id="cf107-121">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf107-121">-BatchContext</span></span>
<span data-ttu-id="cf107-122">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf107-122">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf107-123">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf107-123">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf107-124">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf107-124">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf107-125">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf107-125">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf107-126">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cf107-126">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf107-127">-ComputeNodeDeallocationOption</span><span class="sxs-lookup"><span data-stu-id="cf107-127">-ComputeNodeDeallocationOption</span></span>
<span data-ttu-id="cf107-128">Gibt eine Deallocationoption für den Größenänderungsvorgang an, der mit diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cf107-128">Specifies a deallocation option for the resizing operation that this cmdlet starts.</span></span>

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

### <span data-ttu-id="cf107-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf107-129">-DefaultProfile</span></span>
<span data-ttu-id="cf107-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf107-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf107-131">-ID</span><span class="sxs-lookup"><span data-stu-id="cf107-131">-Id</span></span>
<span data-ttu-id="cf107-132">Gibt die ID des Pools an, dessen Größe dieses Cmdlets ändert.</span><span class="sxs-lookup"><span data-stu-id="cf107-132">Specifies the ID of the pool that this cmdlet resizes.</span></span>

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

### <span data-ttu-id="cf107-133">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="cf107-133">-ResizeTimeout</span></span>
<span data-ttu-id="cf107-134">Gibt einen Zeitzeitraum für den Größenänderungsvorgang an.</span><span class="sxs-lookup"><span data-stu-id="cf107-134">Specifies a time-out period for the resizing operation.</span></span>
<span data-ttu-id="cf107-135">Wenn der Pool die Zielgröße bis zu diesem Zeitpunkt nicht erreicht, wird der Größenänderungsvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="cf107-135">If the pool does not reach the target size by this time, the resize operation stops.</span></span>

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

### <span data-ttu-id="cf107-136">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="cf107-136">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="cf107-137">Die Anzahl der dedizierten Zielberechnungsknoten.</span><span class="sxs-lookup"><span data-stu-id="cf107-137">The number of target dedicated compute nodes.</span></span>

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

### <span data-ttu-id="cf107-138">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="cf107-138">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="cf107-139">Die Anzahl der Zielberechnungsknoten mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="cf107-139">The number of target low-priority compute nodes.</span></span>

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

### <span data-ttu-id="cf107-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf107-140">CommonParameters</span></span>
<span data-ttu-id="cf107-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf107-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf107-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf107-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf107-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf107-143">INPUTS</span></span>

### <span data-ttu-id="cf107-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cf107-144">System.String</span></span>

### <span data-ttu-id="cf107-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf107-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cf107-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf107-146">OUTPUTS</span></span>

### <span data-ttu-id="cf107-147">System.Void</span><span class="sxs-lookup"><span data-stu-id="cf107-147">System.Void</span></span>

## <span data-ttu-id="cf107-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf107-148">NOTES</span></span>

## <span data-ttu-id="cf107-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf107-149">RELATED LINKS</span></span>

[<span data-ttu-id="cf107-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cf107-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cf107-151">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cf107-151">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="cf107-152">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cf107-152">Stop-AzBatchPoolResize</span></span>](./Stop-AzBatchPoolResize.md)

[<span data-ttu-id="cf107-153">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cf107-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
