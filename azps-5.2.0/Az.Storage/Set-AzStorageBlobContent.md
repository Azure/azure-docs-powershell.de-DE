---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d99bde2839e1b4e91d6299cd47319827a57f4f33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303320"
---
# <span data-ttu-id="c68ef-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c68ef-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="c68ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c68ef-103">Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="c68ef-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="c68ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c68ef-104">SYNTAX</span></span>

### <span data-ttu-id="c68ef-105">SendManual (Standard)</span><span class="sxs-lookup"><span data-stu-id="c68ef-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c68ef-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c68ef-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c68ef-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c68ef-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c68ef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c68ef-108">DESCRIPTION</span></span>
<span data-ttu-id="c68ef-109">Das **Cmdlet "Set-AzStorageBlobContent"** lädt eine lokale Datei in ein Azure Storage-BLOB hoch.</span><span class="sxs-lookup"><span data-stu-id="c68ef-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="c68ef-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c68ef-110">EXAMPLES</span></span>

### <span data-ttu-id="c68ef-111">Beispiel 1: Hochladen einer benannten Datei</span><span class="sxs-lookup"><span data-stu-id="c68ef-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="c68ef-112">Mit diesem Befehl wird die Datei mit dem Namen "PlanningData" in ein BLOB namens "Planning2015" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="c68ef-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="c68ef-113">Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="c68ef-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="c68ef-114">Dieser Befehl verwendet das core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern zu erhalten, und übergibt sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c68ef-115">Das **Cmdlet "Set-AzStorageBlobContent"** lädt die Dateien in den Container "ContosoUploads" hoch.</span><span class="sxs-lookup"><span data-stu-id="c68ef-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="c68ef-116">Beispiel 3: Überschreiben eines vorhandenen BLOB</span><span class="sxs-lookup"><span data-stu-id="c68ef-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="c68ef-117">Dieser Befehl ruft das BLOB namens Planning2015 im Container "ContosoUploads" mithilfe des Cmdlets Get-AzStorageBlob ab und übergibt dieses BLOB dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="c68ef-118">Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.</span><span class="sxs-lookup"><span data-stu-id="c68ef-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="c68ef-119">Dieser Befehl gibt den Parameter *"Force" nicht* an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="c68ef-120">Der Befehl fordert Sie zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="c68ef-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="c68ef-121">Wenn Sie den Befehl bestätigen, überschreibt das Cmdlet das vorhandene BLOB.</span><span class="sxs-lookup"><span data-stu-id="c68ef-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="c68ef-122">Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="c68ef-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="c68ef-123">Dieser Befehl ruft den Container ab, der mit der Zeichenfolge "ContosoUpload" mit dem **Cmdlet "Get-AzStorageContainer"** beginnt, und übergibt dieses BLOB dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="c68ef-124">Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.</span><span class="sxs-lookup"><span data-stu-id="c68ef-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="c68ef-125">Beispiel 5: Hochladen einer Datei auf den Seiten-BLOB mit Metadaten und PremiumPageBlobTier als P10</span><span class="sxs-lookup"><span data-stu-id="c68ef-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="c68ef-126">Der erste Befehl erstellt eine Hashtabelle, die Metadaten für ein BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variable.</span><span class="sxs-lookup"><span data-stu-id="c68ef-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="c68ef-127">Mit dem zweiten Befehl wird die Datei mit dem Namen "ContosoPlanning" in den Container "ContosoUploads" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="c68ef-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="c68ef-128">Das BLOB enthält die metadaten, die in $Metadata gespeichert sind, und verfügt über PremiumPageBlobTier als P10.</span><span class="sxs-lookup"><span data-stu-id="c68ef-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="c68ef-129">Beispiel 6: Hochladen einer Datei in blob mit angegebenen BLOB-Eigenschaften und Festlegen von "StandardBlobTier" auf "Cool"</span><span class="sxs-lookup"><span data-stu-id="c68ef-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="c68ef-130">Dieser Befehl lädt die Datei c:\temp\index.html in den Container mit dem Namen "contosouploads" mit angegebenen BLOB-Eigenschaften hoch, und legen Sie "StandardBlobTier" als "Cool" fest.</span><span class="sxs-lookup"><span data-stu-id="c68ef-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="c68ef-131">Mit diesem Befehl wird der ContentType-Wert von der [System.Web.MimeMapping]::GetMimeMapping()-API auf BLOB-Eigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="c68ef-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c68ef-132">PARAMETERS</span></span>

### <span data-ttu-id="c68ef-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c68ef-133">-AsJob</span></span>
<span data-ttu-id="c68ef-134">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="c68ef-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c68ef-135">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c68ef-135">-Blob</span></span>
<span data-ttu-id="c68ef-136">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="c68ef-137">Dieses Cmdlet lädt eine Datei in das Azure Storage-BLOB hoch, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="c68ef-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="c68ef-138">-BlobType</span></span>
<span data-ttu-id="c68ef-139">Gibt den Typ für den BLOB an, den dieses Cmdlet hochlädt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="c68ef-140">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="c68ef-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c68ef-141">Blockieren</span><span class="sxs-lookup"><span data-stu-id="c68ef-141">Block</span></span>
- <span data-ttu-id="c68ef-142">Seite</span><span class="sxs-lookup"><span data-stu-id="c68ef-142">Page</span></span>
- <span data-ttu-id="c68ef-143">Anfügen Der Standardwert ist "Block".</span><span class="sxs-lookup"><span data-stu-id="c68ef-143">Append The default value is Block.</span></span>

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

### <span data-ttu-id="c68ef-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c68ef-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c68ef-145">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c68ef-146">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c68ef-147">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c68ef-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c68ef-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c68ef-148">-CloudBlob</span></span>
<span data-ttu-id="c68ef-149">Gibt ein **CloudBlob-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-149">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="c68ef-150">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="c68ef-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c68ef-151">-CloudBlobContainer</span></span>
<span data-ttu-id="c68ef-152">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="c68ef-153">Dieses Cmdlet lädt Inhalte in ein BLOB im Container hoch, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-153">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="c68ef-154">Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="c68ef-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c68ef-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c68ef-156">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c68ef-157">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="c68ef-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c68ef-158">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="c68ef-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c68ef-159">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="c68ef-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c68ef-160">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="c68ef-160">The default value is 10.</span></span>

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

### <span data-ttu-id="c68ef-161">-Container</span><span class="sxs-lookup"><span data-stu-id="c68ef-161">-Container</span></span>
<span data-ttu-id="c68ef-162">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-162">Specifies the name of a container.</span></span>
<span data-ttu-id="c68ef-163">Dieses Cmdlet lädt eine Datei in ein BLOB im Container hoch, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-163">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="c68ef-164">-Context</span><span class="sxs-lookup"><span data-stu-id="c68ef-164">-Context</span></span>
<span data-ttu-id="c68ef-165">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-165">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c68ef-166">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c68ef-166">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c68ef-167">Wenn Sie einen Speicherkontext verwenden möchten, der aus einem SAS-Token ohne Leseberechtigung erstellt wurde, müssen Sie den Parameter "add -Force" verwenden, um das Vorhandensein von Blobs zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="c68ef-167">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="c68ef-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68ef-168">-DefaultProfile</span></span>
<span data-ttu-id="c68ef-169">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c68ef-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68ef-170">-File</span><span class="sxs-lookup"><span data-stu-id="c68ef-170">-File</span></span>
<span data-ttu-id="c68ef-171">Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c68ef-171">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="c68ef-172">-Force</span><span class="sxs-lookup"><span data-stu-id="c68ef-172">-Force</span></span>
<span data-ttu-id="c68ef-173">Gibt an, dass dieses Cmdlet ein vorhandenes BLOB überschreibt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c68ef-173">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c68ef-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c68ef-174">-Metadata</span></span>
<span data-ttu-id="c68ef-175">Gibt Die Metadaten für den hochgeladenen BLOB an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-175">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="c68ef-176">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="c68ef-176">-PremiumPageBlobTier</span></span>
<span data-ttu-id="c68ef-177">Page Blob Tier</span><span class="sxs-lookup"><span data-stu-id="c68ef-177">Page Blob Tier</span></span>

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

### <span data-ttu-id="c68ef-178">-Properties</span><span class="sxs-lookup"><span data-stu-id="c68ef-178">-Properties</span></span>
<span data-ttu-id="c68ef-179">Gibt Eigenschaften für den hochgeladenen BLOB an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-179">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="c68ef-180">Die unterstützten Eigenschaften sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="c68ef-180">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="c68ef-181">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c68ef-181">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c68ef-182">Gibt das intervallseitige Dienstzeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c68ef-182">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c68ef-183">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c68ef-183">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c68ef-184">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="c68ef-184">-StandardBlobTier</span></span>
<span data-ttu-id="c68ef-185">Block BLOB Tier, gültige Werte sind Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="c68ef-185">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="c68ef-186">Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="c68ef-186">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="c68ef-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c68ef-187">-Confirm</span></span>
<span data-ttu-id="c68ef-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c68ef-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68ef-189">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c68ef-189">-WhatIf</span></span>
<span data-ttu-id="c68ef-190">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c68ef-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c68ef-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c68ef-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68ef-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68ef-192">CommonParameters</span></span>
<span data-ttu-id="c68ef-193">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68ef-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68ef-194">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68ef-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68ef-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c68ef-195">INPUTS</span></span>

### <span data-ttu-id="c68ef-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c68ef-196">System.String</span></span>

### <span data-ttu-id="c68ef-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c68ef-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c68ef-198">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c68ef-198">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c68ef-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c68ef-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c68ef-200">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c68ef-200">OUTPUTS</span></span>

### <span data-ttu-id="c68ef-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c68ef-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c68ef-202">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c68ef-202">NOTES</span></span>

## <span data-ttu-id="c68ef-203">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c68ef-203">RELATED LINKS</span></span>

[<span data-ttu-id="c68ef-204">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c68ef-204">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="c68ef-205">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c68ef-205">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c68ef-206">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c68ef-206">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
