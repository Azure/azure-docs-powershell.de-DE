---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 9eb7337ee39ed0e9c4d179a6a89401398a0d80f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501013"
---
# <span data-ttu-id="abcd7-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abcd7-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="abcd7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abcd7-102">SYNOPSIS</span></span>
<span data-ttu-id="abcd7-103">Lädt ein Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="abcd7-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abcd7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abcd7-104">SYNTAX</span></span>

### <span data-ttu-id="abcd7-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="abcd7-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abcd7-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="abcd7-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abcd7-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="abcd7-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abcd7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abcd7-108">DESCRIPTION</span></span>
<span data-ttu-id="abcd7-109">Das Cmdlet " **Get-AzureStorageBlobContent** " lädt das angegebene Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="abcd7-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="abcd7-110">Wenn der BLOB-Name für den lokalen Computer nicht gültig ist, wird er von diesem Cmdlet automatisch aufgelöst, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="abcd7-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="abcd7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abcd7-111">EXAMPLES</span></span>

### <span data-ttu-id="abcd7-112">Beispiel 1: Herunterladen von BLOB-Inhalten nach Name</span><span class="sxs-lookup"><span data-stu-id="abcd7-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="abcd7-113">Mit diesem Befehl wird ein BLOB nach Name heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="abcd7-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="abcd7-114">Beispiel 2: Herunterladen von BLOB-Inhalten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="abcd7-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="abcd7-115">Dieser Befehl verwendet die Pipeline zum Suchen und Herunterladen von BLOB-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="abcd7-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="abcd7-116">Beispiel 3: Herunterladen von BLOB-Inhalten mithilfe der Pipeline und eines Platzhalterzeichens</span><span class="sxs-lookup"><span data-stu-id="abcd7-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="abcd7-117">In diesem Beispiel wird das Platzhalterzeichen Sternchen und die Pipeline verwendet, um BLOB-Inhalt zu suchen und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="abcd7-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="abcd7-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="abcd7-118">PARAMETERS</span></span>

### <span data-ttu-id="abcd7-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="abcd7-119">-Blob</span></span>
<span data-ttu-id="abcd7-120">Gibt den Namen des BLOB an, das heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="abcd7-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="abcd7-121">-CheckMd5</span></span>
<span data-ttu-id="abcd7-122">Gibt an, ob die MD5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="abcd7-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="abcd7-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="abcd7-124">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="abcd7-125">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="abcd7-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="abcd7-126">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="abcd7-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="abcd7-127">-CloudBlob</span></span>
<span data-ttu-id="abcd7-128">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="abcd7-129">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="abcd7-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="abcd7-130">-CloudBlobContainer</span></span>
<span data-ttu-id="abcd7-131">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Clientbibliothek an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="abcd7-132">Sie können Sie erstellen oder das Get-AzureStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="abcd7-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="abcd7-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="abcd7-134">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="abcd7-135">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="abcd7-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="abcd7-136">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="abcd7-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="abcd7-137">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="abcd7-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="abcd7-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="abcd7-138">The default value is 10.</span></span>

<span data-ttu-id="abcd7-139">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="abcd7-139">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-140">-Container</span><span class="sxs-lookup"><span data-stu-id="abcd7-140">-Container</span></span>
<span data-ttu-id="abcd7-141">Gibt den Namen des Containers an, der das BLOB enthält, das Sie herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="abcd7-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-142">-Context</span><span class="sxs-lookup"><span data-stu-id="abcd7-142">-Context</span></span>
<span data-ttu-id="abcd7-143">Gibt das Azure-Speicherkonto an, aus dem Sie BLOB-Inhalte herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="abcd7-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="abcd7-144">Sie können das New-AzureStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="abcd7-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-145">-Ziel</span><span class="sxs-lookup"><span data-stu-id="abcd7-145">-Destination</span></span>
<span data-ttu-id="abcd7-146">Gibt den Speicherort für die heruntergeladene Datei an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-147">-Force</span><span class="sxs-lookup"><span data-stu-id="abcd7-147">-Force</span></span>
<span data-ttu-id="abcd7-148">Eine vorhandene Datei wird ohne Bestätigung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="abcd7-148">Overwrites an existing file without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="abcd7-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="abcd7-150">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="abcd7-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="abcd7-151">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="abcd7-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abcd7-152">-Confirm</span></span>
<span data-ttu-id="abcd7-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abcd7-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abcd7-154">-WhatIf</span></span>
<span data-ttu-id="abcd7-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abcd7-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abcd7-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abcd7-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abcd7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abcd7-157">CommonParameters</span></span>
<span data-ttu-id="abcd7-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abcd7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abcd7-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abcd7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abcd7-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abcd7-160">INPUTS</span></span>

### <span data-ttu-id="abcd7-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="abcd7-161">IStorageContext</span></span>

<span data-ttu-id="abcd7-162">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="abcd7-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="abcd7-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abcd7-163">OUTPUTS</span></span>

### <span data-ttu-id="abcd7-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="abcd7-164">AzureStorageContainer</span></span>

## <span data-ttu-id="abcd7-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="abcd7-165">NOTES</span></span>
* <span data-ttu-id="abcd7-166">Wenn der BLOB-Name für den lokalen Computer ungültig ist, löst dieses Cmdlet ihn, falls möglich, selbst.</span><span class="sxs-lookup"><span data-stu-id="abcd7-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="abcd7-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abcd7-167">RELATED LINKS</span></span>

[<span data-ttu-id="abcd7-168">Satz-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="abcd7-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="abcd7-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="abcd7-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="abcd7-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="abcd7-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
