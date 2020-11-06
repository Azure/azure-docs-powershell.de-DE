---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc15650b9a3cf16b1448b5e971669fbd37733b94
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474217"
---
# <span data-ttu-id="a36c6-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="a36c6-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="a36c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a36c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a36c6-103">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="a36c6-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="a36c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36c6-104">SYNTAX</span></span>

### <span data-ttu-id="a36c6-105">ContainerInstance (Standard)</span><span class="sxs-lookup"><span data-stu-id="a36c6-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a36c6-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="a36c6-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a36c6-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="a36c6-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a36c6-108">Containername</span><span class="sxs-lookup"><span data-stu-id="a36c6-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a36c6-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="a36c6-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a36c6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a36c6-110">DESCRIPTION</span></span>
<span data-ttu-id="a36c6-111">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="a36c6-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="a36c6-112">Weitere Informationen zu diesem Feature finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="a36c6-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="a36c6-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a36c6-113">EXAMPLES</span></span>

### <span data-ttu-id="a36c6-114">Beispiel 1: Starten des inkrementellen Kopiervorgangs nach BLOB-Name und Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="a36c6-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="a36c6-115">Mit diesem Befehl wird der inkrementelle Kopiervorgang nach BLOB-Name und Momentaufnahme Zeit gestartet.</span><span class="sxs-lookup"><span data-stu-id="a36c6-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="a36c6-116">Beispiel 2: Starten des inkrementellen Kopiervorgangs mit dem Quell-URI</span><span class="sxs-lookup"><span data-stu-id="a36c6-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="a36c6-117">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe des Quell-URIs.</span><span class="sxs-lookup"><span data-stu-id="a36c6-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="a36c6-118">Beispiel 3: Starten des inkrementellen Kopiervorgangs mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a36c6-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="a36c6-119">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a36c6-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="a36c6-120">Beispiel 4: Starten des inkrementellen Kopiervorgangs vom CloudPageBlob-Objekt in das Ziel-BLOB mit BLOB-Namen</span><span class="sxs-lookup"><span data-stu-id="a36c6-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="a36c6-121">Mit diesem Befehl wird der inkrementelle Kopiervorgang vom CloudPageBlob-Objekt in das Ziel-BLOB mit dem BLOB-Namen gestartet.</span><span class="sxs-lookup"><span data-stu-id="a36c6-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="a36c6-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36c6-122">PARAMETERS</span></span>

### <span data-ttu-id="a36c6-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="a36c6-123">-AbsoluteUri</span></span>
<span data-ttu-id="a36c6-124">Absoluter URI für die Quelle.</span><span class="sxs-lookup"><span data-stu-id="a36c6-124">Absolute Uri to the source.</span></span>
<span data-ttu-id="a36c6-125">Beachten Sie, dass die Anmeldeinformationen im URI bereitgestellt werden sollten, wenn für die Quelle ein any erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a36c6-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a36c6-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a36c6-127">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a36c6-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="a36c6-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-128">-CloudBlob</span></span>
<span data-ttu-id="a36c6-129">CloudBlob-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a36c6-129">CloudBlob object from Azure Storage Client library.</span></span>
<span data-ttu-id="a36c6-130">Sie können Sie erstellen oder Get-AzureStorageBlob Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="a36c6-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a36c6-131">-CloudBlobContainer</span></span>
<span data-ttu-id="a36c6-132">CloudBlobContainer-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="a36c6-132">CloudBlobContainer object from Azure Storage Client library.</span></span>
<span data-ttu-id="a36c6-133">Sie können Sie erstellen oder Get-AzureStorageContainer Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="a36c6-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a36c6-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a36c6-135">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="a36c6-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="a36c6-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a36c6-136">The default value is 10.</span></span>

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

### <span data-ttu-id="a36c6-137">-Context</span><span class="sxs-lookup"><span data-stu-id="a36c6-137">-Context</span></span>
<span data-ttu-id="a36c6-138">Ursprünglicher Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="a36c6-138">Source Azure Storage Context.</span></span>
<span data-ttu-id="a36c6-139">Sie können es über New-AzureStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="a36c6-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-140">-DestBlob</span></span>
<span data-ttu-id="a36c6-141">Ziel-BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="a36c6-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-142">-DestCloudBlob</span></span>
<span data-ttu-id="a36c6-143">Ziel-CloudBlob-Objekt</span><span class="sxs-lookup"><span data-stu-id="a36c6-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="a36c6-144">-DestContainer</span></span>
<span data-ttu-id="a36c6-145">Name des Zielcontainers</span><span class="sxs-lookup"><span data-stu-id="a36c6-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-146">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="a36c6-146">-DestContext</span></span>
<span data-ttu-id="a36c6-147">Ziel-Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="a36c6-147">Destination Azure Storage Context.</span></span>
<span data-ttu-id="a36c6-148">Sie können es über New-AzureStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="a36c6-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a36c6-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a36c6-150">Der Servertimeout für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a36c6-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="a36c6-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-151">-SrcBlob</span></span>
<span data-ttu-id="a36c6-152">BLOB-Name der Quellseite.</span><span class="sxs-lookup"><span data-stu-id="a36c6-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a36c6-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="a36c6-154">BLOB-Momentaufnahme Zeit für Quellseiten.</span><span class="sxs-lookup"><span data-stu-id="a36c6-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="a36c6-155">-SrcContainer</span></span>
<span data-ttu-id="a36c6-156">Name des Quellcontainers</span><span class="sxs-lookup"><span data-stu-id="a36c6-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36c6-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a36c6-157">-Confirm</span></span>
<span data-ttu-id="a36c6-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a36c6-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a36c6-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36c6-159">-WhatIf</span></span>
<span data-ttu-id="a36c6-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a36c6-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a36c6-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a36c6-161">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="a36c6-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a36c6-162">INPUTS</span></span>

### <span data-ttu-id="a36c6-163">Microsoft. WindowsAzure. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-163">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="a36c6-164">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer System. String Microsoft. WindowsAzure. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a36c6-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="a36c6-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a36c6-165">OUTPUTS</span></span>

### <span data-ttu-id="a36c6-166">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a36c6-166">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a36c6-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="a36c6-167">NOTES</span></span>

## <span data-ttu-id="a36c6-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a36c6-168">RELATED LINKS</span></span>

