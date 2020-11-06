---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: c399c967fbff477d487a27e944929855e9268744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502237"
---
# <span data-ttu-id="7084e-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="7084e-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="7084e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7084e-102">SYNOPSIS</span></span>
<span data-ttu-id="7084e-103">Ruft eine Batch-Knoten Datei ab.</span><span class="sxs-lookup"><span data-stu-id="7084e-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7084e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7084e-104">SYNTAX</span></span>

### <span data-ttu-id="7084e-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="7084e-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7084e-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="7084e-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7084e-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="7084e-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7084e-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="7084e-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7084e-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="7084e-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7084e-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="7084e-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7084e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7084e-111">DESCRIPTION</span></span>
<span data-ttu-id="7084e-112">Das Cmdlet " **Get-AzureBatchNodeFileContent** " Ruft eine Azure-Batch-Knoten Datei ab und speichert Sie als Datei oder in einem Stream.</span><span class="sxs-lookup"><span data-stu-id="7084e-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="7084e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7084e-113">EXAMPLES</span></span>

### <span data-ttu-id="7084e-114">Beispiel 1: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="7084e-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="7084e-115">Dieser Befehl ruft die Knoten Datei mit dem Namen StdOut.txt ab und speichert Sie im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="7084e-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="7084e-116">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task01 für den Auftrag mit der ID Job01 hat.</span><span class="sxs-lookup"><span data-stu-id="7084e-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="7084e-117">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7084e-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="7084e-118">Beispiel 2: Abrufen einer Batch-Knoten Datei und Speichern der Datei in einem angegebenen Dateipfad mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7084e-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="7084e-119">Dieser Befehl ruft die Knoten Datei mit dem Namen StdErr.txt mithilfe des Get-AzureBatchNodeFile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="7084e-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="7084e-120">Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7084e-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7084e-121">Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="7084e-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="7084e-122">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task02 für den Auftrag enthält, der die ID Job02 hat.</span><span class="sxs-lookup"><span data-stu-id="7084e-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="7084e-123">Beispiel 3: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="7084e-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="7084e-124">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7084e-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="7084e-125">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus der Aufgabe ab, die die ID-Task11 für den Auftrag mit der ID Job03 hat.</span><span class="sxs-lookup"><span data-stu-id="7084e-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="7084e-126">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="7084e-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="7084e-127">Beispiel 4: Abrufen einer Knoten Datei von einem Compute-Knoten und speichern</span><span class="sxs-lookup"><span data-stu-id="7084e-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="7084e-128">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="7084e-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="7084e-129">Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="7084e-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="7084e-130">Beispiel 5: Abrufen einer Knoten Datei aus einem Compute-Knoten und speichern mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7084e-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="7084e-131">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt mithilfe von Get-AzureBatchNodeFile aus dem Compute-Knoten ab, der die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="7084e-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="7084e-132">Der Compute-Knoten befindet sich im Pool mit der ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="7084e-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="7084e-133">Der Befehl übergibt diese Knoten Datei an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7084e-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="7084e-134">Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="7084e-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="7084e-135">Beispiel 6: Abrufen einer Knoten Datei aus einem Compute-Knoten und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="7084e-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="7084e-136">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7084e-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="7084e-137">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="7084e-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="7084e-138">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="7084e-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="7084e-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="7084e-139">PARAMETERS</span></span>

### <span data-ttu-id="7084e-140">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="7084e-140">-BatchContext</span></span>
<span data-ttu-id="7084e-141">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7084e-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7084e-142">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7084e-142">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7084e-143">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7084e-143">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7084e-144">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="7084e-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7084e-145">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7084e-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7084e-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7084e-146">-ByteRangeEnd</span></span>
<span data-ttu-id="7084e-147">Das Ende des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7084e-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="7084e-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="7084e-148">-ByteRangeStart</span></span>
<span data-ttu-id="7084e-149">Der Anfang des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7084e-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="7084e-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="7084e-150">-ComputeNodeId</span></span>
<span data-ttu-id="7084e-151">Gibt die ID des Compute-Knotens an, der die vom Cmdlet zurückgegebene Knoten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="7084e-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="7084e-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7084e-152">-DefaultProfile</span></span>
<span data-ttu-id="7084e-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7084e-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7084e-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="7084e-154">-DestinationPath</span></span>
<span data-ttu-id="7084e-155">Gibt den Dateipfad an, in dem dieses Cmdlet die Knoten Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="7084e-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="7084e-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="7084e-156">-DestinationStream</span></span>
<span data-ttu-id="7084e-157">Gibt den Datenstrom an, in den das Cmdlet den Inhalt der Knoten Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="7084e-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="7084e-158">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.</span><span class="sxs-lookup"><span data-stu-id="7084e-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="7084e-159">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7084e-159">-InputObject</span></span>
<span data-ttu-id="7084e-160">Gibt die Datei an, die dieses Cmdlet erhält, als **PSNodeFile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="7084e-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="7084e-161">Verwenden Sie das Get-AzureBatchNodeFile-Cmdlet, um ein Knoten Dateiobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7084e-161">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="7084e-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="7084e-162">-JobId</span></span>
<span data-ttu-id="7084e-163">Gibt die ID des Auftrags an, der die Ziel Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="7084e-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="7084e-164">-Path</span><span class="sxs-lookup"><span data-stu-id="7084e-164">-Path</span></span>
<span data-ttu-id="7084e-165">Der Pfad der Knoten Datei, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7084e-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="7084e-166">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="7084e-166">-PoolId</span></span>
<span data-ttu-id="7084e-167">Gibt die ID des Pools an, der den Compute-Knoten enthält, der die Knoten Datei enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7084e-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7084e-168">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="7084e-168">-TaskId</span></span>
<span data-ttu-id="7084e-169">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="7084e-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="7084e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7084e-170">CommonParameters</span></span>
<span data-ttu-id="7084e-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7084e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7084e-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7084e-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7084e-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7084e-173">INPUTS</span></span>

### <span data-ttu-id="7084e-174">System. String</span><span class="sxs-lookup"><span data-stu-id="7084e-174">System.String</span></span>

### <span data-ttu-id="7084e-175">Microsoft.Azure.Commands.Batch. Models. PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="7084e-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>
<span data-ttu-id="7084e-176">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7084e-176">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7084e-177">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7084e-177">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7084e-178">Parameter: batchcontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7084e-178">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7084e-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7084e-179">OUTPUTS</span></span>

### <span data-ttu-id="7084e-180">System. void</span><span class="sxs-lookup"><span data-stu-id="7084e-180">System.Void</span></span>

## <span data-ttu-id="7084e-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="7084e-181">NOTES</span></span>

## <span data-ttu-id="7084e-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7084e-182">RELATED LINKS</span></span>

[<span data-ttu-id="7084e-183">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7084e-183">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7084e-184">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="7084e-184">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="7084e-185">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7084e-185">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


