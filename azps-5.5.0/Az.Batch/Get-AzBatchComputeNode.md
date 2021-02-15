---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: a50329620944aa18458c3bb667e3a95ff45bc21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164353"
---
# <span data-ttu-id="e0cb6-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e0cb6-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="e0cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cb6-103">Ruft Stapelberechnungsknoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="e0cb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0cb6-104">SYNTAX</span></span>

### <span data-ttu-id="e0cb6-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0cb6-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cb6-106">ID</span><span class="sxs-lookup"><span data-stu-id="e0cb6-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cb6-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="e0cb6-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0cb6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0cb6-108">DESCRIPTION</span></span>
<span data-ttu-id="e0cb6-109">Das **Get-AzBatchComputeNode-Cmdlet** ruft Azure Batch-Berechnungsknoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="e0cb6-110">Geben Sie entweder *den Parameter "PoolID"* oder *"Pool"* an.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="e0cb6-111">Geben Sie den *Parameter "Id"* an, um einen einzelnen Rechenknoten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="e0cb6-112">Geben Sie den *Filterparameter* an, um die Rechenknoten zu erhalten, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e0cb6-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0cb6-113">EXAMPLES</span></span>

### <span data-ttu-id="e0cb6-114">Beispiel 1: Erhalten eines Rechenknotens nach ID</span><span class="sxs-lookup"><span data-stu-id="e0cb6-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="e0cb6-115">Dieser Befehl ruft den Rechenknoten mit der ID tvm-2316545714_1-20150725t213220z aus dem Pool mit dem ID Pool06 ab.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="e0cb6-116">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="e0cb6-117">Beispiel 2: Alle Im Leerlaufberechnungsknoten aus einem Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="e0cb6-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="e0cb6-118">Mit diesem Befehl werden alle im Leerlauf ausgeführten Berechnungsknoten in dem Pool mit dem ID Pool06 ruft.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="e0cb6-119">Der Befehl gibt den Leerlaufzustand mit dem Parameter *"Filter"* an.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="e0cb6-120">Beispiel 3: Alle Rechenknoten in einem angegebenen Pool erhalten</span><span class="sxs-lookup"><span data-stu-id="e0cb6-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="e0cb6-121">Dieser Befehl ruft den Pool mit dem ID Pool07 mithilfe des Get-AzBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="e0cb6-122">Der Befehl übergibt diesen Pool mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e0cb6-123">Dieses Cmdlet ruft alle Rechenknoten aus diesem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="e0cb6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0cb6-124">PARAMETERS</span></span>

### <span data-ttu-id="e0cb6-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e0cb6-125">-BatchContext</span></span>
<span data-ttu-id="e0cb6-126">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e0cb6-127">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e0cb6-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e0cb6-129">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e0cb6-130">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e0cb6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cb6-131">-DefaultProfile</span></span>
<span data-ttu-id="e0cb6-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0cb6-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="e0cb6-133">-Filter</span></span>
<span data-ttu-id="e0cb6-134">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="e0cb6-135">Dieses Cmdlet gibt Rechenknoten zurück, die dem von diesem Parameter angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="e0cb6-136">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Rechenknoten für den Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="e0cb6-137">-ID</span><span class="sxs-lookup"><span data-stu-id="e0cb6-137">-Id</span></span>
<span data-ttu-id="e0cb6-138">Gibt die ID des Rechenknotens an, den dieses Cmdlet aus dem Pool erhält.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="e0cb6-139">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="e0cb6-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e0cb6-140">-MaxCount</span></span>
<span data-ttu-id="e0cb6-141">Gibt die maximale Anzahl der zurückzukehrenden Rechenknoten an.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="e0cb6-142">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="e0cb6-143">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="e0cb6-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="e0cb6-144">-Pool</span></span>
<span data-ttu-id="e0cb6-145">Gibt den Pool als **PSCloudPool-Objekt** an, das die Rechenknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="e0cb6-146">Verwenden Sie zum Abrufen **eines PSCloudPool-Objekts** das Get-AzBatchPool-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="e0cb6-147">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e0cb6-147">-PoolId</span></span>
<span data-ttu-id="e0cb6-148">Gibt die ID des Pools an, der die Rechenknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="e0cb6-149">-Select</span><span class="sxs-lookup"><span data-stu-id="e0cb6-149">-Select</span></span>
<span data-ttu-id="e0cb6-150">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="e0cb6-151">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="e0cb6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cb6-152">CommonParameters</span></span>
<span data-ttu-id="e0cb6-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0cb6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cb6-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0cb6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cb6-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0cb6-155">INPUTS</span></span>

### <span data-ttu-id="e0cb6-156">System.String</span><span class="sxs-lookup"><span data-stu-id="e0cb6-156">System.String</span></span>

### <span data-ttu-id="e0cb6-157">Microsoft.Azure.Commands.Batch. Models.PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="e0cb6-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="e0cb6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e0cb6-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e0cb6-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0cb6-159">OUTPUTS</span></span>

### <span data-ttu-id="e0cb6-160">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="e0cb6-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="e0cb6-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e0cb6-161">NOTES</span></span>

## <span data-ttu-id="e0cb6-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e0cb6-162">RELATED LINKS</span></span>

[<span data-ttu-id="e0cb6-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e0cb6-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="e0cb6-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="e0cb6-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="e0cb6-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="e0cb6-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="e0cb6-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="e0cb6-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="e0cb6-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e0cb6-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="e0cb6-168">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="e0cb6-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="e0cb6-169">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e0cb6-169">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
