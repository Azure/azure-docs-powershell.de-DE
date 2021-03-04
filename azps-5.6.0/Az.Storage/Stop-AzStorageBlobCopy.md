---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922648"
---
# <span data-ttu-id="7631c-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7631c-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="7631c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7631c-102">SYNOPSIS</span></span>
<span data-ttu-id="7631c-103">Beendet einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="7631c-103">Stops a copy operation.</span></span>

## <span data-ttu-id="7631c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7631c-104">SYNTAX</span></span>

### <span data-ttu-id="7631c-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="7631c-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7631c-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="7631c-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7631c-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="7631c-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7631c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7631c-108">DESCRIPTION</span></span>
<span data-ttu-id="7631c-109">Das **Cmdlet Stop-AzStorageBlobCopy** beendet einen Kopiervorgang in das angegebene Zielblob.</span><span class="sxs-lookup"><span data-stu-id="7631c-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="7631c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7631c-110">EXAMPLES</span></span>

### <span data-ttu-id="7631c-111">Beispiel 1: Beenden des Kopiervorgangs nach Name</span><span class="sxs-lookup"><span data-stu-id="7631c-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="7631c-112">Mit diesem Befehl wird der Kopiervorgang nach Name beendet.</span><span class="sxs-lookup"><span data-stu-id="7631c-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="7631c-113">Beispiel 2: Beenden des Kopiervorgangs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="7631c-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="7631c-114">Mit diesem Befehl wird der Kopiervorgang beendet, indem der Container in der Pipeline von **Get-AzStorageContainer übergeben wird.**</span><span class="sxs-lookup"><span data-stu-id="7631c-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="7631c-115">Beispiel 3: Beenden des Kopiervorgangs mithilfe der Pipeline und Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7631c-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="7631c-116">In diesem Beispiel wird der Kopiervorgang beendet, indem der Container in der Pipeline aus dem Get-AzStorageBlob übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7631c-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="7631c-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7631c-117">PARAMETERS</span></span>

### <span data-ttu-id="7631c-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="7631c-118">-Blob</span></span>
<span data-ttu-id="7631c-119">Gibt den Namen des Blobs an.</span><span class="sxs-lookup"><span data-stu-id="7631c-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7631c-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7631c-121">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="7631c-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7631c-122">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7631c-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7631c-123">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7631c-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7631c-124">-CloudBlob</span></span>
<span data-ttu-id="7631c-125">Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="7631c-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="7631c-126">Um ein **CloudBlob-Objekt zu** erhalten, verwenden Sie das Get-AzStorageBlob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7631c-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7631c-127">-CloudBlobContainer</span></span>
<span data-ttu-id="7631c-128">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="7631c-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="7631c-129">Sie können das -Objekt erstellen oder das cmdlet Get-AzStorageContainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="7631c-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7631c-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7631c-131">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="7631c-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7631c-132">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="7631c-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7631c-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="7631c-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7631c-134">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="7631c-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7631c-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="7631c-135">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-136">-Container</span><span class="sxs-lookup"><span data-stu-id="7631c-136">-Container</span></span>
<span data-ttu-id="7631c-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="7631c-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-138">-Context</span><span class="sxs-lookup"><span data-stu-id="7631c-138">-Context</span></span>
<span data-ttu-id="7631c-139">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7631c-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7631c-140">Sie können den Kontext mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="7631c-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="7631c-141">-CopyId</span></span>
<span data-ttu-id="7631c-142">Gibt die Kopier-ID an.</span><span class="sxs-lookup"><span data-stu-id="7631c-142">Specifies the copy ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7631c-143">-DefaultProfile</span></span>
<span data-ttu-id="7631c-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7631c-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-145">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7631c-145">-Force</span></span>
<span data-ttu-id="7631c-146">Beendet die aktuelle Kopieraufgabe für den angegebenen Blob, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="7631c-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7631c-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7631c-148">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="7631c-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7631c-149">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7631c-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7631c-150">-Confirm</span></span>
<span data-ttu-id="7631c-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7631c-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7631c-152">-WhatIf</span></span>
<span data-ttu-id="7631c-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7631c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7631c-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7631c-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7631c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7631c-155">CommonParameters</span></span>
<span data-ttu-id="7631c-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7631c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7631c-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7631c-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7631c-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7631c-158">INPUTS</span></span>

### <span data-ttu-id="7631c-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7631c-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="7631c-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7631c-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="7631c-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7631c-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7631c-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7631c-162">OUTPUTS</span></span>

### <span data-ttu-id="7631c-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7631c-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="7631c-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7631c-164">NOTES</span></span>

## <span data-ttu-id="7631c-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7631c-165">RELATED LINKS</span></span>

[<span data-ttu-id="7631c-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7631c-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="7631c-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7631c-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="7631c-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7631c-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="7631c-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="7631c-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
