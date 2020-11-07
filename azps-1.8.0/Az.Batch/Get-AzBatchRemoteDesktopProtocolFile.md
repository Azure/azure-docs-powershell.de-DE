---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 491deaff0b609ce20de60299de71686ee2ece2a3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662079"
---
# <span data-ttu-id="a4fec-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="a4fec-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="a4fec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4fec-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fec-103">Ruft eine RDP-Datei von einem Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="a4fec-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="a4fec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4fec-104">SYNTAX</span></span>

### <span data-ttu-id="a4fec-105">Id_Path (Standard)</span><span class="sxs-lookup"><span data-stu-id="a4fec-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fec-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="a4fec-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fec-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="a4fec-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4fec-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="a4fec-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4fec-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4fec-109">DESCRIPTION</span></span>
<span data-ttu-id="a4fec-110">Das Cmdlet " **Get-AzBatchRemoteDesktopProtocolFile** " Ruft eine RDP-Datei (Remote Desktop Protocol) von einem Compute-Knoten ab und speichert Sie als Datei oder für einen vom Benutzer angegebenen Stream.</span><span class="sxs-lookup"><span data-stu-id="a4fec-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="a4fec-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4fec-111">EXAMPLES</span></span>

### <span data-ttu-id="a4fec-112">Beispiel 1: Abrufen einer RDP-Datei von einem angegebenen Compute-Knoten und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="a4fec-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="a4fec-113">Dieser Befehl ruft eine RDP-Datei vom Compute-Knoten ab, die die ID-ComputeNode01 im Pool mit der ID Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="a4fec-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a4fec-114">Der Befehl speichert die RDP-Datei als C:\PowerShell\MyComputeNode.RDP.</span><span class="sxs-lookup"><span data-stu-id="a4fec-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="a4fec-115">Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a4fec-115">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="a4fec-116">Beispiel 2: Abrufen einer RDP-Datei von einem Compute-Knoten und Speichern der Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a4fec-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="a4fec-117">Dieser Befehl ruft den Compute-Knoten ab, dessen ID-ComputeNode02 im Pool mit der ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="a4fec-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a4fec-118">Der Befehl übergibt diesen Compute-Knoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4fec-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a4fec-119">Das aktuelle Cmdlet ruft eine RPD-Datei vom Compute-Knoten ab und speichert dann den Inhalt als Datei mit dem Namen C:\PowerShell\MyComputeNode02.RDP.</span><span class="sxs-lookup"><span data-stu-id="a4fec-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="a4fec-120">Beispiel 3: Abrufen einer RDP-Datei aus einem angegebenen Compute-Knoten und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="a4fec-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="a4fec-121">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a4fec-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="a4fec-122">Der zweite Befehl ruft eine RDP-Datei vom Compute-Knoten ab, die die ID-ComputeNode03 im Pool mit der ID Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="a4fec-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="a4fec-123">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="a4fec-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="a4fec-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4fec-124">PARAMETERS</span></span>

### <span data-ttu-id="a4fec-125">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a4fec-125">-BatchContext</span></span>
<span data-ttu-id="a4fec-126">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4fec-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a4fec-127">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4fec-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a4fec-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4fec-128">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a4fec-129">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4fec-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a4fec-130">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="a4fec-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a4fec-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4fec-131">-ComputeNode</span></span>
<span data-ttu-id="a4fec-132">Gibt einen Compute-Knoten als **PSComputeNode** -Objekt an, auf das die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="a4fec-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="a4fec-133">Verwenden Sie das Get-AzBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4fec-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fec-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a4fec-134">-ComputeNodeId</span></span>
<span data-ttu-id="a4fec-135">Gibt die ID des Compute-Knotens an, auf den die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="a4fec-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fec-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fec-136">-DefaultProfile</span></span>
<span data-ttu-id="a4fec-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4fec-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4fec-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="a4fec-138">-DestinationPath</span></span>
<span data-ttu-id="a4fec-139">Gibt den Dateipfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="a4fec-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fec-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="a4fec-140">-DestinationStream</span></span>
<span data-ttu-id="a4fec-141">Gibt den Stream an, in den das Cmdlet die RDP-Daten leitet.</span><span class="sxs-lookup"><span data-stu-id="a4fec-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="a4fec-142">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.</span><span class="sxs-lookup"><span data-stu-id="a4fec-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fec-143">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="a4fec-143">-PoolId</span></span>
<span data-ttu-id="a4fec-144">Gibt die ID des Pools an, der den Compute-Knoten enthält, aus dem dieses Cmdlet eine RDP-Datei erhält.</span><span class="sxs-lookup"><span data-stu-id="a4fec-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4fec-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fec-145">CommonParameters</span></span>
<span data-ttu-id="a4fec-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4fec-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fec-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fec-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fec-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4fec-148">INPUTS</span></span>

### <span data-ttu-id="a4fec-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a4fec-149">System.String</span></span>

### <span data-ttu-id="a4fec-150">Microsoft.Azure.Commands.Batch. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4fec-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a4fec-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a4fec-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a4fec-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4fec-152">OUTPUTS</span></span>

### <span data-ttu-id="a4fec-153">System. void</span><span class="sxs-lookup"><span data-stu-id="a4fec-153">System.Void</span></span>

## <span data-ttu-id="a4fec-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4fec-154">NOTES</span></span>

## <span data-ttu-id="a4fec-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4fec-155">RELATED LINKS</span></span>

[<span data-ttu-id="a4fec-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a4fec-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a4fec-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a4fec-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a4fec-158">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a4fec-158">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


