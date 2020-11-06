---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFile.md
ms.openlocfilehash: 580065e44f57ee8ff6ad022f425983860930b3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476237"
---
# <span data-ttu-id="74bf8-101">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="74bf8-101">Get-AzureBatchNodeFile</span></span>

## <span data-ttu-id="74bf8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="74bf8-103">Ruft die Eigenschaften von Batch-Knoten Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="74bf8-103">Gets the properties of Batch node files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74bf8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74bf8-104">SYNTAX</span></span>

### <span data-ttu-id="74bf8-105">ComputeNode_Id (Standard)</span><span class="sxs-lookup"><span data-stu-id="74bf8-105">ComputeNode_Id (Default)</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74bf8-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="74bf8-106">Task_Id</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74bf8-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="74bf8-107">Task_ODataFilter</span></span>
```
Get-AzureBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74bf8-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="74bf8-108">ParentTask</span></span>
```
Get-AzureBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74bf8-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="74bf8-109">ComputeNode_ODataFilter</span></span>
```
Get-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="74bf8-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="74bf8-110">ParentComputeNode</span></span>
```
Get-AzureBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74bf8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74bf8-111">DESCRIPTION</span></span>
<span data-ttu-id="74bf8-112">Das Cmdlet " **Get-AzureBatchNodeFile** " Ruft die Eigenschaften der Azure-Batch-Knoten Dateien eines Vorgangs oder COMPUTE-Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="74bf8-112">The **Get-AzureBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="74bf8-113">Um die Ergebnisse einzuschränken, können Sie einen OData-Filter (Open Data Protocol) angeben.</span><span class="sxs-lookup"><span data-stu-id="74bf8-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="74bf8-114">Wenn Sie eine Aufgabe, aber keinen Filter angeben, gibt dieses Cmdlet Eigenschaften für alle Knoten Dateien für diesen Vorgang zurück.</span><span class="sxs-lookup"><span data-stu-id="74bf8-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="74bf8-115">Wenn Sie einen Compute-Knoten, aber keinen Filter angeben, gibt dieses Cmdlet Eigenschaften für alle Knoten Dateien für diesen Compute-Knoten zurück.</span><span class="sxs-lookup"><span data-stu-id="74bf8-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="74bf8-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74bf8-116">EXAMPLES</span></span>

### <span data-ttu-id="74bf8-117">Beispiel 1: Abrufen der Eigenschaften einer Knoten Datei, die einem Vorgang zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="74bf8-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-118">Dieser Befehl ruft die Eigenschaften der StdOut.txt-Knoten Datei ab, die der Aufgabe zugeordnet ist, die die ID Task26 in dem Auftrag enthält, der die ID Job-000001 hat.</span><span class="sxs-lookup"><span data-stu-id="74bf8-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="74bf8-119">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="74bf8-119">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="74bf8-120">Beispiel 2: Abrufen der Eigenschaften von Knoten Dateien, die einem Vorgang zugeordnet sind, mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="74bf8-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-121">Dieser Befehl ruft die Eigenschaften der Knoten Dateien ab, deren Namen mit "St" beginnen und mit der Aufgabe verknüpft sind, die die ID Task26 unter Job enthält, die die ID Job-00002 hat.</span><span class="sxs-lookup"><span data-stu-id="74bf8-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="74bf8-122">Beispiel 3: rekursives Abrufen der Eigenschaften von Knoten Dateien, die einem Vorgang zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="74bf8-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzureBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzureBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        wd                                                               https://cmdletexample.westus.Batch.contoso... 
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-123">Dieser Befehl ruft die Eigenschaften aller Dateien ab, die der Aufgabe zugeordnet sind, die die ID Task31 in Job Job-00003.</span><span class="sxs-lookup"><span data-stu-id="74bf8-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="74bf8-124">Dieser Befehl gibt den *rekursiven* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="74bf8-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="74bf8-125">Daher führt das Cmdlet eine rekursive Dateisuche durch und gibt die wd\newFile.txt-Knoten Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="74bf8-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="74bf8-126">Beispiel 4: Abrufen einer einzelnen Datei von einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="74bf8-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-127">Dieser Befehl ruft die Datei mit dem Namen Startup\StdOut.txt aus dem Compute-Knoten ab, der über die ID-ComputeNode01 im Pool mit der ID Pool22 verfügt.</span><span class="sxs-lookup"><span data-stu-id="74bf8-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="74bf8-128">Beispiel 5: Abrufen aller Dateien unter einem Ordner von einem Compute-Knoten</span><span class="sxs-lookup"><span data-stu-id="74bf8-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso... 
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso... 
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-129">Dieser Befehl ruft alle Dateien unter dem Startordner aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool22 hat.</span><span class="sxs-lookup"><span data-stu-id="74bf8-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="74bf8-130">Dieses Cmdlet gibt den *rekursiven* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="74bf8-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="74bf8-131">Beispiel 6: Abrufen von Dateien aus dem Stammordner eines Compute-Knotens</span><span class="sxs-lookup"><span data-stu-id="74bf8-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzureBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzureBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso... 
True        startup                         https://cmdletexample.westus.Batch.contoso... 
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="74bf8-132">Dieser Befehl ruft alle Dateien im Stammordner des Compute-Knotens ab, auf dem sich die ID-ComputeNode01 im Pool mit der ID-Pool22 befindet.</span><span class="sxs-lookup"><span data-stu-id="74bf8-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="74bf8-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="74bf8-133">PARAMETERS</span></span>

### <span data-ttu-id="74bf8-134">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="74bf8-134">-BatchContext</span></span>
<span data-ttu-id="74bf8-135">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="74bf8-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="74bf8-136">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="74bf8-136">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="74bf8-137">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="74bf8-137">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="74bf8-138">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="74bf8-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="74bf8-139">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="74bf8-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="74bf8-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="74bf8-140">-ComputeNode</span></span>
<span data-ttu-id="74bf8-141">Gibt den Compute-Knoten als **PSComputeNode** -Objekt an, das die Batch-Knoten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="74bf8-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="74bf8-142">Verwenden Sie das Get-AzureBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="74bf8-142">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentComputeNode
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="74bf8-143">-ComputeNodeId</span></span>
<span data-ttu-id="74bf8-144">Gibt die ID des Compute-Knotens an, der die Batch-Knoten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="74bf8-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bf8-145">-DefaultProfile</span></span>
<span data-ttu-id="74bf8-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74bf8-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74bf8-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="74bf8-147">-Filter</span></span>
<span data-ttu-id="74bf8-148">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="74bf8-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="74bf8-149">Dieses Cmdlet gibt Eigenschaften für Knoten Dateien zurück, die dem Filter entsprechen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="74bf8-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="74bf8-150">-JobId</span></span>
<span data-ttu-id="74bf8-151">Gibt die ID des Auftrags an, der die Ziel Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="74bf8-151">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="74bf8-152">-MaxCount</span></span>
<span data-ttu-id="74bf8-153">Gibt die maximale Anzahl von Knoten Dateien an, für die dieses Cmdlet Eigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="74bf8-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="74bf8-154">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="74bf8-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="74bf8-155">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="74bf8-155">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-156">-Path</span><span class="sxs-lookup"><span data-stu-id="74bf8-156">-Path</span></span>
<span data-ttu-id="74bf8-157">Gibt den Pfad der Knoten Datei an, für die dieses Cmdlet Eigenschaften abruft.</span><span class="sxs-lookup"><span data-stu-id="74bf8-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="74bf8-158">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="74bf8-158">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, Task_Id
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-159">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="74bf8-159">-PoolId</span></span>
<span data-ttu-id="74bf8-160">Gibt die ID des Pools an, der den Compute-Knoten enthält, aus dem die Eigenschaften von Knoten Dateien abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="74bf8-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id, ComputeNode_ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-161">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="74bf8-161">-Recursive</span></span>
<span data-ttu-id="74bf8-162">Gibt an, dass dieses Cmdlet eine rekursive Liste von Dateien zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="74bf8-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="74bf8-163">Andernfalls werden nur die Dateien im Stammordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74bf8-163">Otherwise, it returns only the files in the root folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Task_ODataFilter, ParentTask, ComputeNode_ODataFilter, ParentComputeNode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-164">– Aufgabe</span><span class="sxs-lookup"><span data-stu-id="74bf8-164">-Task</span></span>
<span data-ttu-id="74bf8-165">Gibt die Aufgabe als **PSCloudTask** -Objekt an, dem die Knoten Dateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="74bf8-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="74bf8-166">Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein Aufgabenobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="74bf8-166">To obtain a task object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentTask
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-167">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="74bf8-167">-TaskId</span></span>
<span data-ttu-id="74bf8-168">Gibt die ID der Aufgabe an, für die dieses Cmdlet Eigenschaften von Knoten Dateien abruft.</span><span class="sxs-lookup"><span data-stu-id="74bf8-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id, Task_ODataFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74bf8-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bf8-169">CommonParameters</span></span>
<span data-ttu-id="74bf8-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74bf8-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bf8-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74bf8-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bf8-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74bf8-172">INPUTS</span></span>

### <span data-ttu-id="74bf8-173">System. String</span><span class="sxs-lookup"><span data-stu-id="74bf8-173">System.String</span></span>

### <span data-ttu-id="74bf8-174">Microsoft.Azure.Commands.Batch. Models. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="74bf8-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="74bf8-175">Parameter: Aufgabe (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74bf8-175">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="74bf8-176">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="74bf8-176">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="74bf8-177">Parameter: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74bf8-177">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="74bf8-178">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="74bf8-178">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="74bf8-179">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="74bf8-179">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="74bf8-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74bf8-180">OUTPUTS</span></span>

### <span data-ttu-id="74bf8-181">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="74bf8-181">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="74bf8-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="74bf8-182">NOTES</span></span>

## <span data-ttu-id="74bf8-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74bf8-183">RELATED LINKS</span></span>

[<span data-ttu-id="74bf8-184">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="74bf8-184">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="74bf8-185">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="74bf8-185">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="74bf8-186">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="74bf8-186">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="74bf8-187">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="74bf8-187">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="74bf8-188">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="74bf8-188">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


