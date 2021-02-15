---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164332"
---
# <span data-ttu-id="1d1a6-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="1d1a6-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="1d1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1a6-103">Ruft eine RDP-Datei aus einem Rechenknoten ab.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="1d1a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d1a6-104">SYNTAX</span></span>

### <span data-ttu-id="1d1a6-105">Id_Path (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d1a6-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d1a6-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="1d1a6-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d1a6-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="1d1a6-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d1a6-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="1d1a6-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d1a6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d1a6-109">DESCRIPTION</span></span>
<span data-ttu-id="1d1a6-110">Das **Cmdlet "Get-AzBatchRemoteDesktopProtocolFile"** ruft eine Remotedesktopprotokolldatei (Remote Desktop Protocol, RDP) aus einem Rechenknoten ab und speichert sie als Datei oder in einem vom Benutzer bereitgestellten Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="1d1a6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d1a6-111">EXAMPLES</span></span>

### <span data-ttu-id="1d1a6-112">Beispiel 1: Herunterladen einer RDP-Datei von einem angegebenen Rechenknoten und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="1d1a6-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="1d1a6-113">Dieser Befehl ruft eine RDP-Datei aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID Pool06 enthält.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="1d1a6-114">Der Befehl speichert die #A0 als "C:\PowerShell\MyComputeNode.rdp".</span><span class="sxs-lookup"><span data-stu-id="1d1a6-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="1d1a6-115">Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="1d1a6-116">Beispiel 2: Get an RDP file from a compute node and save the file by using the pipeline</span><span class="sxs-lookup"><span data-stu-id="1d1a6-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="1d1a6-117">Dieser Befehl ruft den Rechenknoten ab, der die ID ComputeNode02 im Pool mit dem ID Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="1d1a6-118">Der Befehl übergibt diesen Rechenknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d1a6-119">Das aktuelle Cmdlet ruft eine #A0 vom Computeknoten ab und speichert den Inhalt dann als Datei mit dem Namen "C:\PowerShell\MyComputeNode02.rdp".</span><span class="sxs-lookup"><span data-stu-id="1d1a6-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="1d1a6-120">Beispiel 3: Herunterladen einer RDP-Datei von einem angegebenen Rechenknoten und Direktes an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="1d1a6-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="1d1a6-121">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in $Stream Variable.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="1d1a6-122">Der zweite Befehl ruft eine "RDP"-Datei aus dem Computeknoten ab, der die ID ComputeNode03 im Pool mit dem ID Pool06 enthält.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="1d1a6-123">Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="1d1a6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d1a6-124">PARAMETERS</span></span>

### <span data-ttu-id="1d1a6-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1d1a6-125">-BatchContext</span></span>
<span data-ttu-id="1d1a6-126">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1d1a6-127">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1d1a6-128">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1d1a6-129">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1d1a6-130">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1d1a6-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="1d1a6-131">-ComputeNode</span></span>
<span data-ttu-id="1d1a6-132">Gibt einen Rechenknoten als ein **PSComputeNode-Objekt** an, auf den die .rdp-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="1d1a6-133">Verwenden Sie zum Abrufen eines Rechenknotenobjekts das Get-AzBatchComputeNode Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="1d1a6-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="1d1a6-134">-ComputeNodeId</span></span>
<span data-ttu-id="1d1a6-135">Gibt die ID des Rechenknotens an, auf den die .rdp-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="1d1a6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1a6-136">-DefaultProfile</span></span>
<span data-ttu-id="1d1a6-137">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d1a6-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="1d1a6-138">-DestinationPath</span></span>
<span data-ttu-id="1d1a6-139">Gibt den Dateipfad an, unter dem die RDP-Datei von diesem Cmdlet gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="1d1a6-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="1d1a6-140">-DestinationStream</span></span>
<span data-ttu-id="1d1a6-141">Gibt den Datenstrom an, in den dieses Cmdlet die RDP-Daten leitet.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="1d1a6-142">Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückspulen.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="1d1a6-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="1d1a6-143">-PoolId</span></span>
<span data-ttu-id="1d1a6-144">Gibt die ID des Pools an, der den Rechenknoten enthält, von dem dieses Cmdlet eine RDP-Datei erhält.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="1d1a6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1a6-145">CommonParameters</span></span>
<span data-ttu-id="1d1a6-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d1a6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1a6-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d1a6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1a6-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d1a6-148">INPUTS</span></span>

### <span data-ttu-id="1d1a6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1d1a6-149">System.String</span></span>

### <span data-ttu-id="1d1a6-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="1d1a6-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="1d1a6-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1d1a6-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1d1a6-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d1a6-152">OUTPUTS</span></span>

### <span data-ttu-id="1d1a6-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="1d1a6-153">System.Void</span></span>

## <span data-ttu-id="1d1a6-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d1a6-154">NOTES</span></span>

## <span data-ttu-id="1d1a6-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d1a6-155">RELATED LINKS</span></span>

[<span data-ttu-id="1d1a6-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d1a6-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1d1a6-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="1d1a6-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="1d1a6-158">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1d1a6-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
