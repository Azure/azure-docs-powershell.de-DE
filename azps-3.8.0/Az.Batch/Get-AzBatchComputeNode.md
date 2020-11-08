---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchComputeNode.md
ms.openlocfilehash: aabc7b9d6001bf2efd02d2bb03735af312edfd88
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007515"
---
# <span data-ttu-id="6ca24-101">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ca24-101">Get-AzBatchComputeNode</span></span>

## <span data-ttu-id="6ca24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ca24-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca24-103">Ruft Batch-Compute-Knoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="6ca24-103">Gets Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="6ca24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ca24-104">SYNTAX</span></span>

### <span data-ttu-id="6ca24-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ca24-105">ODataFilter (Default)</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ca24-106">ID</span><span class="sxs-lookup"><span data-stu-id="6ca24-106">Id</span></span>
```
Get-AzBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ca24-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ca24-107">ParentObject</span></span>
```
Get-AzBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca24-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ca24-108">DESCRIPTION</span></span>
<span data-ttu-id="6ca24-109">Das Cmdlet " **Get-AzBatchComputeNode** " ruft Azure Batch Compute-Knoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="6ca24-109">The **Get-AzBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="6ca24-110">Geben Sie entweder *Pool* -oder *Pool* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="6ca24-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="6ca24-111">Geben Sie den *ID-* Parameter an, um einen einzelnen Compute-Knoten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="6ca24-112">Geben Sie den *Filter* -Parameter an, um die Compute-Knoten abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="6ca24-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ca24-113">EXAMPLES</span></span>

### <span data-ttu-id="6ca24-114">Beispiel 1: Abrufen eines Compute-Knotens anhand der ID</span><span class="sxs-lookup"><span data-stu-id="6ca24-114">Example 1: Get a compute node by ID</span></span>
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

<span data-ttu-id="6ca24-115">Dieser Befehl ruft den Compute-Knoten ab, dessen ID-TVM-2316545714_1-20150725t213220z aus dem Pool mit der ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="6ca24-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="6ca24-116">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-116">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="6ca24-117">Beispiel 2: Abrufen aller Leerlauf-Compute-Knoten aus einem Pool</span><span class="sxs-lookup"><span data-stu-id="6ca24-117">Example 2: Get all idle compute nodes from a pool</span></span>
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

<span data-ttu-id="6ca24-118">Dieser Befehl ruft alle Leerlauf-Compute-Knoten ab, die im Pool enthalten sind, die die ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="6ca24-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="6ca24-119">Der Befehl gibt den Leerlaufzustand mithilfe des *Filters* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="6ca24-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="6ca24-120">Beispiel 3: Abrufen aller Compute-Knoten in einem angegebenen Pool</span><span class="sxs-lookup"><span data-stu-id="6ca24-120">Example 3: Get all compute nodes in a specified pool</span></span>
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

<span data-ttu-id="6ca24-121">Dieser Befehl ruft den Pool mit der ID-Pool07 mithilfe des Get-AzBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="6ca24-121">This command gets the pool that has the ID Pool07 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="6ca24-122">Der Befehl übergibt diesen Pool mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca24-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ca24-123">Dieses Cmdlet ruft alle Compute-Knoten aus diesem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="6ca24-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="6ca24-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ca24-124">PARAMETERS</span></span>

### <span data-ttu-id="6ca24-125">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="6ca24-125">-BatchContext</span></span>
<span data-ttu-id="6ca24-126">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ca24-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6ca24-127">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ca24-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6ca24-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6ca24-129">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ca24-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6ca24-130">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6ca24-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca24-131">-DefaultProfile</span></span>
<span data-ttu-id="6ca24-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ca24-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca24-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="6ca24-133">-Filter</span></span>
<span data-ttu-id="6ca24-134">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="6ca24-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="6ca24-135">Dieses Cmdlet gibt Compute-Knoten zurück, die dem Filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="6ca24-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="6ca24-136">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Compute-Knoten für den Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca24-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

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

### <span data-ttu-id="6ca24-137">-ID</span><span class="sxs-lookup"><span data-stu-id="6ca24-137">-Id</span></span>
<span data-ttu-id="6ca24-138">Gibt die ID des Compute-Knotens an, den dieses Cmdlet aus dem Pool erhält.</span><span class="sxs-lookup"><span data-stu-id="6ca24-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="6ca24-139">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="6ca24-139">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="6ca24-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6ca24-140">-MaxCount</span></span>
<span data-ttu-id="6ca24-141">Gibt die maximale Anzahl von Compute-Knoten an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="6ca24-142">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="6ca24-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6ca24-143">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="6ca24-143">The default value is 1000.</span></span>

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

### <span data-ttu-id="6ca24-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="6ca24-144">-Pool</span></span>
<span data-ttu-id="6ca24-145">Gibt den Pool als **PSCloudPool** -Objekt an, das die Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca24-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="6ca24-146">Verwenden Sie das Get-AzBatchPool-Cmdlet, um ein **PSCloudPool** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ca24-146">To obtain a **PSCloudPool** object, use the Get-AzBatchPool cmdlet.</span></span>

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

### <span data-ttu-id="6ca24-147">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="6ca24-147">-PoolId</span></span>
<span data-ttu-id="6ca24-148">Gibt die ID des Pools an, der die Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca24-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

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

### <span data-ttu-id="6ca24-149">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="6ca24-149">-Select</span></span>
<span data-ttu-id="6ca24-150">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="6ca24-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="6ca24-151">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ca24-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="6ca24-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca24-152">CommonParameters</span></span>
<span data-ttu-id="6ca24-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca24-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca24-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ca24-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca24-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ca24-155">INPUTS</span></span>

### <span data-ttu-id="6ca24-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca24-156">System.String</span></span>

### <span data-ttu-id="6ca24-157">Microsoft.Azure.Commands.Batch. Models. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="6ca24-157">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="6ca24-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6ca24-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6ca24-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ca24-159">OUTPUTS</span></span>

### <span data-ttu-id="6ca24-160">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ca24-160">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

## <span data-ttu-id="6ca24-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ca24-161">NOTES</span></span>

## <span data-ttu-id="6ca24-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ca24-162">RELATED LINKS</span></span>

[<span data-ttu-id="6ca24-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ca24-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="6ca24-164">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="6ca24-164">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="6ca24-165">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="6ca24-165">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="6ca24-166">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="6ca24-166">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="6ca24-167">Reset-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ca24-167">Reset-AzBatchComputeNode</span></span>](./Reset-AzBatchComputeNode.md)

[<span data-ttu-id="6ca24-168">Neustart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="6ca24-168">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

[<span data-ttu-id="6ca24-169">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ca24-169">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


