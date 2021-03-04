---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 21e1848266f13fd44513ea0bce8c540b0387320a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935368"
---
# <span data-ttu-id="96030-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="96030-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="96030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96030-102">SYNOPSIS</span></span>
<span data-ttu-id="96030-103">Ruft eine RDP-Datei aus einem Computeknoten ab.</span><span class="sxs-lookup"><span data-stu-id="96030-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="96030-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96030-104">SYNTAX</span></span>

### <span data-ttu-id="96030-105">Id_Path (Standard)</span><span class="sxs-lookup"><span data-stu-id="96030-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96030-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="96030-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96030-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="96030-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96030-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="96030-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96030-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96030-109">DESCRIPTION</span></span>
<span data-ttu-id="96030-110">Das **Get-AzBatchRemoteDesktopProtocolFile-Cmdlet** ruft eine RDP-Datei (Remote Desktop Protocol) von einem Computeknoten ab und speichert sie als Datei oder in einem vom Benutzer bereitgestellten Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="96030-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="96030-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="96030-111">EXAMPLES</span></span>

### <span data-ttu-id="96030-112">Beispiel 1: Herunterladen einer RDP-Datei von einem angegebenen Computeknoten und Speichern der Datei</span><span class="sxs-lookup"><span data-stu-id="96030-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="96030-113">Dieser Befehl ruft eine RDP-Datei aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID-Pool06 enthält.</span><span class="sxs-lookup"><span data-stu-id="96030-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="96030-114">Der Befehl speichert die #A0 als C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="96030-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="96030-115">Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um der Variablen $Context Kontext zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="96030-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="96030-116">Beispiel 2: Herunterladen einer RDP-Datei von einem Computeknoten und Speichern der Datei mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="96030-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="96030-117">Dieser Befehl ruft den Computeknoten ab, der die ID ComputeNode02 im Pool mit dem ID-Pool06 hat.</span><span class="sxs-lookup"><span data-stu-id="96030-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="96030-118">Der Befehl übergibt diesen Computeknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96030-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="96030-119">Das aktuelle Cmdlet ruft eine #A0 vom Computeknoten ab und speichert den Inhalt dann als Datei mit dem Namen C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="96030-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="96030-120">Beispiel 3: Herunterladen einer RDP-Datei von einem angegebenen Computeknoten und Direktes an einen Datenstrom</span><span class="sxs-lookup"><span data-stu-id="96030-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="96030-121">Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream Variablen.</span><span class="sxs-lookup"><span data-stu-id="96030-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="96030-122">Der zweite Befehl ruft eine RDP-Datei vom Computeknoten ab, der die ID ComputeNode03 im Pool mit dem ID-Pool06 enthält.</span><span class="sxs-lookup"><span data-stu-id="96030-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="96030-123">Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.</span><span class="sxs-lookup"><span data-stu-id="96030-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="96030-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="96030-124">PARAMETERS</span></span>

### <span data-ttu-id="96030-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="96030-125">-BatchContext</span></span>
<span data-ttu-id="96030-126">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96030-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="96030-127">Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="96030-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="96030-128">Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="96030-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="96030-129">Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="96030-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="96030-130">Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="96030-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="96030-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="96030-131">-ComputeNode</span></span>
<span data-ttu-id="96030-132">Gibt einen Computeknoten als **PSComputeNode-Objekt** an, auf den die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="96030-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="96030-133">Verwenden Sie zum Abrufen eines Computeknotenobjekts das Get-AzBatchComputeNode Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96030-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="96030-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="96030-134">-ComputeNodeId</span></span>
<span data-ttu-id="96030-135">Gibt die ID des Computeknotens an, auf den die RDP-Datei verweist.</span><span class="sxs-lookup"><span data-stu-id="96030-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="96030-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96030-136">-DefaultProfile</span></span>
<span data-ttu-id="96030-137">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96030-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96030-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="96030-138">-DestinationPath</span></span>
<span data-ttu-id="96030-139">Gibt den Dateipfad an, in dem dieses Cmdlet die RDP-Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="96030-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="96030-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="96030-140">-DestinationStream</span></span>
<span data-ttu-id="96030-141">Gibt den Datenstrom an, in den dieses Cmdlet die RDP-Daten leitet.</span><span class="sxs-lookup"><span data-stu-id="96030-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="96030-142">Dieser Datenstrom wird von diesem Cmdlet nicht geschlossen oder zurückspulen.</span><span class="sxs-lookup"><span data-stu-id="96030-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="96030-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="96030-143">-PoolId</span></span>
<span data-ttu-id="96030-144">Gibt die ID des Pools an, der den Computeknoten enthält, von dem dieses Cmdlet eine RDP-Datei erhält.</span><span class="sxs-lookup"><span data-stu-id="96030-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="96030-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96030-145">CommonParameters</span></span>
<span data-ttu-id="96030-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96030-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96030-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96030-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96030-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="96030-148">INPUTS</span></span>

### <span data-ttu-id="96030-149">System.String</span><span class="sxs-lookup"><span data-stu-id="96030-149">System.String</span></span>

### <span data-ttu-id="96030-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="96030-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="96030-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="96030-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="96030-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="96030-152">OUTPUTS</span></span>

### <span data-ttu-id="96030-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="96030-153">System.Void</span></span>

## <span data-ttu-id="96030-154">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="96030-154">NOTES</span></span>

## <span data-ttu-id="96030-155">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="96030-155">RELATED LINKS</span></span>

[<span data-ttu-id="96030-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="96030-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="96030-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="96030-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="96030-158">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="96030-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
