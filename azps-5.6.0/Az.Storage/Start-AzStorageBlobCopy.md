---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 754ac7657561ba52e28f90d951c0843a8c206484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944423"
---
# <span data-ttu-id="90e3c-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90e3c-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="90e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="90e3c-103">Beginnt mit dem Kopieren eines Blobs.</span><span class="sxs-lookup"><span data-stu-id="90e3c-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="90e3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90e3c-104">SYNTAX</span></span>

### <span data-ttu-id="90e3c-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="90e3c-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e3c-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e3c-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e3c-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e3c-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="90e3c-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e3c-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e3c-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e3c-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e3c-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="90e3c-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e3c-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="90e3c-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e3c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90e3c-115">DESCRIPTION</span></span>
<span data-ttu-id="90e3c-116">Das **Cmdlet Start-AzStorageBlobCopy** beginnt mit dem Kopieren eines Blobs.</span><span class="sxs-lookup"><span data-stu-id="90e3c-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="90e3c-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90e3c-117">EXAMPLES</span></span>

### <span data-ttu-id="90e3c-118">Beispiel 1: Kopieren eines benannten Blobs</span><span class="sxs-lookup"><span data-stu-id="90e3c-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="90e3c-119">Mit diesem Befehl wird der Kopiervorgang des Blobs namens ContosoPlanning2015 aus dem Container namens ContosoUploads in den Container contosoArchives gestartet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="90e3c-120">Beispiel 2: Einen Container zum Angeben von zu kopierenden Blobs erhalten</span><span class="sxs-lookup"><span data-stu-id="90e3c-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="90e3c-121">Dieser Befehl ruft den Container namens ContosoUploads mithilfe des **Get-AzStorageContainer-Cmdlets** ab und übergibt den Container dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90e3c-122">Dieses Cmdlet startet den Kopiervorgang des Blobs namens ContosoPlanning2015.</span><span class="sxs-lookup"><span data-stu-id="90e3c-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="90e3c-123">Das vorherige Cmdlet stellt den Quellcontainer zur.</span><span class="sxs-lookup"><span data-stu-id="90e3c-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="90e3c-124">Der *Parameter DestContainer* gibt ContosoArchives als Zielcontainer an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="90e3c-125">Beispiel 3: Alle Blobs in einem Container erhalten und kopieren</span><span class="sxs-lookup"><span data-stu-id="90e3c-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="90e3c-126">Dieser Befehl ruft die Blobs im Container contosoUploads mithilfe des **Get-AzStorageBlob-Cmdlets** ab und übergibt die Ergebnisse dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="90e3c-127">Dieses Cmdlet startet den Kopiervorgang der Blobs in den Container namens ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="90e3c-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="90e3c-128">Beispiel 4: Kopieren eines Blobs, das als Objekt angegeben ist</span><span class="sxs-lookup"><span data-stu-id="90e3c-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="90e3c-129">Der erste Befehl ruft das Blob mit dem Namen ContosoPlanning2015 im Container namens ContosoUploads ab.</span><span class="sxs-lookup"><span data-stu-id="90e3c-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="90e3c-130">Der Befehl speichert dieses Objekt in der $SrcBlob-Variable.</span><span class="sxs-lookup"><span data-stu-id="90e3c-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="90e3c-131">Der zweite Befehl ruft das Blob mit dem Namen ContosoPlanning2015Archiviert im Container namens ContosoArchives ab.</span><span class="sxs-lookup"><span data-stu-id="90e3c-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="90e3c-132">Mit dem Befehl wird dieses Objekt in der $DestBlob gespeichert.</span><span class="sxs-lookup"><span data-stu-id="90e3c-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="90e3c-133">Der letzte Befehl startet den Kopiervorgang aus dem Quellcontainer in den Zielcontainer.</span><span class="sxs-lookup"><span data-stu-id="90e3c-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="90e3c-134">Der Befehl verwendet die Standardpunkt-Notation, um die **ICloudBlob-Objekte** für die $SrcBlob und $DestBlob anzugeben.</span><span class="sxs-lookup"><span data-stu-id="90e3c-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="90e3c-135">Beispiel 5: Kopieren eines Blobs aus einem URI</span><span class="sxs-lookup"><span data-stu-id="90e3c-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="90e3c-136">Mit diesem Befehl wird ein Kontext für das Konto namens ContosoGeneral erstellt, das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="90e3c-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="90e3c-137">Mit dem zweiten Befehl wird die Datei aus dem angegebenen URI in das Blob namens ContosoPlanning im Container namens ContosoArchive kopiert.</span><span class="sxs-lookup"><span data-stu-id="90e3c-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="90e3c-138">Der Befehl startet den Kopiervorgang in den Zielkontext, der in der Datei $Context.</span><span class="sxs-lookup"><span data-stu-id="90e3c-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="90e3c-139">Es gibt keinen Quellspeicherkontext, daher muss der Quell-URI Zugriff auf das Quellobjekt haben.</span><span class="sxs-lookup"><span data-stu-id="90e3c-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="90e3c-140">Beispiel: Wenn es sich bei der Quelle um einen nicht öffentlichen Azure-Blob handelt, sollte der Uri SAS-Token enthalten, das Lesezugriff auf den Blob hat.</span><span class="sxs-lookup"><span data-stu-id="90e3c-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="90e3c-141">Beispiel 6: Kopieren eines Blockblobs in den Zielcontainer mit einem neuen Blobnamen und Festlegen des Zielblobs StandardBlobTier als "Hot", "RehydratePriority" als "Hoch"</span><span class="sxs-lookup"><span data-stu-id="90e3c-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="90e3c-142">Dieser Befehl startet den Kopiervorgang eines Blockblobs in den Zielcontainer mit einem neuen Blobnamen, und legen Sie Zielblob StandardBlobTier als "Hot", "RehydratePriority" als "Hoch"</span><span class="sxs-lookup"><span data-stu-id="90e3c-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="90e3c-143">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90e3c-143">PARAMETERS</span></span>

### <span data-ttu-id="90e3c-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="90e3c-144">-AbsoluteUri</span></span>
<span data-ttu-id="90e3c-145">Gibt den absoluten URI einer Datei an, die in einen Azure Storage-Blob kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90e3c-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="90e3c-146">-BlobBaseClient</span></span>
<span data-ttu-id="90e3c-147">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="90e3c-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90e3c-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="90e3c-149">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="90e3c-150">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e3c-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="90e3c-151">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="90e3c-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="90e3c-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-152">-CloudBlob</span></span>
<span data-ttu-id="90e3c-153">Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90e3c-154">Um ein **CloudBlob-Objekt zu** erhalten, verwenden Sie das Get-AzStorageBlob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="90e3c-155">-CloudBlobContainer</span></span>
<span data-ttu-id="90e3c-156">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="90e3c-157">Dieses Cmdlet kopiert einen Blob aus dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="90e3c-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="90e3c-158">Zum Abrufen eines **CloudBlobContainer-Objekts** verwenden Sie das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="90e3c-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="90e3c-160">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="90e3c-161">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="90e3c-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="90e3c-162">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="90e3c-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="90e3c-163">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="90e3c-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="90e3c-164">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="90e3c-164">The default value is 10.</span></span>

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

### <span data-ttu-id="90e3c-165">-Context</span><span class="sxs-lookup"><span data-stu-id="90e3c-165">-Context</span></span>
<span data-ttu-id="90e3c-166">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90e3c-167">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e3c-168">-DefaultProfile</span></span>
<span data-ttu-id="90e3c-169">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90e3c-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e3c-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-170">-DestBlob</span></span>
<span data-ttu-id="90e3c-171">Gibt den Namen des Zielblobs an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-171">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-172">-DestCloudBlob</span></span>
<span data-ttu-id="90e3c-173">Gibt ein **CloudBlob-Zielobjekt** an</span><span class="sxs-lookup"><span data-stu-id="90e3c-173">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="90e3c-174">-DestContainer</span></span>
<span data-ttu-id="90e3c-175">Gibt den Namen des Zielcontainers an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-175">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="90e3c-176">-DestContext</span></span>
<span data-ttu-id="90e3c-177">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="90e3c-178">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3c-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-179">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="90e3c-179">-Force</span></span>
<span data-ttu-id="90e3c-180">Gibt an, dass dieses Cmdlet den Zielblob überschreibt, ohne Sie zur Bestätigung auffordern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="90e3c-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="90e3c-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="90e3c-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="90e3c-182">Premium Page Blob Tier</span><span class="sxs-lookup"><span data-stu-id="90e3c-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="90e3c-183">-RehydratePriority</span></span>
<span data-ttu-id="90e3c-184">Block Blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="90e3c-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="90e3c-185">Gibt die Priorität an, mit der ein archiviertes Blob neu hydratisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90e3c-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="90e3c-186">Gültige Werte sind Hoch/Standard.</span><span class="sxs-lookup"><span data-stu-id="90e3c-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="90e3c-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="90e3c-188">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="90e3c-189">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="90e3c-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="90e3c-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-190">-SrcBlob</span></span>
<span data-ttu-id="90e3c-191">Gibt den Namen des Quellblobs an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-191">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="90e3c-192">-SrcContainer</span></span>
<span data-ttu-id="90e3c-193">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-193">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="90e3c-194">-SrcDir</span></span>
<span data-ttu-id="90e3c-195">Gibt ein **CloudFileDirectory-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="90e3c-196">-SrcFile</span></span>
<span data-ttu-id="90e3c-197">Gibt ein **CloudFile-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90e3c-198">Sie können das Cmdlet erstellen oder Get-AzStorageFile verwenden.</span><span class="sxs-lookup"><span data-stu-id="90e3c-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="90e3c-199">-SrcFilePath</span></span>
<span data-ttu-id="90e3c-200">Gibt den relativen Pfad der Quelldatei des Quellverzeichnisses oder der Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-200">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="90e3c-201">-SrcShare</span></span>
<span data-ttu-id="90e3c-202">Gibt ein **CloudFileShare-Objekt** aus der Azure Storage-Clientbibliothek an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="90e3c-203">Sie können das Cmdlet erstellen oder Get-AzStorageShare verwenden.</span><span class="sxs-lookup"><span data-stu-id="90e3c-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="90e3c-204">-SrcShareName</span></span>
<span data-ttu-id="90e3c-205">Gibt den Namen der Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="90e3c-205">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="90e3c-206">-StandardBlobTier</span></span>
<span data-ttu-id="90e3c-207">Block Blob Tier, gültige Werte sind Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="90e3c-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="90e3c-208">Details finden Sie unter https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="90e3c-208">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e3c-209">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90e3c-209">-Confirm</span></span>
<span data-ttu-id="90e3c-210">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90e3c-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e3c-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e3c-211">-WhatIf</span></span>
<span data-ttu-id="90e3c-212">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e3c-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e3c-213">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e3c-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e3c-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e3c-214">CommonParameters</span></span>
<span data-ttu-id="90e3c-215">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e3c-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e3c-216">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e3c-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e3c-217">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90e3c-217">INPUTS</span></span>

### <span data-ttu-id="90e3c-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="90e3c-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="90e3c-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="90e3c-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="90e3c-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="90e3c-221">System.String</span><span class="sxs-lookup"><span data-stu-id="90e3c-221">System.String</span></span>

### <span data-ttu-id="90e3c-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="90e3c-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="90e3c-223">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90e3c-223">OUTPUTS</span></span>

### <span data-ttu-id="90e3c-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="90e3c-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="90e3c-225">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90e3c-225">NOTES</span></span>

## <span data-ttu-id="90e3c-226">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90e3c-226">RELATED LINKS</span></span>

[<span data-ttu-id="90e3c-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="90e3c-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="90e3c-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="90e3c-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
