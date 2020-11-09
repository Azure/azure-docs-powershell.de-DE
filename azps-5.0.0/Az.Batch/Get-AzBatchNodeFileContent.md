---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303202"
---
# <span data-ttu-id="a5243-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="a5243-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="a5243-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5243-102">SYNOPSIS</span></span>
<span data-ttu-id="a5243-103">Ruft eine Batch-Knoten Datei ab.</span><span class="sxs-lookup"><span data-stu-id="a5243-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="a5243-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5243-104">SYNTAX</span></span>

### <span data-ttu-id="a5243-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a5243-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5243-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a5243-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5243-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="a5243-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5243-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a5243-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5243-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="a5243-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5243-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="a5243-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5243-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5243-111">DESCRIPTION</span></span>
<span data-ttu-id="a5243-112">Das Cmdlet " **Get-AzBatchNodeFileContent** " Ruft eine Azure-Batch-Knoten Datei ab und speichert Sie als Datei oder in einem Stream.</span><span class="sxs-lookup"><span data-stu-id="a5243-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="a5243-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5243-113">EXAMPLES</span></span>

### <span data-ttu-id="a5243-114">Beispiel 1: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="a5243-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a5243-115">Dieser Befehl ruft die Knoten Datei mit dem Namen StdOut.txt ab und speichert Sie im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a5243-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a5243-116">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task01 für den Auftrag mit der ID Job01 hat.</span><span class="sxs-lookup"><span data-stu-id="a5243-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="a5243-117">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a5243-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a5243-118">Beispiel 2: Abrufen einer Batch-Knoten Datei und Speichern der Datei in einem angegebenen Dateipfad mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a5243-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a5243-119">Dieser Befehl ruft die Knoten Datei mit dem Namen StdErr.txt mithilfe des Get-AzBatchNodeFile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="a5243-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="a5243-120">Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5243-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a5243-121">Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a5243-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="a5243-122">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task02 für den Auftrag enthält, der die ID Job02 hat.</span><span class="sxs-lookup"><span data-stu-id="a5243-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="a5243-123">Beispiel 3: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="a5243-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a5243-124">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5243-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a5243-125">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus der Aufgabe ab, die die ID-Task11 für den Auftrag mit der ID Job03 hat.</span><span class="sxs-lookup"><span data-stu-id="a5243-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="a5243-126">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="a5243-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="a5243-127">Beispiel 4: Abrufen einer Knoten Datei von einem Compute-Knoten und speichern</span><span class="sxs-lookup"><span data-stu-id="a5243-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a5243-128">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="a5243-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a5243-129">Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a5243-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a5243-130">Beispiel 5: Abrufen einer Knoten Datei aus einem Compute-Knoten und speichern mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a5243-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="a5243-131">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt mithilfe von Get-AzBatchNodeFile aus dem Compute-Knoten ab, der die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="a5243-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="a5243-132">Der Compute-Knoten befindet sich im Pool mit der ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="a5243-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a5243-133">Der Befehl übergibt diese Knoten Datei an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5243-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="a5243-134">Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a5243-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="a5243-135">Beispiel 6: Abrufen einer Knoten Datei aus einem Compute-Knoten und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="a5243-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a5243-136">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a5243-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a5243-137">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="a5243-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="a5243-138">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="a5243-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="a5243-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5243-139">PARAMETERS</span></span>

### <span data-ttu-id="a5243-140">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a5243-140">-BatchContext</span></span>
<span data-ttu-id="a5243-141">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5243-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a5243-142">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5243-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a5243-143">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a5243-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a5243-144">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5243-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a5243-145">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="a5243-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a5243-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="a5243-146">-ByteRangeEnd</span></span>
<span data-ttu-id="a5243-147">Das Ende des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5243-147">The end of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="a5243-148">-ByteRangeStart</span></span>
<span data-ttu-id="a5243-149">Der Anfang des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5243-149">The start of the byte range to be downloaded.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a5243-150">-ComputeNodeId</span></span>
<span data-ttu-id="a5243-151">Gibt die ID des Compute-Knotens an, der die vom Cmdlet zurückgegebene Knoten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="a5243-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5243-152">-DefaultProfile</span></span>
<span data-ttu-id="a5243-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5243-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5243-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="a5243-154">-DestinationPath</span></span>
<span data-ttu-id="a5243-155">Gibt den Dateipfad an, in dem dieses Cmdlet die Knoten Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="a5243-155">Specifies the file path where this cmdlet saves the node file.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="a5243-156">-DestinationStream</span></span>
<span data-ttu-id="a5243-157">Gibt den Datenstrom an, in den das Cmdlet den Inhalt der Knoten Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="a5243-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="a5243-158">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.</span><span class="sxs-lookup"><span data-stu-id="a5243-158">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-159">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5243-159">-InputObject</span></span>
<span data-ttu-id="a5243-160">Gibt die Datei an, die dieses Cmdlet erhält, als **PSNodeFile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5243-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="a5243-161">Verwenden Sie das Get-AzBatchNodeFile-Cmdlet, um ein Knoten Dateiobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5243-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="a5243-162">-JobId</span></span>
<span data-ttu-id="a5243-163">Gibt die ID des Auftrags an, der die Ziel Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="a5243-163">Specifies the ID of the job that contains the target task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-164">-Path</span><span class="sxs-lookup"><span data-stu-id="a5243-164">-Path</span></span>
<span data-ttu-id="a5243-165">Der Pfad der Knoten Datei, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5243-165">The path of the node file to download.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-166">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="a5243-166">-PoolId</span></span>
<span data-ttu-id="a5243-167">Gibt die ID des Pools an, der den Compute-Knoten enthält, der die Knoten Datei enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a5243-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-168">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="a5243-168">-TaskId</span></span>
<span data-ttu-id="a5243-169">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="a5243-169">Specifies the ID of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5243-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5243-170">CommonParameters</span></span>
<span data-ttu-id="a5243-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5243-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5243-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5243-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5243-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5243-173">INPUTS</span></span>

### <span data-ttu-id="a5243-174">System. String</span><span class="sxs-lookup"><span data-stu-id="a5243-174">System.String</span></span>

### <span data-ttu-id="a5243-175">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="a5243-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="a5243-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a5243-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a5243-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5243-177">OUTPUTS</span></span>

### <span data-ttu-id="a5243-178">System. void</span><span class="sxs-lookup"><span data-stu-id="a5243-178">System.Void</span></span>

## <span data-ttu-id="a5243-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5243-179">NOTES</span></span>

## <span data-ttu-id="a5243-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5243-180">RELATED LINKS</span></span>

[<span data-ttu-id="a5243-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a5243-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a5243-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="a5243-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="a5243-183">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a5243-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
