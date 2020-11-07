---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 28d0c33a1aa74b5c5f69670622cc12c48810906f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842835"
---
# <span data-ttu-id="b9122-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="b9122-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="b9122-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9122-102">SYNOPSIS</span></span>
<span data-ttu-id="b9122-103">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="b9122-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="b9122-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9122-104">SYNTAX</span></span>

### <span data-ttu-id="b9122-105">ContainerInstance (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9122-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9122-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="b9122-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9122-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="b9122-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9122-108">Containername</span><span class="sxs-lookup"><span data-stu-id="b9122-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9122-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="b9122-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9122-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9122-110">DESCRIPTION</span></span>
<span data-ttu-id="b9122-111">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="b9122-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="b9122-112">Weitere Informationen zu diesem Feature finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="b9122-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="b9122-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9122-113">EXAMPLES</span></span>

### <span data-ttu-id="b9122-114">Beispiel 1: Starten des inkrementellen Kopiervorgangs nach BLOB-Name und Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="b9122-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b9122-115">Mit diesem Befehl wird der inkrementelle Kopiervorgang nach BLOB-Name und Momentaufnahme Zeit gestartet.</span><span class="sxs-lookup"><span data-stu-id="b9122-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="b9122-116">Beispiel 2: Starten des inkrementellen Kopiervorgangs mit dem Quell-URI</span><span class="sxs-lookup"><span data-stu-id="b9122-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="b9122-117">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe des Quell-URIs.</span><span class="sxs-lookup"><span data-stu-id="b9122-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="b9122-118">Beispiel 3: Starten des inkrementellen Kopiervorgangs mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="b9122-119">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="b9122-120">Beispiel 4: Starten des inkrementellen Kopiervorgangs vom CloudPageBlob-Objekt in das Ziel-BLOB mit BLOB-Namen</span><span class="sxs-lookup"><span data-stu-id="b9122-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="b9122-121">Mit diesem Befehl wird der inkrementelle Kopiervorgang vom CloudPageBlob-Objekt in das Ziel-BLOB mit dem BLOB-Namen gestartet.</span><span class="sxs-lookup"><span data-stu-id="b9122-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="b9122-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9122-122">PARAMETERS</span></span>

### <span data-ttu-id="b9122-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="b9122-123">-AbsoluteUri</span></span>
<span data-ttu-id="b9122-124">Absoluter URI für die Quelle.</span><span class="sxs-lookup"><span data-stu-id="b9122-124">Absolute Uri to the source.</span></span> <span data-ttu-id="b9122-125">Beachten Sie, dass die Anmeldeinformationen im URI bereitgestellt werden sollten, wenn für die Quelle ein any erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9122-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="b9122-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b9122-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b9122-127">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b9122-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="b9122-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-128">-CloudBlob</span></span>
<span data-ttu-id="b9122-129">CloudBlob-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b9122-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="b9122-130">Sie können Sie erstellen oder Get-AzStorageBlob Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9122-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-131">-CloudBlobContainer</span></span>
<span data-ttu-id="b9122-132">CloudBlobContainer-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="b9122-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="b9122-133">Sie können Sie erstellen oder Get-AzStorageContainer Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9122-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b9122-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b9122-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b9122-135">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="b9122-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="b9122-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b9122-136">The default value is 10.</span></span>

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

### <span data-ttu-id="b9122-137">-Context</span><span class="sxs-lookup"><span data-stu-id="b9122-137">-Context</span></span>
<span data-ttu-id="b9122-138">Ursprünglicher Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="b9122-138">Source Azure Storage Context.</span></span> <span data-ttu-id="b9122-139">Sie können es über New-AzStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9122-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
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

### <span data-ttu-id="b9122-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9122-140">-DefaultProfile</span></span>
<span data-ttu-id="b9122-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9122-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9122-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-142">-DestBlob</span></span>
<span data-ttu-id="b9122-143">Ziel-BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="b9122-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
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

### <span data-ttu-id="b9122-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-144">-DestCloudBlob</span></span>
<span data-ttu-id="b9122-145">Ziel-CloudBlob-Objekt</span><span class="sxs-lookup"><span data-stu-id="b9122-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-146">-DestContainer</span></span>
<span data-ttu-id="b9122-147">Name des Zielcontainers</span><span class="sxs-lookup"><span data-stu-id="b9122-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-148">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="b9122-148">-DestContext</span></span>
<span data-ttu-id="b9122-149">Ziel-Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="b9122-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="b9122-150">Sie können es über New-AzStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9122-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b9122-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b9122-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b9122-152">Der Servertimeout für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b9122-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="b9122-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-153">-SrcBlob</span></span>
<span data-ttu-id="b9122-154">BLOB-Name der Quellseite.</span><span class="sxs-lookup"><span data-stu-id="b9122-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="b9122-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="b9122-156">BLOB-Momentaufnahme Zeit für Quellseiten.</span><span class="sxs-lookup"><span data-stu-id="b9122-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-157">-SrcContainer</span></span>
<span data-ttu-id="b9122-158">Name des Quellcontainers</span><span class="sxs-lookup"><span data-stu-id="b9122-158">Source Container name</span></span>

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

### <span data-ttu-id="b9122-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9122-159">-Confirm</span></span>
<span data-ttu-id="b9122-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9122-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9122-161">-WhatIf</span></span>
<span data-ttu-id="b9122-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9122-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9122-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9122-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9122-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9122-164">CommonParameters</span></span>
<span data-ttu-id="b9122-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9122-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9122-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9122-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9122-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9122-167">INPUTS</span></span>

### <span data-ttu-id="b9122-168">Microsoft. WindowsAz. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-168">Microsoft.WindowsAz.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="b9122-169">Microsoft. WindowsAz. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b9122-169">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b9122-170">System. String</span><span class="sxs-lookup"><span data-stu-id="b9122-170">System.String</span></span>

### <span data-ttu-id="b9122-171">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b9122-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b9122-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9122-172">OUTPUTS</span></span>

### <span data-ttu-id="b9122-173">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b9122-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b9122-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9122-174">NOTES</span></span>

## <span data-ttu-id="b9122-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9122-175">RELATED LINKS</span></span>
