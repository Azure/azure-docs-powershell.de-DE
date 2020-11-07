---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: 53f162ccf811176d375c745b1dbb539dba10f000
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843099"
---
# <span data-ttu-id="9c1ce-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9c1ce-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="9c1ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1ce-103">Lädt ein Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="9c1ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c1ce-104">SYNTAX</span></span>

### <span data-ttu-id="9c1ce-105">ReceiveManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c1ce-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c1ce-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="9c1ce-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c1ce-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="9c1ce-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c1ce-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c1ce-108">DESCRIPTION</span></span>
<span data-ttu-id="9c1ce-109">Das Cmdlet " **Get-AzStorageBlobContent** " lädt das angegebene Speicher-BLOB herunter.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="9c1ce-110">Wenn der BLOB-Name für den lokalen Computer nicht gültig ist, wird er von diesem Cmdlet automatisch aufgelöst, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="9c1ce-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c1ce-111">EXAMPLES</span></span>

### <span data-ttu-id="9c1ce-112">Beispiel 1: Herunterladen von BLOB-Inhalten nach Name</span><span class="sxs-lookup"><span data-stu-id="9c1ce-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="9c1ce-113">Mit diesem Befehl wird ein BLOB nach Name heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="9c1ce-114">Beispiel 2: Herunterladen von BLOB-Inhalten mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="9c1ce-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="9c1ce-115">Dieser Befehl verwendet die Pipeline zum Suchen und Herunterladen von BLOB-Inhalten.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="9c1ce-116">Beispiel 3: Herunterladen von BLOB-Inhalten mithilfe der Pipeline und eines Platzhalterzeichens</span><span class="sxs-lookup"><span data-stu-id="9c1ce-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="9c1ce-117">In diesem Beispiel wird das Platzhalterzeichen Sternchen und die Pipeline verwendet, um BLOB-Inhalt zu suchen und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="9c1ce-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c1ce-118">PARAMETERS</span></span>

### <span data-ttu-id="9c1ce-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9c1ce-119">-Blob</span></span>
<span data-ttu-id="9c1ce-120">Gibt den Namen des BLOB an, das heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-120">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="9c1ce-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="9c1ce-121">-CheckMd5</span></span>
<span data-ttu-id="9c1ce-122">Gibt an, ob die MD5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="9c1ce-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c1ce-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9c1ce-124">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9c1ce-125">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9c1ce-126">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9c1ce-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9c1ce-127">-CloudBlob</span></span>
<span data-ttu-id="9c1ce-128">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="9c1ce-129">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1ce-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9c1ce-130">-CloudBlobContainer</span></span>
<span data-ttu-id="9c1ce-131">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Clientbibliothek an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="9c1ce-132">Sie können Sie erstellen oder das Get-AzStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-132">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c1ce-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9c1ce-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9c1ce-134">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9c1ce-135">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9c1ce-136">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9c1ce-137">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9c1ce-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-138">The default value is 10.</span></span>
<span data-ttu-id="9c1ce-139">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-139">The default value is 10.</span></span>

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

### <span data-ttu-id="9c1ce-140">-Container</span><span class="sxs-lookup"><span data-stu-id="9c1ce-140">-Container</span></span>
<span data-ttu-id="9c1ce-141">Gibt den Namen des Containers an, der das BLOB enthält, das Sie herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-141">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="9c1ce-142">-Context</span><span class="sxs-lookup"><span data-stu-id="9c1ce-142">-Context</span></span>
<span data-ttu-id="9c1ce-143">Gibt das Azure-Speicherkonto an, aus dem Sie BLOB-Inhalte herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="9c1ce-144">Sie können das New-AzStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-144">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="9c1ce-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1ce-145">-DefaultProfile</span></span>
<span data-ttu-id="9c1ce-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c1ce-147">-Ziel</span><span class="sxs-lookup"><span data-stu-id="9c1ce-147">-Destination</span></span>
<span data-ttu-id="9c1ce-148">Gibt den Speicherort für die heruntergeladene Datei an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-148">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="9c1ce-149">-Force</span><span class="sxs-lookup"><span data-stu-id="9c1ce-149">-Force</span></span>
<span data-ttu-id="9c1ce-150">Eine vorhandene Datei wird ohne Bestätigung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-150">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="9c1ce-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9c1ce-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9c1ce-152">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-152">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9c1ce-153">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-153">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9c1ce-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c1ce-154">-Confirm</span></span>
<span data-ttu-id="9c1ce-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c1ce-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c1ce-156">-WhatIf</span></span>
<span data-ttu-id="9c1ce-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c1ce-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c1ce-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1ce-159">CommonParameters</span></span>
<span data-ttu-id="9c1ce-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1ce-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c1ce-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1ce-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c1ce-162">INPUTS</span></span>

### <span data-ttu-id="9c1ce-163">Microsoft. WindowsAz. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9c1ce-163">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="9c1ce-164">Microsoft. WindowsAz. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="9c1ce-164">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="9c1ce-165">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c1ce-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9c1ce-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c1ce-166">OUTPUTS</span></span>

### <span data-ttu-id="9c1ce-167">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c1ce-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="9c1ce-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c1ce-168">NOTES</span></span>
* <span data-ttu-id="9c1ce-169">Wenn der BLOB-Name für den lokalen Computer ungültig ist, löst dieses Cmdlet ihn, falls möglich, selbst.</span><span class="sxs-lookup"><span data-stu-id="9c1ce-169">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="9c1ce-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c1ce-170">RELATED LINKS</span></span>

[<span data-ttu-id="9c1ce-171">Satz-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="9c1ce-171">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="9c1ce-172">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c1ce-172">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="9c1ce-173">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c1ce-173">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
