---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: caaa36aa27cfb008fbbecced78f1fefc04958f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658728"
---
# <span data-ttu-id="2ae9b-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="2ae9b-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="2ae9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ae9b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae9b-103">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="2ae9b-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="2ae9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ae9b-104">SYNTAX</span></span>

### <span data-ttu-id="2ae9b-105">ContainerInstance (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ae9b-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae9b-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="2ae9b-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae9b-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="2ae9b-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae9b-108">Containername</span><span class="sxs-lookup"><span data-stu-id="2ae9b-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ae9b-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="2ae9b-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ae9b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ae9b-110">DESCRIPTION</span></span>
<span data-ttu-id="2ae9b-111">Starten eines inkrementellen Kopiervorgangs von einem Page BLOB-Snapshot zum angegebenen Zielseiten-BLOB</span><span class="sxs-lookup"><span data-stu-id="2ae9b-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="2ae9b-112">Weitere Informationen zu diesem Feature finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="2ae9b-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="2ae9b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ae9b-113">EXAMPLES</span></span>

### <span data-ttu-id="2ae9b-114">Beispiel 1: Starten des inkrementellen Kopiervorgangs nach BLOB-Name und Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="2ae9b-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="2ae9b-115">Mit diesem Befehl wird der inkrementelle Kopiervorgang nach BLOB-Name und Momentaufnahme Zeit gestartet.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="2ae9b-116">Beispiel 2: Starten des inkrementellen Kopiervorgangs mit dem Quell-URI</span><span class="sxs-lookup"><span data-stu-id="2ae9b-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="2ae9b-117">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe des Quell-URIs.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="2ae9b-118">Beispiel 3: Starten des inkrementellen Kopiervorgangs mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="2ae9b-119">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe der Container Pipeline von GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="2ae9b-120">Beispiel 4: Starten des inkrementellen Kopiervorgangs vom CloudPageBlob-Objekt in das Ziel-BLOB mit BLOB-Namen</span><span class="sxs-lookup"><span data-stu-id="2ae9b-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="2ae9b-121">Mit diesem Befehl wird der inkrementelle Kopiervorgang vom CloudPageBlob-Objekt in das Ziel-BLOB mit dem BLOB-Namen gestartet.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="2ae9b-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ae9b-122">PARAMETERS</span></span>

### <span data-ttu-id="2ae9b-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="2ae9b-123">-AbsoluteUri</span></span>
<span data-ttu-id="2ae9b-124">Absoluter URI für die Quelle.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-124">Absolute Uri to the source.</span></span> <span data-ttu-id="2ae9b-125">Beachten Sie, dass die Anmeldeinformationen im URI bereitgestellt werden sollten, wenn für die Quelle ein any erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="2ae9b-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ae9b-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2ae9b-127">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="2ae9b-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-128">-CloudBlob</span></span>
<span data-ttu-id="2ae9b-129">CloudBlob-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="2ae9b-130">Sie können Sie erstellen oder Get-AzStorageBlob Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae9b-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-131">-CloudBlobContainer</span></span>
<span data-ttu-id="2ae9b-132">CloudBlobContainer-Objekt aus Azure Storage-Client Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="2ae9b-133">Sie können Sie erstellen oder Get-AzStorageContainer Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ae9b-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2ae9b-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2ae9b-135">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="2ae9b-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-136">The default value is 10.</span></span>

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

### <span data-ttu-id="2ae9b-137">-Context</span><span class="sxs-lookup"><span data-stu-id="2ae9b-137">-Context</span></span>
<span data-ttu-id="2ae9b-138">Ursprünglicher Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-138">Source Azure Storage Context.</span></span> <span data-ttu-id="2ae9b-139">Sie können es über New-AzStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ae9b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae9b-140">-DefaultProfile</span></span>
<span data-ttu-id="2ae9b-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae9b-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-142">-DestBlob</span></span>
<span data-ttu-id="2ae9b-143">Ziel-BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="2ae9b-143">Destination blob name</span></span>

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

### <span data-ttu-id="2ae9b-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-144">-DestCloudBlob</span></span>
<span data-ttu-id="2ae9b-145">Ziel-CloudBlob-Objekt</span><span class="sxs-lookup"><span data-stu-id="2ae9b-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae9b-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-146">-DestContainer</span></span>
<span data-ttu-id="2ae9b-147">Name des Zielcontainers</span><span class="sxs-lookup"><span data-stu-id="2ae9b-147">Destination container name</span></span>

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

### <span data-ttu-id="2ae9b-148">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="2ae9b-148">-DestContext</span></span>
<span data-ttu-id="2ae9b-149">Ziel-Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="2ae9b-150">Sie können es über New-AzStorageContext-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ae9b-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ae9b-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2ae9b-152">Der Servertimeout für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="2ae9b-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-153">-SrcBlob</span></span>
<span data-ttu-id="2ae9b-154">BLOB-Name der Quellseite.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-154">Source page blob name.</span></span>

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

### <span data-ttu-id="2ae9b-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2ae9b-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="2ae9b-156">BLOB-Momentaufnahme Zeit für Quellseiten.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="2ae9b-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-157">-SrcContainer</span></span>
<span data-ttu-id="2ae9b-158">Name des Quellcontainers</span><span class="sxs-lookup"><span data-stu-id="2ae9b-158">Source Container name</span></span>

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

### <span data-ttu-id="2ae9b-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ae9b-159">-Confirm</span></span>
<span data-ttu-id="2ae9b-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae9b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae9b-161">-WhatIf</span></span>
<span data-ttu-id="2ae9b-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae9b-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae9b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae9b-164">CommonParameters</span></span>
<span data-ttu-id="2ae9b-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ae9b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae9b-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae9b-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae9b-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ae9b-167">INPUTS</span></span>

### <span data-ttu-id="2ae9b-168">Microsoft. WindowsAzure. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-168">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="2ae9b-169">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2ae9b-169">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="2ae9b-170">System. String</span><span class="sxs-lookup"><span data-stu-id="2ae9b-170">System.String</span></span>

### <span data-ttu-id="2ae9b-171">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ae9b-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2ae9b-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ae9b-172">OUTPUTS</span></span>

### <span data-ttu-id="2ae9b-173">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2ae9b-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2ae9b-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ae9b-174">NOTES</span></span>

## <span data-ttu-id="2ae9b-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ae9b-175">RELATED LINKS</span></span>
