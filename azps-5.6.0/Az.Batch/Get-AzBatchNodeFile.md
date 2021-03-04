---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 38ED2854-23D0-400E-A5C8-239346B2AF99
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFile.md
ms.openlocfilehash: 0169748ffc6fa2004fe8b0ade542d288677776b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946349"
---
# <span data-ttu-id="01c33-101">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="01c33-101">Get-AzBatchNodeFile</span></span>

## <span data-ttu-id="01c33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c33-102">SYNOPSIS</span></span>
<span data-ttu-id="01c33-103">Ruft die Eigenschaften von Batchknotendateien ab.</span><span class="sxs-lookup"><span data-stu-id="01c33-103">Gets the properties of Batch node files.</span></span>

## <span data-ttu-id="01c33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01c33-104">SYNTAX</span></span>

### <span data-ttu-id="01c33-105">ComputeNode_Id (Standard)</span><span class="sxs-lookup"><span data-stu-id="01c33-105">ComputeNode_Id (Default)</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [[-Path] <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c33-106">Task_Id</span><span class="sxs-lookup"><span data-stu-id="01c33-106">Task_Id</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [[-Path] <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c33-107">Task_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="01c33-107">Task_ODataFilter</span></span>
```
Get-AzBatchNodeFile -JobId <String> -TaskId <String> [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c33-108">ParentTask</span><span class="sxs-lookup"><span data-stu-id="01c33-108">ParentTask</span></span>
```
Get-AzBatchNodeFile [[-Task] <PSCloudTask>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01c33-109">ComputeNode_ODataFilter</span><span class="sxs-lookup"><span data-stu-id="01c33-109">ComputeNode_ODataFilter</span></span>
```
Get-AzBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Recursive] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01c33-110">ParentComputeNode</span><span class="sxs-lookup"><span data-stu-id="01c33-110">ParentComputeNode</span></span>
```
Get-AzBatchNodeFile [[-ComputeNode] <PSComputeNode>] [-Filter <String>] [-MaxCount <Int32>] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01c33-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01c33-111">DESCRIPTION</span></span>
<span data-ttu-id="01c33-112">Das **Get-AzBatchNodeFile-Cmdlet** ruft die Eigenschaften der Azure Batch-Knotendateien einer Aufgabe oder eines Computeknotens ab.</span><span class="sxs-lookup"><span data-stu-id="01c33-112">The **Get-AzBatchNodeFile** cmdlet gets the properties of the Azure Batch node files of a task or compute node.</span></span>
<span data-ttu-id="01c33-113">Zum Einen der Ergebnisse können Sie einen OData-Filter (Open Data Protocol) angeben.</span><span class="sxs-lookup"><span data-stu-id="01c33-113">To narrow your results, you can specify an Open Data Protocol (OData) filter.</span></span>
<span data-ttu-id="01c33-114">Wenn Sie eine Aufgabe, aber keinen Filter angeben, gibt dieses Cmdlet Eigenschaften für alle Knotendateien für diese Aufgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="01c33-114">If you specify a task, but not a filter, this cmdlet returns properties for all node files for that task.</span></span>
<span data-ttu-id="01c33-115">Wenn Sie einen Computeknoten, aber keinen Filter angeben, gibt dieses Cmdlet Eigenschaften für alle Knotendateien für diesen Computeknoten zurück.</span><span class="sxs-lookup"><span data-stu-id="01c33-115">If you specify a compute node, but not a filter, this cmdlet returns properties for all node files for that compute node.</span></span>

## <span data-ttu-id="01c33-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01c33-116">EXAMPLES</span></span>

### <span data-ttu-id="01c33-117">Beispiel 1: Erhalten der Eigenschaften einer Knotendatei, die einer Aufgabe zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="01c33-117">Example 1: Get the properties of a node file associated with a task</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Path "Stdout.txt" -BatchContext $Context
IsDirectory Name          Properties                                      Url

----------- ----          ----------                                      ---

False       StdOut.txt    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-118">Dieser Befehl ruft die Eigenschaften der StdOut.txt-Knotendatei ab, die der Aufgabe zugeordnet ist, die die ID Task26 im Auftrag mit der ID Job-000001 enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-118">This command gets the properties of the StdOut.txt node file associated with the task that has the ID Task26 in the job that has the ID Job-000001.</span></span>
<span data-ttu-id="01c33-119">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="01c33-119">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="01c33-120">Beispiel 2: Herunterladen der Eigenschaften von Knotendateien, die einer Aufgabe zugeordnet sind, mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="01c33-120">Example 2: Get the properties of node files associated with a task by using a filter</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job-00002" -TaskId "Task26" -Filter "startswith(name,'St')" -BatchContext $Context
IsDirectory Name        Properties                                      Url

----------- ----        ----------                                      ---

False       StdErr.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt  Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-121">Dieser Befehl ruft die Eigenschaften der Knotendateien ab, deren Namen mit "st" beginnen und der Aufgabe zugeordnet sind, die die ID Task26 unter Auftrag mit der ID Job-00002 hat.</span><span class="sxs-lookup"><span data-stu-id="01c33-121">This command gets the properties of the node files whose names start with st and are associated with task that has the ID Task26 under job that has the ID Job-00002.</span></span>

### <span data-ttu-id="01c33-122">Beispiel 3: Rekursiv die Eigenschaften von Knotendateien erhalten, die einer Aufgabe zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="01c33-122">Example 3: Recursively get the properties of node files associated with a task</span></span>
```
PS C:\>Get-AzBatchTask "Job-00003" "Task31" -BatchContext $Context | Get-AzBatchNodeFile -Recursive -BatchContext $Context
IsDirectory Name             Properties                                      Url

----------- ----             ----------                                      ---

False       ProcessEnv.cmd   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdErr.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       StdOut.txt       Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        wd                                                               https://cmdletexample.westus.Batch.contoso...
False       wd\newFile.txt   Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-123">Dieser Befehl ruft die Eigenschaften aller Dateien ab, die der Aufgabe zugeordnet sind, die die ID Task31 in Job-00003 hat.</span><span class="sxs-lookup"><span data-stu-id="01c33-123">This command gets the properties of all files associated with the task that has the ID Task31 in job Job-00003.</span></span>
<span data-ttu-id="01c33-124">Dieser Befehl gibt den *Parameter Rekursiv* an.</span><span class="sxs-lookup"><span data-stu-id="01c33-124">This command specifies the *Recursive* parameter.</span></span>
<span data-ttu-id="01c33-125">Daher führt das Cmdlet eine rekursive Dateisuche aus und gibt die wd\newFile.txt zurück.</span><span class="sxs-lookup"><span data-stu-id="01c33-125">Therefore, the cmdlet performs a recursive file search is performed, and returns the wd\newFile.txt node file.</span></span>

### <span data-ttu-id="01c33-126">Beispiel 4: Herunterladen einer einzelnen Datei aus einem Computeknoten</span><span class="sxs-lookup"><span data-stu-id="01c33-126">Example 4: Get a single file from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context
IsDirectory Name                    Properties                                      Url
----------- ----                    ----------                                      ---
False       startup\stdout.txt      Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-127">Dieser Befehl ruft die Datei mit dem Namen Startup\StdOut.txt aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID-Pool22 enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-127">This command gets the file that is named Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

### <span data-ttu-id="01c33-128">Beispiel 5: Herunterladen aller Dateien unter einem Ordner aus einem Computeknoten</span><span class="sxs-lookup"><span data-stu-id="01c33-128">Example 5: Get all files under a folder from a compute node</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool22" -ComputeNodeId "ComputeNode01" -Filter "startswith(name,'startup')" -Recursive -BatchContext $Context
IsDirectory Name                      Properties                                      Url
----------- ----                      ----------                                      ---
True        startup                                                                   https://cmdletexample.westus.Batch.contoso...
False       startup\ProcessEnv.cmd    Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stderr.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
False       startup\stdout.txt        Microsoft.Azure.Commands.Batch.Models.PSFile... https://cmdletexample.westus.Batch.contoso...
True        startup\wd                                                                https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-129">Dieser Befehl ruft alle Dateien unter dem Startordner aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID-Pool22 enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-129">This command gets all the files under the startup folder from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>
<span data-ttu-id="01c33-130">Dieses Cmdlet gibt den *Parameter Rekursiv* an.</span><span class="sxs-lookup"><span data-stu-id="01c33-130">This cmdlet specifies the *Recursive* parameter.</span></span>

### <span data-ttu-id="01c33-131">Beispiel 6: Herunterladen von Dateien aus dem Stammordner eines Computeknotens</span><span class="sxs-lookup"><span data-stu-id="01c33-131">Example 6: Get files from the root folder of a compute node</span></span>
```
PS C:\>Get-AzBatchComputeNode "Pool22" -Id "ComputeNode01" -BatchContext $Context | Get-AzBatchNodeFile -BatchContext $Context
IsDirectory Name           Properties       Url
----------- ----           ----------       ---
True        shared                          https://cmdletexample.westus.Batch.contoso...
True        startup                         https://cmdletexample.westus.Batch.contoso...
True        workitems                       https://cmdletexample.westus.Batch.contoso...
```

<span data-ttu-id="01c33-132">Dieser Befehl ruft alle Dateien im Stammordner des Computeknotens ab, der die ID ComputeNode01 im Pool mit dem ID-Pool22 enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-132">This command gets all the files at the root folder of the compute node that has the ID ComputeNode01 in the pool that has the ID Pool22.</span></span>

## <span data-ttu-id="01c33-133">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01c33-133">PARAMETERS</span></span>

### <span data-ttu-id="01c33-134">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="01c33-134">-BatchContext</span></span>
<span data-ttu-id="01c33-135">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01c33-135">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="01c33-136">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c33-136">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="01c33-137">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="01c33-137">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="01c33-138">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c33-138">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="01c33-139">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="01c33-139">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="01c33-140">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="01c33-140">-ComputeNode</span></span>
<span data-ttu-id="01c33-141">Gibt den Computeknoten als **PSComputeNode-Objekt** an, der die Batchknotendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-141">Specifies the compute node, as a **PSComputeNode** object, that contains the Batch node files.</span></span>
<span data-ttu-id="01c33-142">Verwenden Sie zum Abrufen eines Computeknotenobjekts das Get-AzBatchComputeNode Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c33-142">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="01c33-143">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="01c33-143">-ComputeNodeId</span></span>
<span data-ttu-id="01c33-144">Gibt die ID des Computeknotens an, der die Batchknotendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-144">Specifies the ID of the compute node that contains the Batch node files.</span></span>

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

### <span data-ttu-id="01c33-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c33-145">-DefaultProfile</span></span>
<span data-ttu-id="01c33-146">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01c33-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01c33-147">-Filter</span><span class="sxs-lookup"><span data-stu-id="01c33-147">-Filter</span></span>
<span data-ttu-id="01c33-148">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="01c33-148">Specifies an OData filter clause.</span></span>
<span data-ttu-id="01c33-149">Dieses Cmdlet gibt Eigenschaften für Knotendateien zurück, die dem von diesem Parameter angegebenen Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="01c33-149">This cmdlet returns properties for node files that match the filter that this parameter specifies.</span></span>

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

### <span data-ttu-id="01c33-150">-JobId</span><span class="sxs-lookup"><span data-stu-id="01c33-150">-JobId</span></span>
<span data-ttu-id="01c33-151">Gibt die ID des Auftrags an, der die Zielaufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="01c33-151">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="01c33-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="01c33-152">-MaxCount</span></span>
<span data-ttu-id="01c33-153">Gibt die maximale Anzahl von Knotendateien an, für die dieses Cmdlet Eigenschaften zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="01c33-153">Specifies the maximum number of node files for which this cmdlet returns properties.</span></span>
<span data-ttu-id="01c33-154">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c33-154">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="01c33-155">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="01c33-155">The default value is 1000.</span></span>

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

### <span data-ttu-id="01c33-156">-Path</span><span class="sxs-lookup"><span data-stu-id="01c33-156">-Path</span></span>
<span data-ttu-id="01c33-157">Gibt den Pfad der Knotendatei an, für die dieses Cmdlet Eigenschaften abruft.</span><span class="sxs-lookup"><span data-stu-id="01c33-157">Specifies the path of the node file for which this cmdlet retrieves properties.</span></span>
<span data-ttu-id="01c33-158">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="01c33-158">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="01c33-159">-PoolId</span><span class="sxs-lookup"><span data-stu-id="01c33-159">-PoolId</span></span>
<span data-ttu-id="01c33-160">Gibt die ID des Pools an, der den Computeknoten enthält, aus dem Eigenschaften von Knotendateien zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="01c33-160">Specifies the ID of the pool that contains the compute node from which to get properties of node files.</span></span>

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

### <span data-ttu-id="01c33-161">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="01c33-161">-Recursive</span></span>
<span data-ttu-id="01c33-162">Gibt an, dass dieses Cmdlet eine rekursive Liste von Dateien zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="01c33-162">Indicates that this cmdlet returns a recursive list of files.</span></span>
<span data-ttu-id="01c33-163">Andernfalls werden nur die Dateien im Stammordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01c33-163">Otherwise, it returns only the files in the root folder.</span></span>

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

### <span data-ttu-id="01c33-164">-Aufgabe</span><span class="sxs-lookup"><span data-stu-id="01c33-164">-Task</span></span>
<span data-ttu-id="01c33-165">Gibt die Aufgabe als **PSCloudTask-Objekt** an, dem die Knotendateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="01c33-165">Specifies the task, as a **PSCloudTask** object, with which the node files are associated.</span></span>
<span data-ttu-id="01c33-166">Verwenden Sie zum Abrufen eines Aufgabenobjekts das Get-AzBatchTask Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01c33-166">To obtain a task object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="01c33-167">-TaskId</span><span class="sxs-lookup"><span data-stu-id="01c33-167">-TaskId</span></span>
<span data-ttu-id="01c33-168">Gibt die ID der Aufgabe an, für die dieses Cmdlet Eigenschaften von Knotendateien erhält.</span><span class="sxs-lookup"><span data-stu-id="01c33-168">Specifies the ID of the task for which this cmdlet gets properties of node files.</span></span>

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

### <span data-ttu-id="01c33-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c33-169">CommonParameters</span></span>
<span data-ttu-id="01c33-170">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c33-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c33-171">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01c33-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c33-172">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01c33-172">INPUTS</span></span>

### <span data-ttu-id="01c33-173">System.String</span><span class="sxs-lookup"><span data-stu-id="01c33-173">System.String</span></span>

### <span data-ttu-id="01c33-174">Microsoft.Azure.Commands.Batch. Models.PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="01c33-174">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="01c33-175">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="01c33-175">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="01c33-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="01c33-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="01c33-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01c33-177">OUTPUTS</span></span>

### <span data-ttu-id="01c33-178">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="01c33-178">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

## <span data-ttu-id="01c33-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01c33-179">NOTES</span></span>

## <span data-ttu-id="01c33-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01c33-180">RELATED LINKS</span></span>

[<span data-ttu-id="01c33-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="01c33-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="01c33-182">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="01c33-182">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="01c33-183">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="01c33-183">Get-AzBatchNodeFileContent</span></span>](./Get-AzBatchNodeFileContent.md)

[<span data-ttu-id="01c33-184">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="01c33-184">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="01c33-185">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="01c33-185">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
