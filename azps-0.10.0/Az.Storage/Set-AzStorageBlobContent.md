---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 0730d509ddf207d7541e854b15f34c30b44093e0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842891"
---
# <span data-ttu-id="a2d37-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a2d37-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="a2d37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2d37-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d37-103">Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="a2d37-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a2d37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2d37-104">SYNTAX</span></span>

### <span data-ttu-id="a2d37-105">SendManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="a2d37-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2d37-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a2d37-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2d37-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a2d37-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d37-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2d37-108">DESCRIPTION</span></span>
<span data-ttu-id="a2d37-109">Das Cmdlet " **Satz-AzStorageBlobContent** " lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="a2d37-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a2d37-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2d37-110">EXAMPLES</span></span>

### <span data-ttu-id="a2d37-111">Beispiel 1: Hochladen einer benannten Datei</span><span class="sxs-lookup"><span data-stu-id="a2d37-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="a2d37-112">Mit diesem Befehl wird die Datei mit dem Namen PlanningData in ein BLOB mit dem Namen Planning2015 hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="a2d37-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="a2d37-113">Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="a2d37-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="a2d37-114">Dieser Befehl verwendet das Core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2d37-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a2d37-115">Das Cmdlet " **Satz-AzStorageBlobContent** " lädt die Dateien in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a2d37-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="a2d37-116">Beispiel 3: Überschreiben eines vorhandenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="a2d37-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="a2d37-117">Dieser Befehl ruft das BLOB mit dem Namen Planning2015 im ContosoUploads-Container mithilfe des Get-AzStorageBlob-Cmdlets ab und übergibt dieses BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2d37-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a2d37-118">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="a2d37-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="a2d37-119">Mit diesem Befehl wird der Parameter *Force* nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="a2d37-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="a2d37-120">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="a2d37-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="a2d37-121">Wenn Sie den Befehl bestätigen, wird das vorhandene BLOB vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="a2d37-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="a2d37-122">Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a2d37-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="a2d37-123">Dieser Befehl ruft mit dem Cmdlet **Get-AzStorageContainer** den Container ab, der mit der Zeichenfolge ContosoUpload beginnt, und übergibt diesen BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2d37-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a2d37-124">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="a2d37-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="a2d37-125">Beispiel 5: Hochladen einer Datei auf ein Page-BLOB mit Metadaten und PremiumPageBlobTier als P10</span><span class="sxs-lookup"><span data-stu-id="a2d37-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="a2d37-126">Der erste Befehl erstellt eine Hashtabelle, die Metadaten für einen BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variablen.</span><span class="sxs-lookup"><span data-stu-id="a2d37-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="a2d37-127">Der zweite Befehl lädt die Datei mit dem Namen ContosoPlanning in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a2d37-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="a2d37-128">Das BLOB enthält die Metadaten, die in $Metadata gespeichert sind, und hat PremiumPageBlobTier als P10.</span><span class="sxs-lookup"><span data-stu-id="a2d37-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="a2d37-129">Beispiel 6: Hochladen einer Datei in ein BLOB mit den angegebenen BLOB-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2d37-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="a2d37-130">Mit diesem Befehl wird die Datei mit dem Namen ContosoPlanning in den Container mit dem Namen ContosoUploads mit den angegebenen BLOB-Eigenschaften hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="a2d37-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="a2d37-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2d37-131">PARAMETERS</span></span>

### <span data-ttu-id="a2d37-132">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a2d37-132">-Blob</span></span>
<span data-ttu-id="a2d37-133">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-133">Specifies the name of a blob.</span></span>
<span data-ttu-id="a2d37-134">Mit diesem Cmdlet wird eine Datei in das Azure-Speicher-BLOB hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a2d37-134">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-135">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="a2d37-135">-BlobType</span></span>
<span data-ttu-id="a2d37-136">Gibt den Typ für das BLOB an, das vom Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="a2d37-136">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="a2d37-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a2d37-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a2d37-138">Blockieren</span><span class="sxs-lookup"><span data-stu-id="a2d37-138">Block</span></span>
- <span data-ttu-id="a2d37-139">Page der Standardwert ist Block.</span><span class="sxs-lookup"><span data-stu-id="a2d37-139">Page The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-140">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2d37-140">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a2d37-141">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-141">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a2d37-142">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="a2d37-142">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a2d37-143">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a2d37-143">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a2d37-144">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a2d37-144">-CloudBlob</span></span>
<span data-ttu-id="a2d37-145">Gibt ein **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-145">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="a2d37-146">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2d37-146">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a2d37-147">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a2d37-147">-CloudBlobContainer</span></span>
<span data-ttu-id="a2d37-148">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-148">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a2d37-149">Mit diesem Cmdlet wird Inhalt in ein BLOB im Container hochgeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a2d37-149">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a2d37-150">Verwenden Sie das Get-AzStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2d37-150">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a2d37-151">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a2d37-151">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a2d37-152">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-152">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a2d37-153">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="a2d37-153">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a2d37-154">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a2d37-154">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a2d37-155">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a2d37-155">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a2d37-156">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a2d37-156">The default value is 10.</span></span>

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

### <span data-ttu-id="a2d37-157">-Container</span><span class="sxs-lookup"><span data-stu-id="a2d37-157">-Container</span></span>
<span data-ttu-id="a2d37-158">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-158">Specifies the name of a container.</span></span>
<span data-ttu-id="a2d37-159">Mit diesem Cmdlet wird eine Datei in ein BLOB im Container hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a2d37-159">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-160">-Context</span><span class="sxs-lookup"><span data-stu-id="a2d37-160">-Context</span></span>
<span data-ttu-id="a2d37-161">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-161">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a2d37-162">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2d37-162">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a2d37-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d37-163">-DefaultProfile</span></span>
<span data-ttu-id="a2d37-164">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2d37-164">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2d37-165">-Datei</span><span class="sxs-lookup"><span data-stu-id="a2d37-165">-File</span></span>
<span data-ttu-id="a2d37-166">Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2d37-166">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-167">-Force</span><span class="sxs-lookup"><span data-stu-id="a2d37-167">-Force</span></span>
<span data-ttu-id="a2d37-168">Gibt an, dass mit diesem Cmdlet ein vorhandenes BLOB überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a2d37-168">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a2d37-169">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="a2d37-169">-Metadata</span></span>
<span data-ttu-id="a2d37-170">Gibt Metadaten für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-170">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-171">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="a2d37-171">-PremiumPageBlobTier</span></span>
<span data-ttu-id="a2d37-172">Seiten-BLOB-Ebene</span><span class="sxs-lookup"><span data-stu-id="a2d37-172">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-173">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a2d37-173">-Properties</span></span>
<span data-ttu-id="a2d37-174">Gibt Eigenschaften für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-174">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="a2d37-175">Die unterstützten Eigenschaften sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="a2d37-175">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2d37-176">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a2d37-176">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a2d37-177">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a2d37-177">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a2d37-178">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a2d37-178">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a2d37-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2d37-179">-Confirm</span></span>
<span data-ttu-id="a2d37-180">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2d37-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d37-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d37-181">-WhatIf</span></span>
<span data-ttu-id="a2d37-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d37-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d37-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2d37-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d37-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d37-184">CommonParameters</span></span>
<span data-ttu-id="a2d37-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d37-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d37-186">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d37-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d37-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2d37-187">INPUTS</span></span>

### <span data-ttu-id="a2d37-188">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d37-188">System.String</span></span>

### <span data-ttu-id="a2d37-189">Microsoft. WindowsAz. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a2d37-189">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a2d37-190">Microsoft. WindowsAz. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a2d37-190">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a2d37-191">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a2d37-191">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a2d37-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2d37-192">OUTPUTS</span></span>

### <span data-ttu-id="a2d37-193">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2d37-193">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a2d37-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2d37-194">NOTES</span></span>

## <span data-ttu-id="a2d37-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2d37-195">RELATED LINKS</span></span>

[<span data-ttu-id="a2d37-196">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a2d37-196">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a2d37-197">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2d37-197">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a2d37-198">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a2d37-198">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
