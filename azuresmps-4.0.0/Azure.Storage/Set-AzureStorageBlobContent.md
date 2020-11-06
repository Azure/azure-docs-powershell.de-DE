---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475562"
---
# <span data-ttu-id="4b8b7-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4b8b7-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="4b8b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8b7-103">Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="4b8b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b8b7-104">SYNTAX</span></span>

### <span data-ttu-id="4b8b7-105">SendManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b8b7-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8b7-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="4b8b7-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8b7-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="4b8b7-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8b7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b8b7-108">DESCRIPTION</span></span>
<span data-ttu-id="4b8b7-109">Das Cmdlet " **Satz-AzureStorageBlobContent** " lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="4b8b7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b8b7-110">EXAMPLES</span></span>

### <span data-ttu-id="4b8b7-111">Beispiel 1: Hochladen einer benannten Datei</span><span class="sxs-lookup"><span data-stu-id="4b8b7-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="4b8b7-112">Mit diesem Befehl wird die Datei mit dem Namen PlanningData in ein BLOB mit dem Namen Planning2015 hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="4b8b7-113">Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="4b8b7-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="4b8b7-114">Dieser Befehl verwendet das Core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b8b7-115">Das Cmdlet " **Satz-AzureStorageBlobContent** " lädt die Dateien in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="4b8b7-116">Beispiel 3: Überschreiben eines vorhandenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="4b8b7-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="4b8b7-117">Dieser Befehl ruft das BLOB mit dem Namen Planning2015 im ContosoUploads-Container mithilfe des Get-AzureStorageBlob-Cmdlets ab und übergibt dieses BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="4b8b7-118">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="4b8b7-119">Mit diesem Befehl wird der Parameter *Force* nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="4b8b7-120">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="4b8b7-121">Wenn Sie den Befehl bestätigen, wird das vorhandene BLOB vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="4b8b7-122">Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="4b8b7-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="4b8b7-123">Dieser Befehl ruft mit dem Cmdlet **Get-AzureStorageContainer** den Container ab, der mit der Zeichenfolge ContosoUpload beginnt, und übergibt diesen BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="4b8b7-124">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="4b8b7-125">Beispiel 5: Hochladen einer Datei und von Metadaten</span><span class="sxs-lookup"><span data-stu-id="4b8b7-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="4b8b7-126">Der erste Befehl erstellt eine Hashtabelle, die Metadaten für einen BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variablen.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="4b8b7-127">Der zweite Befehl lädt die Datei mit dem Namen ContosoPlanning in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="4b8b7-128">Das BLOB enthält die in $Metadata gespeicherten Metadaten.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="4b8b7-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b8b7-129">PARAMETERS</span></span>

### <span data-ttu-id="4b8b7-130">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4b8b7-130">-Blob</span></span>
<span data-ttu-id="4b8b7-131">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="4b8b7-132">Mit diesem Cmdlet wird eine Datei in das Azure-Speicher-BLOB hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-133">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="4b8b7-133">-BlobType</span></span>
<span data-ttu-id="4b8b7-134">Gibt den Typ für das BLOB an, das vom Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="4b8b7-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4b8b7-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b8b7-136">Blockieren</span><span class="sxs-lookup"><span data-stu-id="4b8b7-136">Block</span></span>
- <span data-ttu-id="4b8b7-137">Seite</span><span class="sxs-lookup"><span data-stu-id="4b8b7-137">Page</span></span>

<span data-ttu-id="4b8b7-138">Der Standardwert ist Block.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4b8b7-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4b8b7-140">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4b8b7-141">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4b8b7-142">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4b8b7-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4b8b7-143">-CloudBlob</span></span>
<span data-ttu-id="4b8b7-144">Gibt ein **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="4b8b7-145">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="4b8b7-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4b8b7-146">-CloudBlobContainer</span></span>
<span data-ttu-id="4b8b7-147">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4b8b7-148">Mit diesem Cmdlet wird Inhalt in ein BLOB im Container hochgeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="4b8b7-149">Verwenden Sie das Get-AzureStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="4b8b7-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4b8b7-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4b8b7-151">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4b8b7-152">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4b8b7-153">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4b8b7-154">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4b8b7-155">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-155">The default value is 10.</span></span>

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

### <span data-ttu-id="4b8b7-156">-Container</span><span class="sxs-lookup"><span data-stu-id="4b8b7-156">-Container</span></span>
<span data-ttu-id="4b8b7-157">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-157">Specifies the name of a container.</span></span>
<span data-ttu-id="4b8b7-158">Mit diesem Cmdlet wird eine Datei in ein BLOB im Container hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-159">-Context</span><span class="sxs-lookup"><span data-stu-id="4b8b7-159">-Context</span></span>
<span data-ttu-id="4b8b7-160">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4b8b7-161">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4b8b7-162">-Datei</span><span class="sxs-lookup"><span data-stu-id="4b8b7-162">-File</span></span>
<span data-ttu-id="4b8b7-163">Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-164">-Force</span><span class="sxs-lookup"><span data-stu-id="4b8b7-164">-Force</span></span>
<span data-ttu-id="4b8b7-165">Gibt an, dass mit diesem Cmdlet ein vorhandenes BLOB überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4b8b7-166">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="4b8b7-166">-Metadata</span></span>
<span data-ttu-id="4b8b7-167">Gibt Metadaten für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-168">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b8b7-168">-Properties</span></span>
<span data-ttu-id="4b8b7-169">Gibt Eigenschaften für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-169">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b8b7-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4b8b7-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4b8b7-171">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4b8b7-172">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4b8b7-173">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b8b7-173">-Confirm</span></span>
<span data-ttu-id="4b8b7-174">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8b7-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8b7-175">-WhatIf</span></span>
<span data-ttu-id="4b8b7-176">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8b7-177">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8b7-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8b7-178">CommonParameters</span></span>
<span data-ttu-id="4b8b7-179">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8b7-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8b7-180">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8b7-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8b7-181">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b8b7-181">INPUTS</span></span>

## <span data-ttu-id="4b8b7-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b8b7-182">OUTPUTS</span></span>

## <span data-ttu-id="4b8b7-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b8b7-183">NOTES</span></span>

## <span data-ttu-id="4b8b7-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b8b7-184">RELATED LINKS</span></span>

[<span data-ttu-id="4b8b7-185">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4b8b7-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="4b8b7-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4b8b7-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="4b8b7-187">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4b8b7-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
