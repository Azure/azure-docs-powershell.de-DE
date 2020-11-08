---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165486"
---
# <span data-ttu-id="4ab27-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ab27-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="4ab27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ab27-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab27-103">Listet BLOBs in einem Container auf.</span><span class="sxs-lookup"><span data-stu-id="4ab27-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="4ab27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ab27-104">SYNTAX</span></span>

### <span data-ttu-id="4ab27-105">Blobname (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ab27-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ab27-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="4ab27-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4ab27-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="4ab27-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4ab27-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="4ab27-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4ab27-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ab27-109">DESCRIPTION</span></span>
<span data-ttu-id="4ab27-110">Das Cmdlet " **Get-AzStorageBlob** " listet BLOBs im angegebenen Container in einem Azure Storage-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="4ab27-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="4ab27-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ab27-111">EXAMPLES</span></span>

### <span data-ttu-id="4ab27-112">Beispiel 1: Abrufen eines BLOB nach BLOB-Namen</span><span class="sxs-lookup"><span data-stu-id="4ab27-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="4ab27-113">Dieser Befehl verwendet einen BLOB-Namen und Platzhalter, um einen BLOB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="4ab27-114">Beispiel 2: Abrufen von BLOBs in einem Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ab27-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="4ab27-115">Dieser Befehl verwendet die Pipeline, um alle BLOBs (einschließlich BLOBs im gelöschten Status) in einem Container abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="4ab27-116">Beispiel 3: Abrufen von BLOBs nach Namen Präfix</span><span class="sxs-lookup"><span data-stu-id="4ab27-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="4ab27-117">Dieser Befehl verwendet ein Namenspräfix, um BLOBs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="4ab27-118">Beispiel 4: Auflisten von BLOBs in mehreren Batches</span><span class="sxs-lookup"><span data-stu-id="4ab27-118">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="4ab27-119">In diesem Beispiel werden die *MaxCount* -und *ContinuationToken* -Parameter verwendet, um Azure-Speicher-BLOBs in mehreren Batches aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="4ab27-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="4ab27-120">Die ersten vier Befehle weisen Variablenwerte zu, die im Beispiel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="4ab27-121">Der fünfte Befehl gibt eine **do-while-** Anweisung an, die das Cmdlet **Get-AzStorageBlob** zum Abrufen von BLOBs verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ab27-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="4ab27-122">Die Anweisung enthält das Fortsetzungstoken, das in der $Token Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4ab27-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="4ab27-123">$Token ändert den Wert während der Ausführung der Schleife.</span><span class="sxs-lookup"><span data-stu-id="4ab27-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="4ab27-124">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="4ab27-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="4ab27-125">Der endgültige Befehl verwendet den Befehl **Echo** , um die Summe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="4ab27-126">Beispiel 5: Abrufen aller BLOBs in einem Container einschließlich BLOB-Version</span><span class="sxs-lookup"><span data-stu-id="4ab27-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="4ab27-127">Dieser Befehl ruft alle BLOBs in einem Container auf, einschließlich BLOB-Version.</span><span class="sxs-lookup"><span data-stu-id="4ab27-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="4ab27-128">Beispiel 6: Abrufen einer einzelnen BLOB-Version</span><span class="sxs-lookup"><span data-stu-id="4ab27-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="4ab27-129">Dieser Befehl ruft eine einzelne BLOBs-Verion mit Versions-Nr ab.</span><span class="sxs-lookup"><span data-stu-id="4ab27-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="4ab27-130">Beispiel 7: Abrufen eines einzelnen BLOB-Snapshots</span><span class="sxs-lookup"><span data-stu-id="4ab27-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="4ab27-131">Mit diesem Befehl wird ein einzelner BLOB-Snapshot mit Snapshotzeit abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="4ab27-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ab27-132">PARAMETERS</span></span>

### <span data-ttu-id="4ab27-133">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4ab27-133">-Blob</span></span>
<span data-ttu-id="4ab27-134">Gibt ein Name-oder Name-Muster an, das für eine Platzhaltersuche verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ab27-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="4ab27-135">Wenn kein BLOB-Name angegeben wird, listet das Cmdlet alle Blobs im angegebenen Container auf.</span><span class="sxs-lookup"><span data-stu-id="4ab27-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="4ab27-136">Wenn für diesen Parameter ein Wert angegeben wird, listet das Cmdlet alle Blobs mit Namen auf, die diesem Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="4ab27-137">Dieser Parameter unterstützt Platzhalter an einer beliebigen Stelle in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4ab27-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ab27-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4ab27-139">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4ab27-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4ab27-140">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="4ab27-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4ab27-141">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4ab27-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4ab27-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4ab27-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4ab27-143">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="4ab27-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4ab27-144">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4ab27-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4ab27-145">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4ab27-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4ab27-146">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4ab27-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4ab27-147">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4ab27-147">The default value is 10.</span></span>

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

### <span data-ttu-id="4ab27-148">-Container</span><span class="sxs-lookup"><span data-stu-id="4ab27-148">-Container</span></span>
<span data-ttu-id="4ab27-149">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="4ab27-149">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-150">-Context</span><span class="sxs-lookup"><span data-stu-id="4ab27-150">-Context</span></span>
<span data-ttu-id="4ab27-151">Gibt das Azure-Speicherkonto an, aus dem Sie eine Liste von BLOBs abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="4ab27-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="4ab27-152">Sie können das New-AzStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="4ab27-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="4ab27-153">-ContinuationToken</span></span>
<span data-ttu-id="4ab27-154">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="4ab27-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="4ab27-155">Verwenden Sie diesen Parameter und den *MaxCount* -Parameter, um BLOBs in mehreren Batches aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="4ab27-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab27-156">-DefaultProfile</span></span>
<span data-ttu-id="4ab27-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ab27-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ab27-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="4ab27-158">-IncludeDeleted</span></span>
<span data-ttu-id="4ab27-159">BLOB für gelöschte Elemente einbeziehen Standardmäßig wird BLOB nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4ab27-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="4ab27-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="4ab27-160">-IncludeVersion</span></span>
<span data-ttu-id="4ab27-161">BLOB-Versionen werden nur aufgelistet, wenn dieser Parameter vorhanden ist, standardmäßig erhalten BLOB keine BLOB-Versionen.</span><span class="sxs-lookup"><span data-stu-id="4ab27-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4ab27-162">-MaxCount</span></span>
<span data-ttu-id="4ab27-163">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4ab27-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="4ab27-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4ab27-164">-Prefix</span></span>
<span data-ttu-id="4ab27-165">Gibt ein Präfix für die BLOB-Namen an, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="4ab27-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="4ab27-166">Dieser Parameter unterstützt nicht die Verwendung regulärer Ausdrücke oder Platzhalterzeichen für die Suche.</span><span class="sxs-lookup"><span data-stu-id="4ab27-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="4ab27-167">Wenn der Container nur BLOBs mit dem Namen "My", "MyBlob1" und "MyBlob2" enthält und Sie "-prefix My \*" angeben, gibt das Cmdlet keine BLOBs zurück.</span><span class="sxs-lookup"><span data-stu-id="4ab27-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="4ab27-168">Wenn Sie jedoch "-prefix My" angeben, gibt das Cmdlet "My", "MyBlob1" und "MyBlob2" zurück.</span><span class="sxs-lookup"><span data-stu-id="4ab27-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ab27-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4ab27-170">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4ab27-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4ab27-171">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4ab27-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4ab27-172">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="4ab27-172">-SnapshotTime</span></span>
<span data-ttu-id="4ab27-173">BLOB-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="4ab27-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-174">-Versions-Nr</span><span class="sxs-lookup"><span data-stu-id="4ab27-174">-VersionId</span></span>
<span data-ttu-id="4ab27-175">BLOB-Versions-Nr</span><span class="sxs-lookup"><span data-stu-id="4ab27-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab27-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab27-176">CommonParameters</span></span>
<span data-ttu-id="4ab27-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab27-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab27-178">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab27-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab27-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ab27-179">INPUTS</span></span>

### <span data-ttu-id="4ab27-180">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab27-180">System.String</span></span>

### <span data-ttu-id="4ab27-181">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ab27-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ab27-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ab27-182">OUTPUTS</span></span>

### <span data-ttu-id="4ab27-183">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ab27-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="4ab27-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ab27-184">NOTES</span></span>

## <span data-ttu-id="4ab27-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ab27-185">RELATED LINKS</span></span>

[<span data-ttu-id="4ab27-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ab27-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="4ab27-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4ab27-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="4ab27-188">Satz-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4ab27-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


