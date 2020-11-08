---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996203"
---
# <span data-ttu-id="e1ec9-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e1ec9-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="e1ec9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ec9-103">Beendet einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-103">Stops a copy operation.</span></span>

## <span data-ttu-id="e1ec9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ec9-104">SYNTAX</span></span>

### <span data-ttu-id="e1ec9-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1ec9-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ec9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="e1ec9-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ec9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="e1ec9-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ec9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="e1ec9-109">Das Cmdlet **Stop-AzStorageBlobCopy** beendet einen Kopiervorgang auf das angegebene Ziel-BLOB.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="e1ec9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="e1ec9-111">Beispiel 1: Beenden des Kopiervorgangs nach Name</span><span class="sxs-lookup"><span data-stu-id="e1ec9-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="e1ec9-112">Mit diesem Befehl wird der Kopiervorgang nach Namen angehalten.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="e1ec9-113">Beispiel 2: Beenden des Kopiervorgangs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ec9-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="e1ec9-114">Mit diesem Befehl wird der Kopiervorgang beendet, indem der Container in der Pipeline von **Get-AzStorageContainer** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="e1ec9-115">Beispiel 3: Beenden des Kopiervorgangs mithilfe der Pipeline und Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e1ec9-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="e1ec9-116">In diesem Beispiel wird der Kopiervorgang beendet, indem der Container in der Pipeline vom Get-AzStorageBlob-Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="e1ec9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ec9-117">PARAMETERS</span></span>

### <span data-ttu-id="e1ec9-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="e1ec9-118">-Blob</span></span>
<span data-ttu-id="e1ec9-119">Gibt den Namen des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="e1ec9-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ec9-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1ec9-121">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1ec9-122">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1ec9-123">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e1ec9-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e1ec9-124">-CloudBlob</span></span>
<span data-ttu-id="e1ec9-125">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="e1ec9-126">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="e1ec9-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e1ec9-127">-CloudBlobContainer</span></span>
<span data-ttu-id="e1ec9-128">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="e1ec9-129">Sie können das Objekt erstellen oder das Get-AzStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="e1ec9-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1ec9-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1ec9-131">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1ec9-132">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1ec9-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1ec9-134">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1ec9-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-135">The default value is 10.</span></span>

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

### <span data-ttu-id="e1ec9-136">-Container</span><span class="sxs-lookup"><span data-stu-id="e1ec9-136">-Container</span></span>
<span data-ttu-id="e1ec9-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="e1ec9-138">-Context</span><span class="sxs-lookup"><span data-stu-id="e1ec9-138">-Context</span></span>
<span data-ttu-id="e1ec9-139">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e1ec9-140">Sie können den Kontext mithilfe des New-AzStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e1ec9-141">-Kopier-Nr</span><span class="sxs-lookup"><span data-stu-id="e1ec9-141">-CopyId</span></span>
<span data-ttu-id="e1ec9-142">Gibt die Kopier-ID an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="e1ec9-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ec9-143">-DefaultProfile</span></span>
<span data-ttu-id="e1ec9-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ec9-145">-Force</span><span class="sxs-lookup"><span data-stu-id="e1ec9-145">-Force</span></span>
<span data-ttu-id="e1ec9-146">Beendet die aktuelle Kopier Aufgabe auf dem angegebenen BLOB, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e1ec9-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1ec9-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1ec9-148">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="e1ec9-149">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e1ec9-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1ec9-150">-Confirm</span></span>
<span data-ttu-id="e1ec9-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ec9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ec9-152">-WhatIf</span></span>
<span data-ttu-id="e1ec9-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ec9-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ec9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ec9-155">CommonParameters</span></span>
<span data-ttu-id="e1ec9-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ec9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ec9-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ec9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ec9-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1ec9-158">INPUTS</span></span>

### <span data-ttu-id="e1ec9-159">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="e1ec9-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="e1ec9-160">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="e1ec9-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="e1ec9-161">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1ec9-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1ec9-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1ec9-162">OUTPUTS</span></span>

### <span data-ttu-id="e1ec9-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e1ec9-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="e1ec9-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1ec9-164">NOTES</span></span>

## <span data-ttu-id="e1ec9-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1ec9-165">RELATED LINKS</span></span>

[<span data-ttu-id="e1ec9-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="e1ec9-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="e1ec9-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e1ec9-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="e1ec9-168">Anfang-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e1ec9-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="e1ec9-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="e1ec9-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
