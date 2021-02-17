---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164724"
---
# <span data-ttu-id="3ac69-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ac69-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="3ac69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac69-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac69-103">Beginnt mit dem Kopieren eines BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ac69-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="3ac69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ac69-104">SYNTAX</span></span>

### <span data-ttu-id="3ac69-105">ContainerName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ac69-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac69-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac69-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac69-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac69-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="3ac69-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac69-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac69-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac69-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac69-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3ac69-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ac69-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="3ac69-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ac69-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ac69-115">DESCRIPTION</span></span>
<span data-ttu-id="3ac69-116">Das **Cmdlet "Start-AzStorageBlobCopy"** beginnt mit dem Kopieren eines BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ac69-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="3ac69-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ac69-117">EXAMPLES</span></span>

### <span data-ttu-id="3ac69-118">Beispiel 1: Kopieren eines benannten BLOB</span><span class="sxs-lookup"><span data-stu-id="3ac69-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="3ac69-119">Mit diesem Befehl wird der Kopiervorgang des BLOB namens "ContosoPlanning2015" aus dem Container "ContosoUploads" in den Container "ContosoArchives" gestartet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3ac69-120">Beispiel 2: Get a container to specify blobs to copy</span><span class="sxs-lookup"><span data-stu-id="3ac69-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="3ac69-121">Dieser Befehl ruft den Container "ContosoUploads" mit dem **Cmdlet "Get-AzStorageContainer"** ab und übergibt den Container dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ac69-122">Dieses Cmdlet startet den Kopiervorgang des BLOB namens "ContosoPlanning2015".</span><span class="sxs-lookup"><span data-stu-id="3ac69-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="3ac69-123">Im vorherigen Cmdlet wird der Quellcontainer verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="3ac69-124">Der *Parameter "DestContainer"* gibt "ContosoArchives" als Zielcontainer an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="3ac69-125">Beispiel 3: Alle Blobs in einem Container erhalten und kopieren</span><span class="sxs-lookup"><span data-stu-id="3ac69-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="3ac69-126">Dieser Befehl ruft die BLOBS im Container mit dem Namen "ContosoUploads" mithilfe des **Cmdlets "Get-AzStorageBlob"** ab und übergibt dann die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3ac69-127">Dieses Cmdlet startet den Kopiervorgang der Blobs in den Container "ContosoArchives".</span><span class="sxs-lookup"><span data-stu-id="3ac69-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3ac69-128">Beispiel 4: Kopieren eines blobs, das als Objekt angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3ac69-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="3ac69-129">Der erste Befehl ruft das BLOB namens "ContosoPlanning2015" im Container "ContosoUploads" ab.</span><span class="sxs-lookup"><span data-stu-id="3ac69-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="3ac69-130">Der Befehl speichert dieses Objekt in der $SrcBlob Variable.</span><span class="sxs-lookup"><span data-stu-id="3ac69-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="3ac69-131">Der zweite Befehl ruft das BLOB namens "ContosoPlanning2015Archived" im Container "ContosoArchives" ab.</span><span class="sxs-lookup"><span data-stu-id="3ac69-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="3ac69-132">Der Befehl speichert dieses Objekt in der $DestBlob Variable.</span><span class="sxs-lookup"><span data-stu-id="3ac69-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="3ac69-133">Der letzte Befehl startet den Kopiervorgang aus dem Quellcontainer in den Zielcontainer.</span><span class="sxs-lookup"><span data-stu-id="3ac69-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="3ac69-134">Der Befehl verwendet die standardmäßige Punktformatierung, um die **ICloudBlob-Objekte** für die $SrcBlob und $DestBlob anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3ac69-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="3ac69-135">Beispiel 5: Kopieren eines BLOB aus einem URI</span><span class="sxs-lookup"><span data-stu-id="3ac69-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="3ac69-136">Dieser Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="3ac69-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="3ac69-137">Der zweite Befehl kopiert die Datei aus dem angegebenen URI in das BLOB namens "ContosoPlanning" im Container "ContosoArchive".</span><span class="sxs-lookup"><span data-stu-id="3ac69-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="3ac69-138">Der Befehl startet den Kopiervorgang in den Zielkontext, der in $Context.</span><span class="sxs-lookup"><span data-stu-id="3ac69-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="3ac69-139">Es gibt keinen Quellspeicherkontext, daher muss der Quell-URI Zugriff auf das Quellobjekt haben.</span><span class="sxs-lookup"><span data-stu-id="3ac69-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="3ac69-140">Beispiel: Wenn es sich bei der Quelle um kein öffentliches Azure-BLOB handelt, sollte der URI das SAS-Token enthalten, das Lesezugriff auf das BLOB hat.</span><span class="sxs-lookup"><span data-stu-id="3ac69-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="3ac69-141">Beispiel 6: Kopieren eines Block-BLOB-in-Zielcontainers mit einem neuen BLOB-Namen und Festlegen des Ziel-BLOB StandardBlobTier als "Hot", "ResdatumePriority" auf "High"</span><span class="sxs-lookup"><span data-stu-id="3ac69-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="3ac69-142">Mit diesem Befehl wird der Kopiervorgang eines Block-BLOB-zu-Zielcontainers mit einem neuen BLOB-Namen gestartet und das Ziel-BLOB StandardBlobTier als "Hot", "RenervePriority" auf "High" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3ac69-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="3ac69-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ac69-143">PARAMETERS</span></span>

### <span data-ttu-id="3ac69-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3ac69-144">-AbsoluteUri</span></span>
<span data-ttu-id="3ac69-145">Gibt den absoluten URI einer Datei an, die in ein Azure Storage-BLOB kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ac69-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="3ac69-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="3ac69-146">-BlobBaseClient</span></span>
<span data-ttu-id="3ac69-147">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="3ac69-147">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="3ac69-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ac69-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3ac69-149">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3ac69-150">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ac69-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3ac69-151">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3ac69-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3ac69-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-152">-CloudBlob</span></span>
<span data-ttu-id="3ac69-153">Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3ac69-154">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3ac69-155">-CloudBlobContainer</span></span>
<span data-ttu-id="3ac69-156">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="3ac69-157">Dieses Cmdlet kopiert ein BLOB aus dem Container, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3ac69-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="3ac69-158">Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3ac69-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3ac69-160">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3ac69-161">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="3ac69-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3ac69-162">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="3ac69-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3ac69-163">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3ac69-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3ac69-164">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3ac69-164">The default value is 10.</span></span>

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

### <span data-ttu-id="3ac69-165">-Context</span><span class="sxs-lookup"><span data-stu-id="3ac69-165">-Context</span></span>
<span data-ttu-id="3ac69-166">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3ac69-167">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac69-168">-DefaultProfile</span></span>
<span data-ttu-id="3ac69-169">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ac69-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac69-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-170">-DestBlob</span></span>
<span data-ttu-id="3ac69-171">Gibt den Namen des Ziel-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="3ac69-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-172">-DestCloudBlob</span></span>
<span data-ttu-id="3ac69-173">Gibt ein **Ziel-CloudBlob-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="3ac69-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="3ac69-174">-DestContainer</span></span>
<span data-ttu-id="3ac69-175">Gibt den Namen des Zielcontainers an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="3ac69-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="3ac69-176">-DestContext</span></span>
<span data-ttu-id="3ac69-177">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3ac69-178">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac69-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-179">-Force</span><span class="sxs-lookup"><span data-stu-id="3ac69-179">-Force</span></span>
<span data-ttu-id="3ac69-180">Gibt an, dass dieses Cmdlet den Ziel-BLOB überschreibt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3ac69-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3ac69-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="3ac69-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="3ac69-182">Premium-Seite-BLOB-Stufe</span><span class="sxs-lookup"><span data-stu-id="3ac69-182">Premium Page Blob Tier</span></span>

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

### <span data-ttu-id="3ac69-183">-ReoreePriority</span><span class="sxs-lookup"><span data-stu-id="3ac69-183">-RehydratePriority</span></span>
<span data-ttu-id="3ac69-184">Block BLOB Re hexadePriority.</span><span class="sxs-lookup"><span data-stu-id="3ac69-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="3ac69-185">Gibt die Priorität an, mit der ein archiviertes BLOB neu auf ihre BloBs umgekniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ac69-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="3ac69-186">Gültige Werte sind "Hoch/Standard".</span><span class="sxs-lookup"><span data-stu-id="3ac69-186">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="3ac69-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ac69-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3ac69-188">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3ac69-189">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3ac69-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3ac69-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-190">-SrcBlob</span></span>
<span data-ttu-id="3ac69-191">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="3ac69-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3ac69-192">-SrcContainer</span></span>
<span data-ttu-id="3ac69-193">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="3ac69-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="3ac69-194">-SrcDir</span></span>
<span data-ttu-id="3ac69-195">Gibt ein **CloudFileDirectory-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="3ac69-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="3ac69-196">-SrcFile</span></span>
<span data-ttu-id="3ac69-197">Gibt ein **CloudFile-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3ac69-198">Sie können das Cmdlet erstellen oder Get-AzStorageFile verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ac69-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="3ac69-199">-SrcFilePath</span></span>
<span data-ttu-id="3ac69-200">Gibt den relativen Pfad der Quelldatei des Quellverzeichnisses oder der Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="3ac69-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="3ac69-201">-SrcShare</span></span>
<span data-ttu-id="3ac69-202">Gibt ein **CloudFileShare-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3ac69-203">Sie können das Cmdlet erstellen oder Get-AzStorageShare verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ac69-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="3ac69-204">-SrcShareName</span></span>
<span data-ttu-id="3ac69-205">Gibt den Quellfreigabenamen an.</span><span class="sxs-lookup"><span data-stu-id="3ac69-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="3ac69-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="3ac69-206">-StandardBlobTier</span></span>
<span data-ttu-id="3ac69-207">Block BLOB Tier, gültige Werte sind Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="3ac69-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="3ac69-208">Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="3ac69-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="3ac69-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ac69-209">-Confirm</span></span>
<span data-ttu-id="3ac69-210">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ac69-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac69-211">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ac69-211">-WhatIf</span></span>
<span data-ttu-id="3ac69-212">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ac69-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac69-213">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ac69-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac69-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac69-214">CommonParameters</span></span>
<span data-ttu-id="3ac69-215">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac69-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac69-216">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac69-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac69-217">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ac69-217">INPUTS</span></span>

### <span data-ttu-id="3ac69-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3ac69-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3ac69-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="3ac69-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="3ac69-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3ac69-221">System.String</span><span class="sxs-lookup"><span data-stu-id="3ac69-221">System.String</span></span>

### <span data-ttu-id="3ac69-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ac69-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3ac69-223">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ac69-223">OUTPUTS</span></span>

### <span data-ttu-id="3ac69-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ac69-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3ac69-225">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ac69-225">NOTES</span></span>

## <span data-ttu-id="3ac69-226">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ac69-226">RELATED LINKS</span></span>

[<span data-ttu-id="3ac69-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="3ac69-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="3ac69-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3ac69-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
