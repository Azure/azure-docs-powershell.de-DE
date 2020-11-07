---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 92c485a743372eff7ddb8725172ac4d9bb030d22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664291"
---
# <span data-ttu-id="67997-101">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="67997-101">Get-AzureBatchNodeFileContent</span></span>

## <span data-ttu-id="67997-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67997-102">SYNOPSIS</span></span>
<span data-ttu-id="67997-103">Ruft eine Batch-Knoten Datei ab.</span><span class="sxs-lookup"><span data-stu-id="67997-103">Gets a Batch node file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67997-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67997-104">SYNTAX</span></span>

### <span data-ttu-id="67997-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="67997-105">Task_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67997-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="67997-106">Task_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Name] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67997-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="67997-107">ComputeNode_Id_Path</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67997-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="67997-108">ComputeNode_Id_Stream</span></span>
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67997-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="67997-109">InputObject_Path</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67997-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="67997-110">InputObject_Stream</span></span>
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67997-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67997-111">DESCRIPTION</span></span>
<span data-ttu-id="67997-112">Das Cmdlet " **Get-AzureBatchNodeFileContent** " Ruft eine Azure-Batch-Knoten Datei ab und speichert Sie als Datei oder in einem Stream.</span><span class="sxs-lookup"><span data-stu-id="67997-112">The **Get-AzureBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="67997-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67997-113">EXAMPLES</span></span>

### <span data-ttu-id="67997-114">Beispiel 1: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="67997-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Name "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="67997-115">Dieser Befehl ruft die Knoten Datei mit dem Namen StdOut.txt ab und speichert Sie im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="67997-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="67997-116">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task01 für den Auftrag mit der ID Job01 hat.</span><span class="sxs-lookup"><span data-stu-id="67997-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="67997-117">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="67997-117">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="67997-118">Beispiel 2: Abrufen einer Batch-Knoten Datei und Speichern der Datei in einem angegebenen Dateipfad mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="67997-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Name "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="67997-119">Dieser Befehl ruft die Knoten Datei mit dem Namen StdErr.txt mithilfe des Get-AzureBatchNodeFile-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="67997-119">This command gets the node file that is named StdErr.txt by using the Get-AzureBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="67997-120">Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67997-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="67997-121">Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="67997-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="67997-122">Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task02 für den Auftrag enthält, der die ID Job02 hat.</span><span class="sxs-lookup"><span data-stu-id="67997-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="67997-123">Beispiel 3: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="67997-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Name "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="67997-124">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="67997-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="67997-125">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus der Aufgabe ab, die die ID-Task11 für den Auftrag mit der ID Job03 hat.</span><span class="sxs-lookup"><span data-stu-id="67997-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="67997-126">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="67997-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="67997-127">Beispiel 4: Abrufen einer Knoten Datei von einem Compute-Knoten und speichern</span><span class="sxs-lookup"><span data-stu-id="67997-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="67997-128">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="67997-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="67997-129">Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="67997-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="67997-130">Beispiel 5: Abrufen einer Knoten Datei aus einem Compute-Knoten und speichern mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="67997-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="67997-131">Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt mithilfe von Get-AzureBatchNodeFile aus dem Compute-Knoten ab, der die ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="67997-131">This command gets the node file Startup\StdOut.txt by using Get-AzureBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="67997-132">Der Compute-Knoten befindet sich im Pool mit der ID Pool01.</span><span class="sxs-lookup"><span data-stu-id="67997-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="67997-133">Der Befehl übergibt diese Knoten Datei an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67997-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="67997-134">Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="67997-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="67997-135">Beispiel 6: Abrufen einer Knoten Datei aus einem Compute-Knoten und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="67997-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="67997-136">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="67997-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="67997-137">Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.</span><span class="sxs-lookup"><span data-stu-id="67997-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="67997-138">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="67997-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="67997-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="67997-139">PARAMETERS</span></span>

### <span data-ttu-id="67997-140">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="67997-140">-BatchContext</span></span>
<span data-ttu-id="67997-141">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="67997-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="67997-142">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67997-142">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="67997-143">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="67997-143">-ByteRangeEnd</span></span>
<span data-ttu-id="67997-144">Das Ende des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="67997-144">The end of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="67997-145">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="67997-145">-ByteRangeStart</span></span>
<span data-ttu-id="67997-146">Der Anfang des Bytebereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="67997-146">The start of the byte range to be downloaded.</span></span>
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

### <span data-ttu-id="67997-147">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="67997-147">-ComputeNodeId</span></span>
<span data-ttu-id="67997-148">Gibt die ID des Compute-Knotens an, der die vom Cmdlet zurückgegebene Knoten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="67997-148">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="67997-149">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="67997-149">-DestinationPath</span></span>
<span data-ttu-id="67997-150">Gibt den Dateipfad an, in dem dieses Cmdlet die Knoten Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="67997-150">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="67997-151">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="67997-151">-DestinationStream</span></span>
<span data-ttu-id="67997-152">Gibt den Datenstrom an, in den das Cmdlet den Inhalt der Knoten Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="67997-152">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="67997-153">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.</span><span class="sxs-lookup"><span data-stu-id="67997-153">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="67997-154">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67997-154">-InputObject</span></span>
<span data-ttu-id="67997-155">Gibt die Datei an, die dieses Cmdlet erhält, als **PSNodeFile** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="67997-155">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="67997-156">Verwenden Sie das Get-AzureBatchNodeFile-Cmdlet, um ein Knoten Dateiobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="67997-156">To obtain a node file object, use the Get-AzureBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="67997-157">-JobId</span><span class="sxs-lookup"><span data-stu-id="67997-157">-JobId</span></span>
<span data-ttu-id="67997-158">Gibt die ID des Auftrags an, der die Ziel Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="67997-158">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="67997-159">-Name</span><span class="sxs-lookup"><span data-stu-id="67997-159">-Name</span></span>
<span data-ttu-id="67997-160">Gibt den Namen der Knoten Datei an, die dieses Cmdlet abruft.</span><span class="sxs-lookup"><span data-stu-id="67997-160">Specifies the name of the node file that this cmdlet retrieves.</span></span>
<span data-ttu-id="67997-161">Sie können keine Platzhalterzeichen angeben.</span><span class="sxs-lookup"><span data-stu-id="67997-161">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67997-162">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="67997-162">-PoolId</span></span>
<span data-ttu-id="67997-163">Gibt die ID des Pools an, der den Compute-Knoten enthält, der die Knoten Datei enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="67997-163">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67997-164">-Task-Nr</span><span class="sxs-lookup"><span data-stu-id="67997-164">-TaskId</span></span>
<span data-ttu-id="67997-165">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="67997-165">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="67997-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67997-166">-DefaultProfile</span></span>
<span data-ttu-id="67997-167">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67997-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67997-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67997-168">CommonParameters</span></span>
<span data-ttu-id="67997-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67997-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67997-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67997-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67997-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67997-171">INPUTS</span></span>

### <span data-ttu-id="67997-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="67997-172">BatchAccountContext</span></span>
<span data-ttu-id="67997-173">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="67997-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="67997-174">PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="67997-174">PSNodeFile</span></span>
<span data-ttu-id="67997-175">Der Parameter "Inputobject" akzeptiert den Wert vom Typ "PSNodeFile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="67997-175">Parameter 'InputObject' accepts value of type 'PSNodeFile' from the pipeline</span></span>

## <span data-ttu-id="67997-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67997-176">OUTPUTS</span></span>

## <span data-ttu-id="67997-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="67997-177">NOTES</span></span>

## <span data-ttu-id="67997-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67997-178">RELATED LINKS</span></span>

[<span data-ttu-id="67997-179">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="67997-179">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="67997-180">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="67997-180">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="67997-181">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="67997-181">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


