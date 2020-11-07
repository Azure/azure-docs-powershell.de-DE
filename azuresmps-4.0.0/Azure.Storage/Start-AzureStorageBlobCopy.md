---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01edb18c72487ada7c51408ce38502b6e87b2f56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662016"
---
# <span data-ttu-id="d95c9-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d95c9-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="d95c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d95c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d95c9-103">Beginnt, ein BLOB zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d95c9-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="d95c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d95c9-104">SYNTAX</span></span>

### <span data-ttu-id="d95c9-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="d95c9-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="d95c9-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-112">Fileinstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="d95c9-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d95c9-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="d95c9-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d95c9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d95c9-115">DESCRIPTION</span></span>
<span data-ttu-id="d95c9-116">Mit dem Cmdlet **Start-AzureStorageBlobCopy** wird ein BLOB kopiert.</span><span class="sxs-lookup"><span data-stu-id="d95c9-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="d95c9-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d95c9-117">EXAMPLES</span></span>

### <span data-ttu-id="d95c9-118">Beispiel 1: Kopieren eines benannten BLOB</span><span class="sxs-lookup"><span data-stu-id="d95c9-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="d95c9-119">Mit diesem Befehl wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 aus dem Container mit dem Namen ContosoUploads in den Container mit dem Namen ContosoArchives gestartet.</span><span class="sxs-lookup"><span data-stu-id="d95c9-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="d95c9-120">Beispiel 2: Abrufen eines Containers zum Angeben der zu kopierenden BLOBs</span><span class="sxs-lookup"><span data-stu-id="d95c9-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="d95c9-121">Dieser Befehl ruft den Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzureStorageContainer** ab und übergibt dann den Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d95c9-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d95c9-122">Mit diesem Cmdlet wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 gestartet.</span><span class="sxs-lookup"><span data-stu-id="d95c9-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="d95c9-123">Das vorherige Cmdlet stellt den Quellcontainer bereit.</span><span class="sxs-lookup"><span data-stu-id="d95c9-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="d95c9-124">Der *DestContainer* -Parameter gibt ContosoArchives als Zielcontainer an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="d95c9-125">Beispiel 3: Abrufen eines zu kopierenden BLOBs</span><span class="sxs-lookup"><span data-stu-id="d95c9-125">Example 3: Get a blob to copy</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="d95c9-126">Dieser Befehl ruft die BLOBs im Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzureStorageBlob** ab und übergibt dann die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d95c9-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d95c9-127">Dieses Cmdlet startet den Kopiervorgang der BLOBs in den Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="d95c9-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="d95c9-128">Beispiel 4: Kopieren eines als Objekt angegebenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="d95c9-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="d95c9-129">Der erste Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="d95c9-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="d95c9-130">Der Befehl speichert das Objekt in der $SrcBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="d95c9-130">The command stores that object in the $SrcBlob variable.</span></span>

<span data-ttu-id="d95c9-131">Der zweite Befehl ruft das BLOB mit dem Namen ContosoPlanning2015Archived im Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="d95c9-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="d95c9-132">Der Befehl speichert das Objekt in der $DestBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="d95c9-132">The command stores that object in the $DestBlob variable.</span></span>

<span data-ttu-id="d95c9-133">Mit dem letzten Befehl wird der Kopiervorgang aus dem Quellcontainer in den Zielcontainer gestartet.</span><span class="sxs-lookup"><span data-stu-id="d95c9-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="d95c9-134">Der Befehl verwendet die standardmäßige Punktnotation, um die **ICloudBlob** -Objekte für die $SrcBlob-und $DestBlob-BLOBs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d95c9-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="d95c9-135">Beispiel 5: Kopieren eines BLOB aus einem URI</span><span class="sxs-lookup"><span data-stu-id="d95c9-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="d95c9-136">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="d95c9-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>

<span data-ttu-id="d95c9-137">Der zweite Befehl kopiert die Datei aus dem angegebenen URI in das BLOB mit dem Namen ContosoPlanning im Container mit dem Namen ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="d95c9-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="d95c9-138">Der Befehl startet den Kopiervorgang im Kontext, der in $context gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d95c9-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="d95c9-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="d95c9-139">PARAMETERS</span></span>

### <span data-ttu-id="d95c9-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="d95c9-140">-AbsoluteUri</span></span>
<span data-ttu-id="d95c9-141">Gibt den absoluten URI einer Datei an, die in ein Azure Storage-BLOB kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d95c9-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="d95c9-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d95c9-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d95c9-143">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d95c9-144">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="d95c9-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d95c9-145">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d95c9-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d95c9-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="d95c9-146">-CloudBlob</span></span>
<span data-ttu-id="d95c9-147">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="d95c9-148">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d95c9-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="d95c9-149">-CloudBlobContainer</span></span>
<span data-ttu-id="d95c9-150">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="d95c9-151">Mit diesem Cmdlet wird ein BLOB aus dem Container kopiert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d95c9-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="d95c9-152">Verwenden Sie das Get-AzureStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d95c9-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="d95c9-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d95c9-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d95c9-154">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d95c9-155">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="d95c9-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d95c9-156">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d95c9-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d95c9-157">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d95c9-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d95c9-158">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d95c9-158">The default value is 10.</span></span>

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

### <span data-ttu-id="d95c9-159">-Context</span><span class="sxs-lookup"><span data-stu-id="d95c9-159">-Context</span></span>
<span data-ttu-id="d95c9-160">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d95c9-161">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d95c9-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="d95c9-162">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="d95c9-162">-DestBlob</span></span>
<span data-ttu-id="d95c9-163">Gibt den Namen des Ziel-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-163">Specifies the name of the destination blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="d95c9-164">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="d95c9-164">-DestCloudBlob</span></span>
<span data-ttu-id="d95c9-165">Gibt ein Ziel- **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-165">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-166">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="d95c9-166">-DestContainer</span></span>
<span data-ttu-id="d95c9-167">Gibt den Namen des Zielcontainers an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-167">Specifies the name of the destination container.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-168">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="d95c9-168">-DestContext</span></span>
<span data-ttu-id="d95c9-169">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-169">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d95c9-170">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d95c9-170">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d95c9-171">-Force</span><span class="sxs-lookup"><span data-stu-id="d95c9-171">-Force</span></span>
<span data-ttu-id="d95c9-172">Gibt an, dass das Ziel-BLOB von diesem Cmdlet überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d95c9-172">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d95c9-173">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d95c9-173">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d95c9-174">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-174">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d95c9-175">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d95c9-175">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d95c9-176">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="d95c9-176">-SrcBlob</span></span>
<span data-ttu-id="d95c9-177">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-177">Specifies the name of the source blob.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-178">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="d95c9-178">-SrcContainer</span></span>
<span data-ttu-id="d95c9-179">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-179">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="d95c9-180">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="d95c9-180">-SrcDir</span></span>
<span data-ttu-id="d95c9-181">Gibt ein **CloudFileDirectory** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-181">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-182">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="d95c9-182">-SrcFile</span></span>
<span data-ttu-id="d95c9-183">Gibt an Sie ein **clouddatei** -Objekt aus der Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="d95c9-183">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="d95c9-184">Sie können Sie erstellen oder Get-AzureStorageFile Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="d95c9-184">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-185">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="d95c9-185">-SrcFilePath</span></span>
<span data-ttu-id="d95c9-186">Gibt den relativen Quellpfad der Quelldatei des Quellverzeichnisses oder der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-186">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-187">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="d95c9-187">-SrcShare</span></span>
<span data-ttu-id="d95c9-188">Gibt ein **CloudFileShare** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-188">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="d95c9-189">Sie können Sie erstellen oder Get-AzureStorageShare Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="d95c9-189">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-190">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="d95c9-190">-SrcShareName</span></span>
<span data-ttu-id="d95c9-191">Gibt den Namen der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="d95c9-191">Specifies the source share name.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d95c9-192">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d95c9-192">-Confirm</span></span>
<span data-ttu-id="d95c9-193">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d95c9-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d95c9-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d95c9-194">-WhatIf</span></span>
<span data-ttu-id="d95c9-195">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d95c9-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d95c9-196">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d95c9-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d95c9-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95c9-197">CommonParameters</span></span>
<span data-ttu-id="d95c9-198">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d95c9-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95c9-199">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95c9-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95c9-200">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d95c9-200">INPUTS</span></span>

## <span data-ttu-id="d95c9-201">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d95c9-201">OUTPUTS</span></span>

## <span data-ttu-id="d95c9-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="d95c9-202">NOTES</span></span>

## <span data-ttu-id="d95c9-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d95c9-203">RELATED LINKS</span></span>

[<span data-ttu-id="d95c9-204">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="d95c9-204">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="d95c9-205">Stopp-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d95c9-205">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
