---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460171"
---
# <span data-ttu-id="a0476-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0476-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="a0476-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0476-102">SYNOPSIS</span></span>
<span data-ttu-id="a0476-103">Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="a0476-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a0476-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0476-104">SYNTAX</span></span>

### <span data-ttu-id="a0476-105">SendManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0476-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0476-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a0476-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0476-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a0476-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0476-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0476-108">DESCRIPTION</span></span>
<span data-ttu-id="a0476-109">Das **Cmdlet "Set-AzStorageBlobContent"** lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="a0476-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a0476-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0476-110">EXAMPLES</span></span>

### <span data-ttu-id="a0476-111">Beispiel 1: Hochladen einer benannten Datei</span><span class="sxs-lookup"><span data-stu-id="a0476-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="a0476-112">Mit diesem Befehl wird die Datei mit dem Namen "PlanningData" in ein BLOB namens "Planning2015" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="a0476-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="a0476-113">Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="a0476-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="a0476-114">Dieser Befehl verwendet das core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern zu erhalten, und übergibt sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0476-115">Das **Cmdlet "Set-AzStorageBlobContent"** lädt die Dateien in den Container "ContosoUploads" hoch.</span><span class="sxs-lookup"><span data-stu-id="a0476-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="a0476-116">Beispiel 3: Überschreiben eines vorhandenen BLOB</span><span class="sxs-lookup"><span data-stu-id="a0476-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="a0476-117">Dieser Befehl ruft das BLOB namens Planning2015 im Container "ContosoUploads" mithilfe des Cmdlets Get-AzStorageBlob ab und übergibt dieses BLOB dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a0476-118">Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.</span><span class="sxs-lookup"><span data-stu-id="a0476-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="a0476-119">Dieser Befehl gibt den Parameter *"Force" nicht* an.</span><span class="sxs-lookup"><span data-stu-id="a0476-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="a0476-120">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="a0476-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="a0476-121">Wenn Sie den Befehl bestätigen, überschreibt das Cmdlet das vorhandene BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0476-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="a0476-122">Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="a0476-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="a0476-123">Dieser Befehl ruft den Container ab, der mit der Zeichenfolge "ContosoUpload" mit dem **Cmdlet "Get-AzStorageContainer"** beginnt, und übergibt dieses BLOB dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a0476-124">Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.</span><span class="sxs-lookup"><span data-stu-id="a0476-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="a0476-125">Beispiel 5: Hochladen einer Datei auf den Seiten-BLOB mit Metadaten und PremiumPageBlobTier als P10</span><span class="sxs-lookup"><span data-stu-id="a0476-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="a0476-126">Der erste Befehl erstellt eine Hashtabelle, die Metadaten für ein BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variable.</span><span class="sxs-lookup"><span data-stu-id="a0476-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="a0476-127">Mit dem zweiten Befehl wird die Datei mit dem Namen "ContosoPlanning" in den Container "ContosoUploads" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="a0476-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="a0476-128">Das BLOB enthält die metadaten, die in $Metadata gespeichert sind, und verfügt über PremiumPageBlobTier als P10.</span><span class="sxs-lookup"><span data-stu-id="a0476-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="a0476-129">Beispiel 6: Hochladen einer Datei in blob mit angegebenen BLOB-Eigenschaften und Festlegen von "StandardBlobTier" auf "Cool"</span><span class="sxs-lookup"><span data-stu-id="a0476-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="a0476-130">Mit diesem Befehl wird die Datei c:\temp\index.html in den Container namens "contosouploads" mit angegebenen BLOB-Eigenschaften hochgeladen und "StandardBlobTier" auf "Cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0476-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="a0476-131">Mit diesem Befehl wird der ContentType-Wert von der [System.Web.MimeMapping]::GetMimeMapping()-API auf BLOB-Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0476-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="a0476-132">Beispiel 7: Hochladen einer Datei in ein BLOB mit Verschlüsselungsbereich</span><span class="sxs-lookup"><span data-stu-id="a0476-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="a0476-133">Mit diesem Befehl wird eine Datei in ein BLOB mit Verschlüsselungsbereich hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="a0476-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="a0476-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0476-134">PARAMETERS</span></span>

### <span data-ttu-id="a0476-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0476-135">-AsJob</span></span>
<span data-ttu-id="a0476-136">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="a0476-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a0476-137">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a0476-137">-Blob</span></span>
<span data-ttu-id="a0476-138">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a0476-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="a0476-139">Dieses Cmdlet lädt eine Datei in das Azure Storage-BLOB hoch, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a0476-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0476-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="a0476-140">-BlobType</span></span>
<span data-ttu-id="a0476-141">Gibt den Typ für den BLOB an, den dieses Cmdlet hochlädt.</span><span class="sxs-lookup"><span data-stu-id="a0476-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="a0476-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a0476-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a0476-143">Blockieren</span><span class="sxs-lookup"><span data-stu-id="a0476-143">Block</span></span>
- <span data-ttu-id="a0476-144">Seite</span><span class="sxs-lookup"><span data-stu-id="a0476-144">Page</span></span>
- <span data-ttu-id="a0476-145">Anfügen Der Standardwert ist "Block".</span><span class="sxs-lookup"><span data-stu-id="a0476-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="a0476-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0476-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a0476-147">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="a0476-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a0476-148">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0476-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a0476-149">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a0476-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a0476-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a0476-150">-CloudBlob</span></span>
<span data-ttu-id="a0476-151">Gibt ein **"CloudBlob"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a0476-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="a0476-152">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0476-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a0476-153">-CloudBlobContainer</span></span>
<span data-ttu-id="a0476-154">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="a0476-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a0476-155">Dieses Cmdlet lädt Inhalte in ein BLOB im Container hoch, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a0476-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a0476-156">Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0476-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a0476-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a0476-158">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="a0476-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a0476-159">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="a0476-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a0476-160">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a0476-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a0476-161">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="a0476-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a0476-162">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a0476-162">The default value is 10.</span></span>

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

### <span data-ttu-id="a0476-163">-Container</span><span class="sxs-lookup"><span data-stu-id="a0476-163">-Container</span></span>
<span data-ttu-id="a0476-164">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="a0476-164">Specifies the name of a container.</span></span>
<span data-ttu-id="a0476-165">Dieses Cmdlet lädt eine Datei in ein BLOB im Container hoch, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a0476-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0476-166">-Context</span><span class="sxs-lookup"><span data-stu-id="a0476-166">-Context</span></span>
<span data-ttu-id="a0476-167">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a0476-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a0476-168">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0476-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="a0476-169">Wenn Sie einen Speicherkontext verwenden möchten, der aus einem SAS-Token ohne Leseberechtigung erstellt wurde, müssen Sie den Parameter "add -Force" verwenden, um das Vorhandensein von Blobs zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="a0476-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="a0476-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0476-170">-DefaultProfile</span></span>
<span data-ttu-id="a0476-171">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0476-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0476-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a0476-172">-EncryptionScope</span></span>
<span data-ttu-id="a0476-173">Verschlüsselungsbereich, der verwendet wird, wenn Anforderungen an das BLOB erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0476-173">Encryption scope to be used when making requests to the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0476-174">-File</span><span class="sxs-lookup"><span data-stu-id="a0476-174">-File</span></span>
<span data-ttu-id="a0476-175">Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0476-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="a0476-176">-Force</span><span class="sxs-lookup"><span data-stu-id="a0476-176">-Force</span></span>
<span data-ttu-id="a0476-177">Gibt an, dass dieses Cmdlet ein vorhandenes BLOB überschreibt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a0476-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a0476-178">-Metadata</span><span class="sxs-lookup"><span data-stu-id="a0476-178">-Metadata</span></span>
<span data-ttu-id="a0476-179">Gibt Metadaten für den hochgeladenen BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a0476-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="a0476-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="a0476-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="a0476-181">Page Blob Tier</span><span class="sxs-lookup"><span data-stu-id="a0476-181">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0476-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="a0476-182">-Properties</span></span>
<span data-ttu-id="a0476-183">Gibt Eigenschaften für den hochgeladenen BLOB an.</span><span class="sxs-lookup"><span data-stu-id="a0476-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="a0476-184">Die unterstützten Eigenschaften sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="a0476-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="a0476-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a0476-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a0476-186">Gibt das intervallseitige Dienstzeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="a0476-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a0476-187">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a0476-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a0476-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="a0476-188">-StandardBlobTier</span></span>
<span data-ttu-id="a0476-189">Block BLOB Tier, gültige Werte sind Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="a0476-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="a0476-190">Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="a0476-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="a0476-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0476-191">-Confirm</span></span>
<span data-ttu-id="a0476-192">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0476-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0476-193">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0476-193">-WhatIf</span></span>
<span data-ttu-id="a0476-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0476-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0476-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0476-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0476-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0476-196">CommonParameters</span></span>
<span data-ttu-id="a0476-197">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0476-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0476-198">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0476-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0476-199">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0476-199">INPUTS</span></span>

### <span data-ttu-id="a0476-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a0476-200">System.String</span></span>

### <span data-ttu-id="a0476-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a0476-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a0476-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a0476-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a0476-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a0476-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0476-204">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0476-204">OUTPUTS</span></span>

### <span data-ttu-id="a0476-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0476-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a0476-206">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0476-206">NOTES</span></span>

## <span data-ttu-id="a0476-207">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0476-207">RELATED LINKS</span></span>

[<span data-ttu-id="a0476-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0476-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a0476-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0476-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a0476-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a0476-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
