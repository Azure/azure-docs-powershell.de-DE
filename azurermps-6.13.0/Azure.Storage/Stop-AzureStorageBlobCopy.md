---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
ms.openlocfilehash: 67a6a9d706b8865ebca4290649a30bc8e9817569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663401"
---
# <span data-ttu-id="b856c-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b856c-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="b856c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b856c-102">SYNOPSIS</span></span>
<span data-ttu-id="b856c-103">Beendet einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="b856c-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b856c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b856c-104">SYNTAX</span></span>

### <span data-ttu-id="b856c-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="b856c-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b856c-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b856c-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b856c-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b856c-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b856c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b856c-108">DESCRIPTION</span></span>
<span data-ttu-id="b856c-109">Das Cmdlet **Stop-AzureStorageBlobCopy** beendet einen Kopiervorgang auf das angegebene Ziel-BLOB.</span><span class="sxs-lookup"><span data-stu-id="b856c-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="b856c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b856c-110">EXAMPLES</span></span>

### <span data-ttu-id="b856c-111">Beispiel 1: Beenden des Kopiervorgangs nach Name</span><span class="sxs-lookup"><span data-stu-id="b856c-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="b856c-112">Mit diesem Befehl wird der Kopiervorgang nach Namen angehalten.</span><span class="sxs-lookup"><span data-stu-id="b856c-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="b856c-113">Beispiel 2: Beenden des Kopiervorgangs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b856c-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="b856c-114">Mit diesem Befehl wird der Kopiervorgang beendet, indem der Container in der Pipeline von **Get-AzureStorageContainer** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b856c-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="b856c-115">Beispiel 3: Beenden des Kopiervorgangs mithilfe der Pipeline und Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b856c-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="b856c-116">In diesem Beispiel wird der Kopiervorgang beendet, indem der Container in der Pipeline vom Get-AzureStorageBlob-Cmdlet übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b856c-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="b856c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b856c-117">PARAMETERS</span></span>

### <span data-ttu-id="b856c-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="b856c-118">-Blob</span></span>
<span data-ttu-id="b856c-119">Gibt den Namen des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="b856c-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="b856c-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b856c-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b856c-121">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b856c-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b856c-122">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="b856c-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b856c-123">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b856c-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b856c-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b856c-124">-CloudBlob</span></span>
<span data-ttu-id="b856c-125">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="b856c-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="b856c-126">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b856c-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b856c-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b856c-127">-CloudBlobContainer</span></span>
<span data-ttu-id="b856c-128">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="b856c-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b856c-129">Sie können das Objekt erstellen oder das Get-AzureStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="b856c-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b856c-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b856c-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b856c-131">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="b856c-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b856c-132">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="b856c-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b856c-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b856c-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b856c-134">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="b856c-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b856c-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b856c-135">The default value is 10.</span></span>

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

### <span data-ttu-id="b856c-136">-Container</span><span class="sxs-lookup"><span data-stu-id="b856c-136">-Container</span></span>
<span data-ttu-id="b856c-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="b856c-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b856c-138">-Context</span><span class="sxs-lookup"><span data-stu-id="b856c-138">-Context</span></span>
<span data-ttu-id="b856c-139">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b856c-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b856c-140">Sie können den Kontext mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="b856c-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b856c-141">-Kopier-Nr</span><span class="sxs-lookup"><span data-stu-id="b856c-141">-CopyId</span></span>
<span data-ttu-id="b856c-142">Gibt die Kopier-ID an.</span><span class="sxs-lookup"><span data-stu-id="b856c-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="b856c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b856c-143">-DefaultProfile</span></span>
<span data-ttu-id="b856c-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b856c-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b856c-145">-Force</span><span class="sxs-lookup"><span data-stu-id="b856c-145">-Force</span></span>
<span data-ttu-id="b856c-146">Beendet die aktuelle Kopier Aufgabe auf dem angegebenen BLOB, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="b856c-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b856c-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b856c-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b856c-148">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b856c-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b856c-149">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b856c-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b856c-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b856c-150">-Confirm</span></span>
<span data-ttu-id="b856c-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b856c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b856c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b856c-152">-WhatIf</span></span>
<span data-ttu-id="b856c-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b856c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b856c-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b856c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b856c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b856c-155">CommonParameters</span></span>
<span data-ttu-id="b856c-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b856c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b856c-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b856c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b856c-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b856c-158">INPUTS</span></span>

### <span data-ttu-id="b856c-159">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b856c-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b856c-160">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b856c-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b856c-161">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b856c-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b856c-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b856c-162">OUTPUTS</span></span>

### <span data-ttu-id="b856c-163">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b856c-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b856c-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="b856c-164">NOTES</span></span>

## <span data-ttu-id="b856c-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b856c-165">RELATED LINKS</span></span>

[<span data-ttu-id="b856c-166">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b856c-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b856c-167">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b856c-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="b856c-168">Anfang-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="b856c-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="b856c-169">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="b856c-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
