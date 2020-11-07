---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d9a602e3e946e28dd04b67c030aeec2aecc3ec93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658750"
---
# <span data-ttu-id="2bdae-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2bdae-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="2bdae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bdae-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdae-103">Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="2bdae-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="2bdae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bdae-104">SYNTAX</span></span>

### <span data-ttu-id="2bdae-105">SendManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="2bdae-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bdae-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2bdae-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bdae-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2bdae-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bdae-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bdae-108">DESCRIPTION</span></span>
<span data-ttu-id="2bdae-109">Das Cmdlet " **Satz-AzStorageBlobContent** " lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="2bdae-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="2bdae-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bdae-110">EXAMPLES</span></span>

### <span data-ttu-id="2bdae-111">Beispiel 1: Hochladen einer benannten Datei</span><span class="sxs-lookup"><span data-stu-id="2bdae-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="2bdae-112">Mit diesem Befehl wird die Datei mit dem Namen PlanningData in ein BLOB mit dem Namen Planning2015 hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2bdae-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="2bdae-113">Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="2bdae-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="2bdae-114">Dieser Befehl verwendet das Core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bdae-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2bdae-115">Das Cmdlet " **Satz-AzStorageBlobContent** " lädt die Dateien in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="2bdae-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="2bdae-116">Beispiel 3: Überschreiben eines vorhandenen BLOBs</span><span class="sxs-lookup"><span data-stu-id="2bdae-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="2bdae-117">Dieser Befehl ruft das BLOB mit dem Namen Planning2015 im ContosoUploads-Container mithilfe des Get-AzStorageBlob-Cmdlets ab und übergibt dieses BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bdae-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2bdae-118">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="2bdae-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="2bdae-119">Mit diesem Befehl wird der Parameter *Force* nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="2bdae-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="2bdae-120">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="2bdae-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="2bdae-121">Wenn Sie den Befehl bestätigen, wird das vorhandene BLOB vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bdae-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="2bdae-122">Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2bdae-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="2bdae-123">Dieser Befehl ruft mit dem Cmdlet **Get-AzStorageContainer** den Container ab, der mit der Zeichenfolge ContosoUpload beginnt, und übergibt diesen BLOB an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bdae-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="2bdae-124">Der Befehl lädt die Datei mit dem Namen ContosoPlanning als Planning2015.</span><span class="sxs-lookup"><span data-stu-id="2bdae-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="2bdae-125">Beispiel 5: Hochladen einer Datei auf ein Page-BLOB mit Metadaten und PremiumPageBlobTier als P10</span><span class="sxs-lookup"><span data-stu-id="2bdae-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="2bdae-126">Der erste Befehl erstellt eine Hashtabelle, die Metadaten für einen BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variablen.</span><span class="sxs-lookup"><span data-stu-id="2bdae-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="2bdae-127">Der zweite Befehl lädt die Datei mit dem Namen ContosoPlanning in den Container mit dem Namen ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="2bdae-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="2bdae-128">Das BLOB enthält die Metadaten, die in $Metadata gespeichert sind, und hat PremiumPageBlobTier als P10.</span><span class="sxs-lookup"><span data-stu-id="2bdae-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="2bdae-129">Beispiel 6: Hochladen einer Datei in ein BLOB mit den angegebenen BLOB-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bdae-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="2bdae-130">Mit diesem Befehl wird die Datei mit dem Namen ContosoPlanning in den Container mit dem Namen ContosoUploads mit den angegebenen BLOB-Eigenschaften hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="2bdae-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="2bdae-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bdae-131">PARAMETERS</span></span>

### <span data-ttu-id="2bdae-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bdae-132">-AsJob</span></span>
<span data-ttu-id="2bdae-133">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2bdae-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2bdae-134">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2bdae-134">-Blob</span></span>
<span data-ttu-id="2bdae-135">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="2bdae-136">Mit diesem Cmdlet wird eine Datei in das Azure-Speicher-BLOB hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2bdae-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="2bdae-137">-Blobtype</span><span class="sxs-lookup"><span data-stu-id="2bdae-137">-BlobType</span></span>
<span data-ttu-id="2bdae-138">Gibt den Typ für das BLOB an, das vom Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="2bdae-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="2bdae-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2bdae-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2bdae-140">Blockieren</span><span class="sxs-lookup"><span data-stu-id="2bdae-140">Block</span></span>
- <span data-ttu-id="2bdae-141">Page der Standardwert ist Block.</span><span class="sxs-lookup"><span data-stu-id="2bdae-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="2bdae-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2bdae-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2bdae-143">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2bdae-144">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="2bdae-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2bdae-145">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2bdae-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2bdae-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2bdae-146">-CloudBlob</span></span>
<span data-ttu-id="2bdae-147">Gibt ein **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="2bdae-148">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2bdae-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bdae-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2bdae-149">-CloudBlobContainer</span></span>
<span data-ttu-id="2bdae-150">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2bdae-151">Mit diesem Cmdlet wird Inhalt in ein BLOB im Container hochgeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2bdae-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="2bdae-152">Verwenden Sie das Get-AzStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2bdae-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bdae-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2bdae-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2bdae-154">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2bdae-155">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="2bdae-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2bdae-156">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2bdae-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2bdae-157">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="2bdae-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2bdae-158">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2bdae-158">The default value is 10.</span></span>

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

### <span data-ttu-id="2bdae-159">-Container</span><span class="sxs-lookup"><span data-stu-id="2bdae-159">-Container</span></span>
<span data-ttu-id="2bdae-160">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-160">Specifies the name of a container.</span></span>
<span data-ttu-id="2bdae-161">Mit diesem Cmdlet wird eine Datei in ein BLOB im Container hochgeladen, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2bdae-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="2bdae-162">-Context</span><span class="sxs-lookup"><span data-stu-id="2bdae-162">-Context</span></span>
<span data-ttu-id="2bdae-163">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2bdae-164">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2bdae-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="2bdae-165">Wenn Sie einen aus einem SAS-Token ohne Leseberechtigung erstellten Speicherkontext verwenden möchten, benötigen Sie den Parameter Add-Force, um die Überprüfung der BLOB-Existenz zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="2bdae-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="2bdae-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bdae-166">-DefaultProfile</span></span>
<span data-ttu-id="2bdae-167">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bdae-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bdae-168">-Datei</span><span class="sxs-lookup"><span data-stu-id="2bdae-168">-File</span></span>
<span data-ttu-id="2bdae-169">Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bdae-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="2bdae-170">-Force</span><span class="sxs-lookup"><span data-stu-id="2bdae-170">-Force</span></span>
<span data-ttu-id="2bdae-171">Gibt an, dass mit diesem Cmdlet ein vorhandenes BLOB überschrieben wird, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="2bdae-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2bdae-172">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="2bdae-172">-Metadata</span></span>
<span data-ttu-id="2bdae-173">Gibt Metadaten für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="2bdae-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="2bdae-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="2bdae-175">Seiten-BLOB-Ebene</span><span class="sxs-lookup"><span data-stu-id="2bdae-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bdae-176">-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bdae-176">-Properties</span></span>
<span data-ttu-id="2bdae-177">Gibt Eigenschaften für das geuploadete BLOB an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="2bdae-178">Die unterstützten Eigenschaften sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="2bdae-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="2bdae-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2bdae-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2bdae-180">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2bdae-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2bdae-181">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2bdae-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2bdae-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2bdae-182">-Confirm</span></span>
<span data-ttu-id="2bdae-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bdae-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bdae-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bdae-184">-WhatIf</span></span>
<span data-ttu-id="2bdae-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bdae-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bdae-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2bdae-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bdae-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdae-187">CommonParameters</span></span>
<span data-ttu-id="2bdae-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bdae-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdae-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bdae-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdae-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bdae-190">INPUTS</span></span>

### <span data-ttu-id="2bdae-191">System. String</span><span class="sxs-lookup"><span data-stu-id="2bdae-191">System.String</span></span>

### <span data-ttu-id="2bdae-192">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2bdae-192">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2bdae-193">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2bdae-193">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2bdae-194">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2bdae-194">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2bdae-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bdae-195">OUTPUTS</span></span>

### <span data-ttu-id="2bdae-196">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2bdae-196">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2bdae-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bdae-197">NOTES</span></span>

## <span data-ttu-id="2bdae-198">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bdae-198">RELATED LINKS</span></span>

[<span data-ttu-id="2bdae-199">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2bdae-199">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="2bdae-200">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2bdae-200">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2bdae-201">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2bdae-201">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
