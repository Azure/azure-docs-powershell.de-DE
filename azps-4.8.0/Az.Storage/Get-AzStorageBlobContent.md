---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174017"
---
# <span data-ttu-id="ef0c5-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ef0c5-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="ef0c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0c5-103">Lädt ein Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="ef0c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef0c5-104">SYNTAX</span></span>

### <span data-ttu-id="ef0c5-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef0c5-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef0c5-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ef0c5-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0c5-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ef0c5-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef0c5-108">DESCRIPTION</span></span>
<span data-ttu-id="ef0c5-109">Das Cmdlet " **Get-AzStorageBlobContent** " lädt das angegebene Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="ef0c5-110">Wenn der BLOB-Name für den lokalen Computer nicht gültig ist, wird er von diesem Cmdlet automatisch aufgelöst, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="ef0c5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef0c5-111">EXAMPLES</span></span>

### <span data-ttu-id="ef0c5-112">Beispiel 1: Herunterladen von BLOB-Inhalten nach Name</span><span class="sxs-lookup"><span data-stu-id="ef0c5-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="ef0c5-113">Mit diesem Befehl wird ein BLOB nach Name heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="ef0c5-114">Beispiel 2: Herunterladen von BLOB-Inhalten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ef0c5-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="ef0c5-115">Dieser Befehl verwendet die Pipeline zum Suchen und Herunterladen von BLOB-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ef0c5-116">Beispiel 3: Herunterladen von BLOB-Inhalten mithilfe der Pipeline und eines Platzhalterzeichens</span><span class="sxs-lookup"><span data-stu-id="ef0c5-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="ef0c5-117">In diesem Beispiel wird das Platzhalterzeichen Sternchen und die Pipeline verwendet, um BLOB-Inhalt zu suchen und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ef0c5-118">Beispiel 4: Abrufen eines BLOB-Objekts und speichern in einer Variablen und anschließendes herunterladen von BLOB-Inhalt mit dem BLOB-Objekt</span><span class="sxs-lookup"><span data-stu-id="ef0c5-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="ef0c5-119">In diesem Beispiel wird zunächst ein BLOB-Objekt abgerufen und in einer Variablen gespeichert, und dann BLOB-Inhalt mit dem BLOB-Objekt heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="ef0c5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef0c5-120">PARAMETERS</span></span>

### <span data-ttu-id="ef0c5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-121">-AsJob</span></span>
<span data-ttu-id="ef0c5-122">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ef0c5-123">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ef0c5-123">-Blob</span></span>
<span data-ttu-id="ef0c5-124">Gibt den Namen des BLOB an, das heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c5-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ef0c5-125">-BlobBaseClient</span></span>
<span data-ttu-id="ef0c5-126">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="ef0c5-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c5-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ef0c5-127">-CheckMd5</span></span>
<span data-ttu-id="ef0c5-128">Gibt an, ob die MD5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ef0c5-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef0c5-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ef0c5-130">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ef0c5-131">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ef0c5-132">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ef0c5-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-133">-CloudBlob</span></span>
<span data-ttu-id="ef0c5-134">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="ef0c5-135">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ef0c5-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ef0c5-136">-CloudBlobContainer</span></span>
<span data-ttu-id="ef0c5-137">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Clientbibliothek an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="ef0c5-138">Sie können Sie erstellen oder das Get-AzStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="ef0c5-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ef0c5-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ef0c5-140">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ef0c5-141">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ef0c5-142">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ef0c5-143">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ef0c5-144">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-144">The default value is 10.</span></span>

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

### <span data-ttu-id="ef0c5-145">-Container</span><span class="sxs-lookup"><span data-stu-id="ef0c5-145">-Container</span></span>
<span data-ttu-id="ef0c5-146">Gibt den Namen des Containers an, der das BLOB enthält, das Sie herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c5-147">-Context</span><span class="sxs-lookup"><span data-stu-id="ef0c5-147">-Context</span></span>
<span data-ttu-id="ef0c5-148">Gibt das Azure-Speicherkonto an, aus dem Sie BLOB-Inhalte herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="ef0c5-149">Sie können das New-AzStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="ef0c5-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0c5-150">-DefaultProfile</span></span>
<span data-ttu-id="ef0c5-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0c5-152">-Ziel</span><span class="sxs-lookup"><span data-stu-id="ef0c5-152">-Destination</span></span>
<span data-ttu-id="ef0c5-153">Gibt den Speicherort für die heruntergeladene Datei an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef0c5-154">-Force</span><span class="sxs-lookup"><span data-stu-id="ef0c5-154">-Force</span></span>
<span data-ttu-id="ef0c5-155">Eine vorhandene Datei wird ohne Bestätigung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="ef0c5-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef0c5-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ef0c5-157">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ef0c5-158">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ef0c5-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef0c5-159">-Confirm</span></span>
<span data-ttu-id="ef0c5-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0c5-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0c5-161">-WhatIf</span></span>
<span data-ttu-id="ef0c5-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0c5-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0c5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0c5-164">CommonParameters</span></span>
<span data-ttu-id="ef0c5-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0c5-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0c5-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0c5-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef0c5-167">INPUTS</span></span>

### <span data-ttu-id="ef0c5-168">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ef0c5-169">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ef0c5-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ef0c5-170">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef0c5-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ef0c5-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef0c5-171">OUTPUTS</span></span>

### <span data-ttu-id="ef0c5-172">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ef0c5-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef0c5-173">NOTES</span></span>
* <span data-ttu-id="ef0c5-174">Wenn der BLOB-Name für den lokalen Computer ungültig ist, löst dieses Cmdlet ihn, falls möglich, selbst.</span><span class="sxs-lookup"><span data-stu-id="ef0c5-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="ef0c5-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef0c5-175">RELATED LINKS</span></span>

[<span data-ttu-id="ef0c5-176">Satz-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ef0c5-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="ef0c5-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ef0c5-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ef0c5-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
