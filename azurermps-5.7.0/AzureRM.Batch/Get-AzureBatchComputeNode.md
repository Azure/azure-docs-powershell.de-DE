---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: d5cbd8c37f6d527a741f5bb92211d6b4f90b8113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502625"
---
# <span data-ttu-id="ffec9-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ffec9-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="ffec9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ffec9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffec9-103">Ruft Batch-Compute-Knoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="ffec9-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffec9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffec9-104">SYNTAX</span></span>

### <span data-ttu-id="ffec9-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffec9-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffec9-106">ID</span><span class="sxs-lookup"><span data-stu-id="ffec9-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffec9-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="ffec9-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffec9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ffec9-108">DESCRIPTION</span></span>
<span data-ttu-id="ffec9-109">Das Cmdlet " **Get-AzureBatchComputeNode** " ruft Azure Batch Compute-Knoten aus einem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="ffec9-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="ffec9-110">Geben Sie entweder *Pool* -oder *Pool* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="ffec9-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="ffec9-111">Geben Sie den *ID-* Parameter an, um einen einzelnen Compute-Knoten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="ffec9-112">Geben Sie den *Filter* -Parameter an, um die Compute-Knoten abzurufen, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ffec9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ffec9-113">EXAMPLES</span></span>

### <span data-ttu-id="ffec9-114">Beispiel 1: Abrufen eines Compute-Knotens anhand der ID</span><span class="sxs-lookup"><span data-stu-id="ffec9-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="ffec9-115">Dieser Befehl ruft den Compute-Knoten ab, dessen ID-TVM-2316545714_1-20150725t213220z aus dem Pool mit der ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="ffec9-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ffec9-116">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ffec9-117">Beispiel 2: Abrufen aller Leerlauf-Compute-Knoten aus einem Pool</span><span class="sxs-lookup"><span data-stu-id="ffec9-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="ffec9-118">Dieser Befehl ruft alle Leerlauf-Compute-Knoten ab, die im Pool enthalten sind, die die ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="ffec9-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ffec9-119">Der Befehl gibt den Leerlaufzustand mithilfe des *Filters* -Parameters an.</span><span class="sxs-lookup"><span data-stu-id="ffec9-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="ffec9-120">Beispiel 3: Abrufen aller Compute-Knoten in einem angegebenen Pool</span><span class="sxs-lookup"><span data-stu-id="ffec9-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
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
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="ffec9-121">Dieser Befehl ruft den Pool mit der ID-Pool07 mithilfe des Get-AzureBatchPool-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="ffec9-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="ffec9-122">Der Befehl übergibt diesen Pool mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffec9-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ffec9-123">Dieses Cmdlet ruft alle Compute-Knoten aus diesem Pool ab.</span><span class="sxs-lookup"><span data-stu-id="ffec9-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="ffec9-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffec9-124">PARAMETERS</span></span>

### <span data-ttu-id="ffec9-125">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="ffec9-125">-BatchContext</span></span>
<span data-ttu-id="ffec9-126">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffec9-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ffec9-127">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffec9-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ffec9-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ffec9-129">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ffec9-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ffec9-130">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ffec9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffec9-131">-DefaultProfile</span></span>
<span data-ttu-id="ffec9-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ffec9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffec9-133">-Filter</span><span class="sxs-lookup"><span data-stu-id="ffec9-133">-Filter</span></span>
<span data-ttu-id="ffec9-134">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="ffec9-134">Specifies an OData filter clause.</span></span>
<span data-ttu-id="ffec9-135">Dieses Cmdlet gibt Compute-Knoten zurück, die dem Filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ffec9-135">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="ffec9-136">Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Compute-Knoten für den Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="ffec9-136">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-137">-ID</span><span class="sxs-lookup"><span data-stu-id="ffec9-137">-Id</span></span>
<span data-ttu-id="ffec9-138">Gibt die ID des Compute-Knotens an, den dieses Cmdlet aus dem Pool erhält.</span><span class="sxs-lookup"><span data-stu-id="ffec9-138">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="ffec9-139">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="ffec9-139">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-140">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ffec9-140">-MaxCount</span></span>
<span data-ttu-id="ffec9-141">Gibt die maximale Anzahl von Compute-Knoten an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-141">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="ffec9-142">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="ffec9-142">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ffec9-143">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="ffec9-143">The default value is 1000.</span></span>

```yaml
Type: Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-144">-Pool</span><span class="sxs-lookup"><span data-stu-id="ffec9-144">-Pool</span></span>
<span data-ttu-id="ffec9-145">Gibt den Pool als **PSCloudPool** -Objekt an, das die Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="ffec9-145">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="ffec9-146">Verwenden Sie das Get-AzureBatchPool-Cmdlet, um ein **PSCloudPool** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ffec9-146">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-147">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="ffec9-147">-PoolId</span></span>
<span data-ttu-id="ffec9-148">Gibt die ID des Pools an, der die Compute-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="ffec9-148">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-149">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="ffec9-149">-Select</span></span>
<span data-ttu-id="ffec9-150">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="ffec9-150">Specifies an OData select clause.</span></span>
<span data-ttu-id="ffec9-151">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ffec9-151">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffec9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffec9-152">CommonParameters</span></span>
<span data-ttu-id="ffec9-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffec9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffec9-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffec9-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffec9-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ffec9-155">INPUTS</span></span>

### <span data-ttu-id="ffec9-156">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ffec9-156">BatchAccountContext</span></span>
<span data-ttu-id="ffec9-157">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffec9-157">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ffec9-158">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="ffec9-158">PSCloudPool</span></span>
<span data-ttu-id="ffec9-159">Der Parameter "Pool" akzeptiert den Wert vom Typ "PSCloudPool" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffec9-159">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="ffec9-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ffec9-160">OUTPUTS</span></span>

### <span data-ttu-id="ffec9-161">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ffec9-161">PSComputeNode</span></span>

## <span data-ttu-id="ffec9-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="ffec9-162">NOTES</span></span>

## <span data-ttu-id="ffec9-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ffec9-163">RELATED LINKS</span></span>

[<span data-ttu-id="ffec9-164">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ffec9-164">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="ffec9-165">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ffec9-165">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="ffec9-166">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="ffec9-166">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="ffec9-167">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ffec9-167">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="ffec9-168">Reset-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ffec9-168">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="ffec9-169">Neustart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ffec9-169">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="ffec9-170">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ffec9-170">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


