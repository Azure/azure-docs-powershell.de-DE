---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 56b5a98e7654d7b8562a166a82e0596643087338
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842848"
---
# <span data-ttu-id="bdee5-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdee5-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="bdee5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdee5-102">SYNOPSIS</span></span>
<span data-ttu-id="bdee5-103">Beginnt, ein BLOB zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="bdee5-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="bdee5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdee5-104">SYNTAX</span></span>

### <span data-ttu-id="bdee5-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdee5-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdee5-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdee5-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdee5-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdee5-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="bdee5-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdee5-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdee5-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdee5-112">Fileinstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdee5-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="bdee5-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdee5-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="bdee5-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdee5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdee5-115">DESCRIPTION</span></span>
<span data-ttu-id="bdee5-116">Mit dem Cmdlet **Start-AzStorageBlobCopy** wird ein BLOB kopiert.</span><span class="sxs-lookup"><span data-stu-id="bdee5-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="bdee5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdee5-117">EXAMPLES</span></span>

### <span data-ttu-id="bdee5-118">Beispiel 1: Kopieren eines benannten BLOB</span><span class="sxs-lookup"><span data-stu-id="bdee5-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="bdee5-119">Mit diesem Befehl wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 aus dem Container mit dem Namen ContosoUploads in den Container mit dem Namen ContosoArchives gestartet.</span><span class="sxs-lookup"><span data-stu-id="bdee5-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="bdee5-120">Beispiel 2: Abrufen eines Containers zum Angeben der zu kopierenden BLOBs</span><span class="sxs-lookup"><span data-stu-id="bdee5-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="bdee5-121">Dieser Befehl ruft den Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzStorageContainer** ab und übergibt dann den Container mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdee5-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bdee5-122">Mit diesem Cmdlet wird der Kopiervorgang des BLOB mit dem Namen ContosoPlanning2015 gestartet.</span><span class="sxs-lookup"><span data-stu-id="bdee5-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="bdee5-123">Das vorherige Cmdlet stellt den Quellcontainer bereit.</span><span class="sxs-lookup"><span data-stu-id="bdee5-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="bdee5-124">Der *DestContainer* -Parameter gibt ContosoArchives als Zielcontainer an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="bdee5-125">Beispiel 3: Abrufen aller BLOBs in einem Container und Kopieren der BLOBs</span><span class="sxs-lookup"><span data-stu-id="bdee5-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="bdee5-126">Dieser Befehl ruft die BLOBs im Container mit dem Namen ContosoUploads mit dem Cmdlet **Get-AzStorageBlob** ab und übergibt dann die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdee5-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bdee5-127">Dieses Cmdlet startet den Kopiervorgang der BLOBs in den Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="bdee5-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="bdee5-128">Beispiel 4: Kopieren eines als Objekt angegebenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="bdee5-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="bdee5-129">Der erste Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="bdee5-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="bdee5-130">Der Befehl speichert das Objekt in der $SrcBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="bdee5-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="bdee5-131">Der zweite Befehl ruft das BLOB mit dem Namen ContosoPlanning2015Archived im Container mit dem Namen ContosoArchives.</span><span class="sxs-lookup"><span data-stu-id="bdee5-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="bdee5-132">Der Befehl speichert das Objekt in der $DestBlob Variablen.</span><span class="sxs-lookup"><span data-stu-id="bdee5-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="bdee5-133">Mit dem letzten Befehl wird der Kopiervorgang aus dem Quellcontainer in den Zielcontainer gestartet.</span><span class="sxs-lookup"><span data-stu-id="bdee5-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="bdee5-134">Der Befehl verwendet die standardmäßige Punktnotation, um die **ICloudBlob** -Objekte für die $SrcBlob-und $DestBlob-BLOBs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bdee5-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="bdee5-135">Beispiel 5: Kopieren eines BLOB aus einem URI</span><span class="sxs-lookup"><span data-stu-id="bdee5-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="bdee5-136">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="bdee5-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="bdee5-137">Der zweite Befehl kopiert die Datei aus dem angegebenen URI in das BLOB mit dem Namen ContosoPlanning im Container mit dem Namen ContosoArchive.</span><span class="sxs-lookup"><span data-stu-id="bdee5-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="bdee5-138">Der Befehl startet den Kopiervorgang im Kontext, der in $context gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="bdee5-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="bdee5-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdee5-139">PARAMETERS</span></span>

### <span data-ttu-id="bdee5-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="bdee5-140">-AbsoluteUri</span></span>
<span data-ttu-id="bdee5-141">Gibt den absoluten URI einer Datei an, die in ein Azure Storage-BLOB kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdee5-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="bdee5-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bdee5-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bdee5-143">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bdee5-144">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="bdee5-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bdee5-145">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bdee5-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bdee5-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-146">-CloudBlob</span></span>
<span data-ttu-id="bdee5-147">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bdee5-148">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdee5-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bdee5-149">-CloudBlobContainer</span></span>
<span data-ttu-id="bdee5-150">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="bdee5-151">Mit diesem Cmdlet wird ein BLOB aus dem Container kopiert, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bdee5-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="bdee5-152">Verwenden Sie das Get-AzStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdee5-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bdee5-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bdee5-154">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bdee5-155">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="bdee5-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bdee5-156">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="bdee5-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bdee5-157">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="bdee5-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bdee5-158">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="bdee5-158">The default value is 10.</span></span>

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

### <span data-ttu-id="bdee5-159">-Context</span><span class="sxs-lookup"><span data-stu-id="bdee5-159">-Context</span></span>
<span data-ttu-id="bdee5-160">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bdee5-161">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdee5-161">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bdee5-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdee5-162">-DefaultProfile</span></span>
<span data-ttu-id="bdee5-163">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdee5-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdee5-164">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-164">-DestBlob</span></span>
<span data-ttu-id="bdee5-165">Gibt den Namen des Ziel-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-165">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="bdee5-166">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-166">-DestCloudBlob</span></span>
<span data-ttu-id="bdee5-167">Gibt ein Ziel- **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-167">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-168">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="bdee5-168">-DestContainer</span></span>
<span data-ttu-id="bdee5-169">Gibt den Namen des Zielcontainers an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-169">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="bdee5-170">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="bdee5-170">-DestContext</span></span>
<span data-ttu-id="bdee5-171">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-171">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bdee5-172">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdee5-172">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bdee5-173">-Force</span><span class="sxs-lookup"><span data-stu-id="bdee5-173">-Force</span></span>
<span data-ttu-id="bdee5-174">Gibt an, dass das Ziel-BLOB von diesem Cmdlet überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bdee5-174">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="bdee5-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="bdee5-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="bdee5-176">BLOB-Ebene der Premium Seite</span><span class="sxs-lookup"><span data-stu-id="bdee5-176">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bdee5-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bdee5-178">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="bdee5-179">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bdee5-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="bdee5-180">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-180">-SrcBlob</span></span>
<span data-ttu-id="bdee5-181">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-181">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="bdee5-182">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="bdee5-182">-SrcContainer</span></span>
<span data-ttu-id="bdee5-183">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-183">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="bdee5-184">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="bdee5-184">-SrcDir</span></span>
<span data-ttu-id="bdee5-185">Gibt ein **CloudFileDirectory** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-185">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-186">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="bdee5-186">-SrcFile</span></span>
<span data-ttu-id="bdee5-187">Gibt an Sie ein **clouddatei** -Objekt aus der Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="bdee5-187">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bdee5-188">Sie können Sie erstellen oder Get-AzStorageFile Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="bdee5-188">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-189">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="bdee5-189">-SrcFilePath</span></span>
<span data-ttu-id="bdee5-190">Gibt den relativen Quellpfad der Quelldatei des Quellverzeichnisses oder der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-190">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="bdee5-191">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="bdee5-191">-SrcShare</span></span>
<span data-ttu-id="bdee5-192">Gibt ein **CloudFileShare** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-192">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="bdee5-193">Sie können Sie erstellen oder Get-AzStorageShare Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="bdee5-193">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdee5-194">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="bdee5-194">-SrcShareName</span></span>
<span data-ttu-id="bdee5-195">Gibt den Namen der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="bdee5-195">Specifies the source share name.</span></span>

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

### <span data-ttu-id="bdee5-196">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdee5-196">-Confirm</span></span>
<span data-ttu-id="bdee5-197">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdee5-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdee5-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdee5-198">-WhatIf</span></span>
<span data-ttu-id="bdee5-199">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdee5-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdee5-200">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdee5-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdee5-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdee5-201">CommonParameters</span></span>
<span data-ttu-id="bdee5-202">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdee5-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdee5-203">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdee5-203">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdee5-204">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdee5-204">INPUTS</span></span>

### <span data-ttu-id="bdee5-205">Microsoft. WindowsAz. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-205">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="bdee5-206">Microsoft. WindowsAz. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="bdee5-206">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="bdee5-207">Microsoft. WindowsAz. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="bdee5-207">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="bdee5-208">Parameter: srcfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bdee5-208">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="bdee5-209">System. String</span><span class="sxs-lookup"><span data-stu-id="bdee5-209">System.String</span></span>

### <span data-ttu-id="bdee5-210">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bdee5-210">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bdee5-211">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdee5-211">OUTPUTS</span></span>

### <span data-ttu-id="bdee5-212">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="bdee5-212">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="bdee5-213">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdee5-213">NOTES</span></span>

## <span data-ttu-id="bdee5-214">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdee5-214">RELATED LINKS</span></span>

[<span data-ttu-id="bdee5-215">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="bdee5-215">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="bdee5-216">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="bdee5-216">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
