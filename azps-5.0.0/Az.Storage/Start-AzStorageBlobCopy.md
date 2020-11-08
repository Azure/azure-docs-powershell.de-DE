---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175952"
---
# <span data-ttu-id="1cfc2-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1cfc2-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="1cfc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfc2-103">Beginnt, ein BLOB zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="1cfc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cfc2-104">SYNTAX</span></span>

### <span data-ttu-id="1cfc2-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="1cfc2-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="1cfc2-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-112">Fileinstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="1cfc2-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="1cfc2-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cfc2-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cfc2-115">DESCRIPTION</span></span>
<span data-ttu-id="1cfc2-116">Mit dem Cmdlet **Start-AzStorageBlobCopy** wird ein BLOB kopiert.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="1cfc2-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cfc2-117">EXAMPLES</span></span>

### <span data-ttu-id="1cfc2-118">Beispiel 1: Kopieren eines benannten BLOB</span><span class="sxs-lookup"><span data-stu-id="1cfc2-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="1cfc2-119">Mit diesem Befehl wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 aus dem Container mit dem Namen ContosoUploads in den Container mit dem Namen ContosoArchives gestartet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="1cfc2-120">Beispiel 2: Abrufen eines Containers zum Angeben der zu kopierenden BLOBs</span><span class="sxs-lookup"><span data-stu-id="1cfc2-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="1cfc2-121">Dieser Befehl ruft den Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzStorageContainer** ab und übergibt dann den Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1cfc2-122">Mit diesem Cmdlet wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 gestartet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="1cfc2-123">Das vorherige Cmdlet stellt den Quellcontainer bereit.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="1cfc2-124">Der *DestContainer* -Parameter gibt ContosoArchives als Zielcontainer an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="1cfc2-125">Beispiel 3: Abrufen aller BLOBs in einem Container und Kopieren der BLOBs</span><span class="sxs-lookup"><span data-stu-id="1cfc2-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="1cfc2-126">Dieser Befehl ruft die BLOBs im Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzStorageBlob** ab und übergibt dann die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1cfc2-127">Dieses Cmdlet startet den Kopiervorgang der BLOBs in den Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="1cfc2-128">Beispiel 4: Kopieren eines als Objekt angegebenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="1cfc2-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="1cfc2-129">Der erste Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="1cfc2-130">Der Befehl speichert das Objekt in der $SrcBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="1cfc2-131">Der zweite Befehl ruft das BLOB mit dem Namen ContosoPlanning2015Archived im Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="1cfc2-132">Der Befehl speichert das Objekt in der $DestBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="1cfc2-133">Mit dem letzten Befehl wird der Kopiervorgang aus dem Quellcontainer in den Zielcontainer gestartet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="1cfc2-134">Der Befehl verwendet die standardmäßige Punktnotation, um die **ICloudBlob** -Objekte für die $SrcBlob-und $DestBlob-BLOBs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="1cfc2-135">Beispiel 5: Kopieren eines BLOB aus einem URI</span><span class="sxs-lookup"><span data-stu-id="1cfc2-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="1cfc2-136">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="1cfc2-137">Der zweite Befehl kopiert die Datei aus dem angegebenen URI in das BLOB mit dem Namen ContosoPlanning im Container mit dem Namen ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="1cfc2-138">Der Befehl startet den Kopiervorgang in den in $context gespeicherten Zielkontext.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="1cfc2-139">Es gibt keinen Quellspeicher Kontext, sodass der Quell-URI Zugriff auf das Quellobjekt haben muss.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="1cfc2-140">Wenn es sich bei der Quelle also um ein öffentliches Azure-BLOB (None) handelt, sollte der URI SAS-Token enthalten, das Lesezugriff auf das BLOB hat.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="1cfc2-141">Beispiel 6: Kopieren eines BLOB-Blocks in den Zielcontainer mit einem neuen BLOB-Namen und Festlegung des Ziel-BLOB-StandardBlobTier als "heiß", "RehydratePriority" als "groß"</span><span class="sxs-lookup"><span data-stu-id="1cfc2-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="1cfc2-142">Mit diesem Befehl wird der Kopiervorgang eines Block-BLOB-in-Zielcontainers mit einem neuen BLOB-Namen gestartet und Ziel-BLOB-StandardBlobTier als "heiß", "RehydratePriority" als "groß" festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="1cfc2-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cfc2-143">PARAMETERS</span></span>

### <span data-ttu-id="1cfc2-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="1cfc2-144">-AbsoluteUri</span></span>
<span data-ttu-id="1cfc2-145">Gibt den absoluten URI einer Datei an, die in ein Azure Storage-BLOB kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="1cfc2-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="1cfc2-146">-BlobBaseClient</span></span>
<span data-ttu-id="1cfc2-147">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="1cfc2-147">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="1cfc2-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cfc2-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1cfc2-149">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1cfc2-150">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1cfc2-151">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1cfc2-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-152">-CloudBlob</span></span>
<span data-ttu-id="1cfc2-153">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1cfc2-154">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1cfc2-155">-CloudBlobContainer</span></span>
<span data-ttu-id="1cfc2-156">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1cfc2-157">Mit diesem Cmdlet wird ein BLOB aus dem Container kopiert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="1cfc2-158">Verwenden Sie das Get-AzStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1cfc2-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1cfc2-160">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1cfc2-161">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1cfc2-162">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1cfc2-163">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1cfc2-164">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-164">The default value is 10.</span></span>

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

### <span data-ttu-id="1cfc2-165">-Context</span><span class="sxs-lookup"><span data-stu-id="1cfc2-165">-Context</span></span>
<span data-ttu-id="1cfc2-166">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1cfc2-167">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfc2-168">-DefaultProfile</span></span>
<span data-ttu-id="1cfc2-169">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfc2-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-170">-DestBlob</span></span>
<span data-ttu-id="1cfc2-171">Gibt den Namen des Ziel-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="1cfc2-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-172">-DestCloudBlob</span></span>
<span data-ttu-id="1cfc2-173">Gibt ein Ziel- **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="1cfc2-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="1cfc2-174">-DestContainer</span></span>
<span data-ttu-id="1cfc2-175">Gibt den Namen des Zielcontainers an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="1cfc2-176">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="1cfc2-176">-DestContext</span></span>
<span data-ttu-id="1cfc2-177">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1cfc2-178">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-179">-Force</span><span class="sxs-lookup"><span data-stu-id="1cfc2-179">-Force</span></span>
<span data-ttu-id="1cfc2-180">Gibt an, dass das Ziel-BLOB von diesem Cmdlet überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1cfc2-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="1cfc2-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="1cfc2-182">BLOB-Ebene der Premium Seite</span><span class="sxs-lookup"><span data-stu-id="1cfc2-182">Premium Page Blob Tier</span></span>

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

### <span data-ttu-id="1cfc2-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="1cfc2-183">-RehydratePriority</span></span>
<span data-ttu-id="1cfc2-184">BLOB-RehydratePriority blockieren</span><span class="sxs-lookup"><span data-stu-id="1cfc2-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="1cfc2-185">Gibt die Priorität an, mit der ein archiviertes BLOB rehydriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="1cfc2-186">Gültige Werte sind "höchst/Standard".</span><span class="sxs-lookup"><span data-stu-id="1cfc2-186">Valid values are High/Standard.</span></span>

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

### <span data-ttu-id="1cfc2-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1cfc2-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1cfc2-188">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1cfc2-189">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1cfc2-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-190">-SrcBlob</span></span>
<span data-ttu-id="1cfc2-191">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="1cfc2-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="1cfc2-192">-SrcContainer</span></span>
<span data-ttu-id="1cfc2-193">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="1cfc2-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="1cfc2-194">-SrcDir</span></span>
<span data-ttu-id="1cfc2-195">Gibt ein **CloudFileDirectory** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="1cfc2-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="1cfc2-196">-SrcFile</span></span>
<span data-ttu-id="1cfc2-197">Gibt ein **clouddatei** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1cfc2-198">Sie können Sie erstellen oder Get-AzStorageFile Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="1cfc2-199">-SrcFilePath</span></span>
<span data-ttu-id="1cfc2-200">Gibt den relativen Quellpfad der Quelldatei des Quellverzeichnisses oder der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="1cfc2-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="1cfc2-201">-SrcShare</span></span>
<span data-ttu-id="1cfc2-202">Gibt ein **CloudFileShare** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1cfc2-203">Sie können Sie erstellen oder Get-AzStorageShare Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="1cfc2-204">-SrcShareName</span></span>
<span data-ttu-id="1cfc2-205">Gibt den Namen der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="1cfc2-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="1cfc2-206">-StandardBlobTier</span></span>
<span data-ttu-id="1cfc2-207">BLOB-Ebene blockieren, gültige Werte sind Hot/cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="1cfc2-208">Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="1cfc2-208">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="1cfc2-209">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1cfc2-209">-Confirm</span></span>
<span data-ttu-id="1cfc2-210">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cfc2-211">-WhatIf</span></span>
<span data-ttu-id="1cfc2-212">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cfc2-213">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cfc2-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfc2-214">CommonParameters</span></span>
<span data-ttu-id="1cfc2-215">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfc2-216">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cfc2-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfc2-217">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cfc2-217">INPUTS</span></span>

### <span data-ttu-id="1cfc2-218">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="1cfc2-219">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1cfc2-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="1cfc2-220">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="1cfc2-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="1cfc2-221">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfc2-221">System.String</span></span>

### <span data-ttu-id="1cfc2-222">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1cfc2-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1cfc2-223">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cfc2-223">OUTPUTS</span></span>

### <span data-ttu-id="1cfc2-224">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="1cfc2-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="1cfc2-225">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cfc2-225">NOTES</span></span>

## <span data-ttu-id="1cfc2-226">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cfc2-226">RELATED LINKS</span></span>

[<span data-ttu-id="1cfc2-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="1cfc2-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="1cfc2-228">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1cfc2-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
