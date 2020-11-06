---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 2a147e00dba480a483b10843b17347145a1dc2a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478753"
---
# <span data-ttu-id="bfb4f-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="bfb4f-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="bfb4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="bfb4f-103">Ruft eine RDP-Datei von einem Compute-Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfb4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfb4f-104">SYNTAX</span></span>

### <span data-ttu-id="bfb4f-105">Id_Path (Standard)</span><span class="sxs-lookup"><span data-stu-id="bfb4f-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfb4f-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="bfb4f-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfb4f-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="bfb4f-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfb4f-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="bfb4f-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfb4f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfb4f-109">DESCRIPTION</span></span>
<span data-ttu-id="bfb4f-110">Das Cmdlet " **Get-AzureBatchRemoteDesktopProtocolFile** " Ruft eine RDP-Datei (Remote Desktop Protocol) von einem Compute-Knoten ab und speichert Sie als Datei oder für einen vom Benutzer angegebenen Stream.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="bfb4f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfb4f-111">EXAMPLES</span></span>

### <span data-ttu-id="bfb4f-112">Beispiel 1: Abrufen einer RDP-Datei von einem angegebenen Compute-Knoten und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="bfb4f-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="bfb4f-113">Dieser Befehl ruft eine RDP-Datei vom Compute-Knoten ab, die die ID-ComputeNode01 im Pool mit der ID Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="bfb4f-114">Der Befehl speichert die RDP-Datei als C:\PowerShell\MyComputeNode.RDP.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="bfb4f-115">Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="bfb4f-116">Beispiel 2: Abrufen einer RDP-Datei von einem Compute-Knoten und Speichern der Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="bfb4f-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="bfb4f-117">Dieser Befehl ruft den Compute-Knoten ab, dessen ID-ComputeNode02 im Pool mit der ID-Pool06.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="bfb4f-118">Der Befehl übergibt diesen Compute-Knoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bfb4f-119">Das aktuelle Cmdlet ruft eine RPD-Datei vom Compute-Knoten ab und speichert dann den Inhalt als Datei mit dem Namen C:\PowerShell\MyComputeNode02.RDP.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="bfb4f-120">Beispiel 3: Abrufen einer RDP-Datei aus einem angegebenen Compute-Knoten und Weiterleiten an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="bfb4f-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="bfb4f-121">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="bfb4f-122">Der zweite Befehl ruft eine RDP-Datei vom Compute-Knoten ab, die die ID-ComputeNode03 im Pool mit der ID Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="bfb4f-123">Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="bfb4f-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfb4f-124">PARAMETERS</span></span>

### <span data-ttu-id="bfb4f-125">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="bfb4f-125">-BatchContext</span></span>
<span data-ttu-id="bfb4f-126">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bfb4f-127">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bfb4f-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bfb4f-129">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bfb4f-130">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bfb4f-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="bfb4f-131">-ComputeNode</span></span>
<span data-ttu-id="bfb4f-132">Gibt einen Compute-Knoten als **PSComputeNode** -Objekt an, auf das die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="bfb4f-133">Verwenden Sie das Get-AzureBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb4f-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="bfb4f-134">-ComputeNodeId</span></span>
<span data-ttu-id="bfb4f-135">Gibt die ID des Compute-Knotens an, auf den die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb4f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfb4f-136">-DefaultProfile</span></span>
<span data-ttu-id="bfb4f-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfb4f-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="bfb4f-138">-DestinationPath</span></span>
<span data-ttu-id="bfb4f-139">Gibt den Dateipfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb4f-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="bfb4f-140">-DestinationStream</span></span>
<span data-ttu-id="bfb4f-141">Gibt den Stream an, in den das Cmdlet die RDP-Daten leitet.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="bfb4f-142">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfb4f-143">-Pool-Nr</span><span class="sxs-lookup"><span data-stu-id="bfb4f-143">-PoolId</span></span>
<span data-ttu-id="bfb4f-144">Gibt die ID des Pools an, der den Compute-Knoten enthält, aus dem dieses Cmdlet eine RDP-Datei erhält.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Id_Path, Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfb4f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfb4f-145">CommonParameters</span></span>
<span data-ttu-id="bfb4f-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfb4f-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfb4f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfb4f-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfb4f-148">INPUTS</span></span>

### <span data-ttu-id="bfb4f-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bfb4f-149">BatchAccountContext</span></span>
<span data-ttu-id="bfb4f-150">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bfb4f-151">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="bfb4f-151">PSComputeNode</span></span>
<span data-ttu-id="bfb4f-152">Der Parameter "ComputeNode" akzeptiert den Wert vom Typ "PSComputeNode" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bfb4f-152">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="bfb4f-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfb4f-153">OUTPUTS</span></span>

## <span data-ttu-id="bfb4f-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfb4f-154">NOTES</span></span>

## <span data-ttu-id="bfb4f-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfb4f-155">RELATED LINKS</span></span>

[<span data-ttu-id="bfb4f-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bfb4f-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bfb4f-157">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="bfb4f-157">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="bfb4f-158">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bfb4f-158">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


