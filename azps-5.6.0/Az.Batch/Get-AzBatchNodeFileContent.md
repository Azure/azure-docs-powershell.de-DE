---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 5790d217a63b7c2ef3aa7011d5f8a708df1dfbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934344"
---
# <span data-ttu-id="c515b-101">Get-AzBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="c515b-101">Get-AzBatchNodeFileContent</span></span>

## <span data-ttu-id="c515b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c515b-102">SYNOPSIS</span></span>
<span data-ttu-id="c515b-103">Ruft eine Batchknotendatei ab.</span><span class="sxs-lookup"><span data-stu-id="c515b-103">Gets a Batch node file.</span></span>

## <span data-ttu-id="c515b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c515b-104">SYNTAX</span></span>

### <span data-ttu-id="c515b-105">Task_Id_Path</span><span class="sxs-lookup"><span data-stu-id="c515b-105">Task_Id_Path</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c515b-106">Task_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="c515b-106">Task_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c515b-107">ComputeNode_Id_Path</span><span class="sxs-lookup"><span data-stu-id="c515b-107">ComputeNode_Id_Path</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c515b-108">ComputeNode_Id_Stream</span><span class="sxs-lookup"><span data-stu-id="c515b-108">ComputeNode_Id_Stream</span></span>
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c515b-109">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="c515b-109">InputObject_Path</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c515b-110">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="c515b-110">InputObject_Stream</span></span>
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c515b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c515b-111">DESCRIPTION</span></span>
<span data-ttu-id="c515b-112">Das **Get-AzBatchNodeFileContent-Cmdlet** ruft eine Azure Batch-Knotendatei ab und speichert sie als Datei oder in einem Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="c515b-112">The **Get-AzBatchNodeFileContent** cmdlet gets an Azure Batch node file and saves it as a file or to a stream.</span></span>

## <span data-ttu-id="c515b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c515b-113">EXAMPLES</span></span>

### <span data-ttu-id="c515b-114">Beispiel 1: Herunterladen einer Einer Aufgabe zugeordneten Batchknotendatei und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="c515b-114">Example 1: Get a Batch node file associated with a task and save the file</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="c515b-115">Dieser Befehl ruft die Knotendatei mit dem Namen StdOut.txt ab und speichert sie im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c515b-115">This command gets the node file that is named StdOut.txt, and saves it to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="c515b-116">Die StdOut.txt-Knotendatei ist einer Aufgabe zugeordnet, die die ID Task01 für den Auftrag mit der ID Job01 enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-116">The StdOut.txt node file is associated with task that has the ID Task01 for the job that has the ID Job01.</span></span>
<span data-ttu-id="c515b-117">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c515b-117">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c515b-118">Beispiel 2: Herunterladen einer Batchknotendatei und Speichern in einem angegebenen Dateipfad mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c515b-118">Example 2: Get a Batch node file and save it to a specified file path using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="c515b-119">Mit diesem Befehl wird die Knotendatei mit dem Namen StdErr.txt mithilfe des cmdlets Get-AzBatchNodeFile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c515b-119">This command gets the node file that is named StdErr.txt by using the Get-AzBatchNodeFile cmdlet.</span></span>
<span data-ttu-id="c515b-120">Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c515b-120">The command passes that file to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c515b-121">Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c515b-121">The current cmdlet saves that file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>
<span data-ttu-id="c515b-122">Die StdOut.txt-Knotendatei ist der Aufgabe zugeordnet, die die ID Task02 für den Auftrag mit der ID Job02 enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-122">The StdOut.txt node file is associated with the task that has the ID Task02 for the job that has the ID Job02.</span></span>

### <span data-ttu-id="c515b-123">Beispiel 3: Erhalten einer einer Aufgabe zugeordneten Batchknotendatei und Direktes an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="c515b-123">Example 3: Get a Batch node file associated with a task and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="c515b-124">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream Variablen.</span><span class="sxs-lookup"><span data-stu-id="c515b-124">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="c515b-125">Der zweite Befehl ruft die Knotendatei ab, die StdOut.txt aufgabe mit der ID Task11 für den Auftrag mit der ID Job03 benannt ist.</span><span class="sxs-lookup"><span data-stu-id="c515b-125">The second command gets the node file that is named StdOut.txt from the task that has the ID Task11 for the job that has the ID Job03.</span></span>
<span data-ttu-id="c515b-126">Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.</span><span class="sxs-lookup"><span data-stu-id="c515b-126">The command directs file contents to the stream in $Stream.</span></span>

### <span data-ttu-id="c515b-127">Beispiel 4: Herunterladen einer Knotendatei aus einem Computeknoten und Speichern</span><span class="sxs-lookup"><span data-stu-id="c515b-127">Example 4: Get a node file from a compute node and save it</span></span>
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="c515b-128">Dieser Befehl ruft die Knotendatei Startup\StdOut.txt aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID-Pool01 enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-128">This command gets the node file Startup\StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="c515b-129">Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c515b-129">The command saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="c515b-130">Beispiel 5: Herunterladen einer Knotendatei von einem Computeknoten und Speichern mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c515b-130">Example 5: Get a node file from a compute node and save it by using the pipeline</span></span>
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

<span data-ttu-id="c515b-131">Mit diesem Befehl wird die Knotendatei Startup\StdOut.txt mithilfe Get-AzBatchNodeFile des Computeknotens mit der ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="c515b-131">This command gets the node file Startup\StdOut.txt by using Get-AzBatchNodeFile from the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="c515b-132">Der Computeknoten befindet sich im Pool mit dem ID-Pool01.</span><span class="sxs-lookup"><span data-stu-id="c515b-132">The compute node is in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="c515b-133">Der Befehl übergibt diese Knotendatei an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c515b-133">The command passes that node file to the current cmdlet.</span></span>
<span data-ttu-id="c515b-134">Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="c515b-134">That cmdlet saves the file to the E:\PowerShell\StdOut.txt file path on the local computer.</span></span>

### <span data-ttu-id="c515b-135">Beispiel 6: Herunterladen einer Knotendatei von einem Computeknoten und Direktes an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="c515b-135">Example 6: Get a node file from a compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="c515b-136">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream Variablen.</span><span class="sxs-lookup"><span data-stu-id="c515b-136">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="c515b-137">Der zweite Befehl ruft die Knotendatei mit dem Namen StdOut.txt aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID-Pool01 enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-137">The second command gets the node file that is named StdOut.txt from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool01.</span></span>
<span data-ttu-id="c515b-138">Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.</span><span class="sxs-lookup"><span data-stu-id="c515b-138">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="c515b-139">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c515b-139">PARAMETERS</span></span>

### <span data-ttu-id="c515b-140">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c515b-140">-BatchContext</span></span>
<span data-ttu-id="c515b-141">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c515b-141">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c515b-142">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="c515b-142">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c515b-143">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c515b-143">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c515b-144">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="c515b-144">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c515b-145">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="c515b-145">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c515b-146">-ByteRangeEnd</span><span class="sxs-lookup"><span data-stu-id="c515b-146">-ByteRangeEnd</span></span>
<span data-ttu-id="c515b-147">Das Ende des byte-Bereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c515b-147">The end of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="c515b-148">-ByteRangeStart</span><span class="sxs-lookup"><span data-stu-id="c515b-148">-ByteRangeStart</span></span>
<span data-ttu-id="c515b-149">Der Anfang des byte-Bereichs, der heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c515b-149">The start of the byte range to be downloaded.</span></span>

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

### <span data-ttu-id="c515b-150">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c515b-150">-ComputeNodeId</span></span>
<span data-ttu-id="c515b-151">Gibt die ID des Computeknotens an, der die von diesem Cmdlet zurückgegebene Knotendatei enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-151">Specifies the ID of the compute node that contains the node file that this cmdlet returns.</span></span>

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

### <span data-ttu-id="c515b-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c515b-152">-DefaultProfile</span></span>
<span data-ttu-id="c515b-153">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c515b-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c515b-154">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="c515b-154">-DestinationPath</span></span>
<span data-ttu-id="c515b-155">Gibt den Dateipfad an, in dem dieses Cmdlet die Knotendatei speichert.</span><span class="sxs-lookup"><span data-stu-id="c515b-155">Specifies the file path where this cmdlet saves the node file.</span></span>

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

### <span data-ttu-id="c515b-156">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="c515b-156">-DestinationStream</span></span>
<span data-ttu-id="c515b-157">Gibt den Datenstrom an, in den dieses Cmdlet den Inhalt der Knotendatei schreibt.</span><span class="sxs-lookup"><span data-stu-id="c515b-157">Specifies the stream into which this cmdlet writes the node file contents.</span></span>
<span data-ttu-id="c515b-158">Dieser Datenstrom wird von diesem Cmdlet nicht geschlossen oder zurückspulen.</span><span class="sxs-lookup"><span data-stu-id="c515b-158">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="c515b-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c515b-159">-InputObject</span></span>
<span data-ttu-id="c515b-160">Gibt die Datei an, die dieses Cmdlet als **PSNodeFile-Objekt erhält.**</span><span class="sxs-lookup"><span data-stu-id="c515b-160">Specifies the file that this cmdlet gets, as a **PSNodeFile** object.</span></span>
<span data-ttu-id="c515b-161">Zum Abrufen eines Knotendateiobjekts verwenden Sie das Get-AzBatchNodeFile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c515b-161">To obtain a node file object, use the Get-AzBatchNodeFile cmdlet.</span></span>

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

### <span data-ttu-id="c515b-162">-JobId</span><span class="sxs-lookup"><span data-stu-id="c515b-162">-JobId</span></span>
<span data-ttu-id="c515b-163">Gibt die ID des Auftrags an, der die Zielaufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="c515b-163">Specifies the ID of the job that contains the target task.</span></span>

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

### <span data-ttu-id="c515b-164">-Path</span><span class="sxs-lookup"><span data-stu-id="c515b-164">-Path</span></span>
<span data-ttu-id="c515b-165">Der Pfad der Knotendatei, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c515b-165">The path of the node file to download.</span></span>

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

### <span data-ttu-id="c515b-166">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c515b-166">-PoolId</span></span>
<span data-ttu-id="c515b-167">Gibt die ID des Pools an, der den Computeknoten enthält, der die Knotendatei enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c515b-167">Specifies the ID of the pool that contains the compute node that contains the node file that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c515b-168">-TaskId</span><span class="sxs-lookup"><span data-stu-id="c515b-168">-TaskId</span></span>
<span data-ttu-id="c515b-169">Gibt die ID der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="c515b-169">Specifies the ID of the task.</span></span>

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

### <span data-ttu-id="c515b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c515b-170">CommonParameters</span></span>
<span data-ttu-id="c515b-171">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c515b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c515b-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c515b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c515b-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c515b-173">INPUTS</span></span>

### <span data-ttu-id="c515b-174">System.String</span><span class="sxs-lookup"><span data-stu-id="c515b-174">System.String</span></span>

### <span data-ttu-id="c515b-175">Microsoft.Azure.Commands.Batch. Models.PSNodeFile</span><span class="sxs-lookup"><span data-stu-id="c515b-175">Microsoft.Azure.Commands.Batch.Models.PSNodeFile</span></span>

### <span data-ttu-id="c515b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c515b-176">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c515b-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c515b-177">OUTPUTS</span></span>

### <span data-ttu-id="c515b-178">System.Void</span><span class="sxs-lookup"><span data-stu-id="c515b-178">System.Void</span></span>

## <span data-ttu-id="c515b-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c515b-179">NOTES</span></span>

## <span data-ttu-id="c515b-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c515b-180">RELATED LINKS</span></span>

[<span data-ttu-id="c515b-181">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c515b-181">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c515b-182">Get-AzBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="c515b-182">Get-AzBatchNodeFile</span></span>](./Get-AzBatchNodeFile.md)

[<span data-ttu-id="c515b-183">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c515b-183">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
