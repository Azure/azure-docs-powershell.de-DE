---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: 2adaebc28f27d2ea785df5a93510375020bcd542
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938296"
---
# <span data-ttu-id="f4ded-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f4ded-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="f4ded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ded-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ded-103">Ruft Batchverarbeitungsknoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="f4ded-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="f4ded-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4ded-104">SYNTAX</span></span>

### <span data-ttu-id="f4ded-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4ded-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ded-106">ID</span><span class="sxs-lookup"><span data-stu-id="f4ded-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4ded-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4ded-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ded-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4ded-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ded-109">Das **Get-AzBatchComputeNode-Cmdlet** ruft Azure Batch-Computeknoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="f4ded-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="f4ded-110">Geben Sie entweder *den Parameter PoolID* *oder Pool* an.</span><span class="sxs-lookup"><span data-stu-id="f4ded-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="f4ded-111">Geben Sie den *Parameter ID* an, um einen einzelnen Computeknoten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4ded-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="f4ded-112">Geben Sie den *Parameter Filter* an, um die Computeknoten zu erhalten, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4ded-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="f4ded-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4ded-113">EXAMPLES</span></span>

### <span data-ttu-id="f4ded-114">Beispiel 1: Berechnen eines Computeknotens nach ID</span><span class="sxs-lookup"><span data-stu-id="f4ded-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="f4ded-115">Dieser Befehl ruft den Computeknoten ab, der die ID tvm-2316545714_1-20150725t213220z aus dem Pool mit dem ID-Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="f4ded-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="f4ded-116">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f4ded-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f4ded-117">Beispiel 2: Alle im Leerlauf ausgeführten Computeknoten aus einem Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="f4ded-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="f4ded-118">Dieser Befehl ruft alle im Leerlauf ausgeführten Computeknoten ab, die im Pool mit dem ID-Pool06 enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f4ded-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="f4ded-119">Der Befehl gibt den Leerlaufzustand mithilfe des Parameters *Filter* an.</span><span class="sxs-lookup"><span data-stu-id="f4ded-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="f4ded-120">Beispiel 3: Alle Computeknoten in einem angegebenen Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="f4ded-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzBatchPool -Id "Pool07" -BatchContext $Context | Get-AzBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 1
StartTaskInformation  :
RecentTasks           : {}
StartTask             :
CertificateReferences :
Errors                :


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : standard_d1_v2
TotalTasksRun         : 0
StartTaskInformation  :
RecentTasks           :
StartTask             :
CertificateReferences :
Errors                :
```

<span data-ttu-id="f4ded-121">Mit diesem Befehl wird der Pool mit dem ID-Pool07 mithilfe des Get-AzBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="f4ded-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="f4ded-122">Der Befehl übergibt diesen Pool mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ded-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f4ded-123">Dieses Cmdlet ruft alle Computeknoten aus diesem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="f4ded-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="f4ded-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4ded-124">PARAMETERS</span></span>

### <span data-ttu-id="f4ded-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4ded-125">-BatchContext</span></span>
<span data-ttu-id="f4ded-126">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f4ded-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4ded-127">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4ded-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4ded-128">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4ded-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4ded-129">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4ded-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4ded-130">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="f4ded-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4ded-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ded-131">-DefaultProfile</span></span>
<span data-ttu-id="f4ded-132">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4ded-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ded-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="f4ded-133">-Filter</span></span>
<span data-ttu-id="f4ded-134">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="f4ded-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="f4ded-135">Dieses Cmdlet gibt Berechnungsknoten zurück, die dem von diesem Parameter angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f4ded-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="f4ded-136">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Computeknoten für den Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="f4ded-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-137">-ID</span><span class="sxs-lookup"><span data-stu-id="f4ded-137">-Id</span></span>
<span data-ttu-id="f4ded-138">Gibt die ID des Computeknotens an, den dieses Cmdlet aus dem Pool erhält.</span><span class="sxs-lookup"><span data-stu-id="f4ded-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="f4ded-139">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="f4ded-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f4ded-140">-MaxCount</span></span>
<span data-ttu-id="f4ded-141">Gibt die maximale Anzahl von zu zurückgebenden Computeknoten an.</span><span class="sxs-lookup"><span data-stu-id="f4ded-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="f4ded-142">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4ded-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="f4ded-143">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="f4ded-143">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="f4ded-144">-Pool</span></span>
<span data-ttu-id="f4ded-145">Gibt den Pool als **PSCloudPool-Objekt** an, das die Computeknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="f4ded-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="f4ded-146">Um ein **PSCloudPool-Objekt zu** erhalten, verwenden Sie das Get-AzBatchPool Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ded-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f4ded-147">-PoolId</span></span>
<span data-ttu-id="f4ded-148">Gibt die ID des Pools an, der die Computeknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="f4ded-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-149">-Select</span><span class="sxs-lookup"><span data-stu-id="f4ded-149">-Select</span></span>
<span data-ttu-id="f4ded-150">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="f4ded-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="f4ded-151">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften anstelle aller Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f4ded-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ded-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ded-152">CommonParameters</span></span>
<span data-ttu-id="f4ded-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ded-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ded-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4ded-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ded-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4ded-155">INPUTS</span></span>

### <span data-ttu-id="f4ded-156">System.String</span><span class="sxs-lookup"><span data-stu-id="f4ded-156">System.String</span></span>

### <span data-ttu-id="f4ded-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="f4ded-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="f4ded-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4ded-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f4ded-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4ded-159">OUTPUTS</span></span>

### <span data-ttu-id="f4ded-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="f4ded-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="f4ded-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4ded-161">NOTES</span></span>

## <span data-ttu-id="f4ded-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4ded-162">RELATED LINKS</span></span>

[<span data-ttu-id="f4ded-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f4ded-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="f4ded-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="f4ded-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="f4ded-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="f4ded-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="f4ded-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f4ded-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="f4ded-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f4ded-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="f4ded-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="f4ded-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="f4ded-169">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="f4ded-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
