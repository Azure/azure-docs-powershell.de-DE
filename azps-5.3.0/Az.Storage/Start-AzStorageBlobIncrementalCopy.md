---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376086"
---
# <span data-ttu-id="c0fb9-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="c0fb9-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="c0fb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fb9-103">Starten Sie einen inkrementellen Kopiervorgang von einer Seiten-BLOB-Momentaufnahme zum angegebenen Zielseiten-BLOB.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="c0fb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0fb9-104">SYNTAX</span></span>

### <span data-ttu-id="c0fb9-105">ContainerInstance (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0fb9-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fb9-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="c0fb9-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fb9-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="c0fb9-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fb9-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="c0fb9-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fb9-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="c0fb9-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0fb9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0fb9-110">DESCRIPTION</span></span>
<span data-ttu-id="c0fb9-111">Starten Sie einen inkrementellen Kopiervorgang von einer Seiten-BLOB-Momentaufnahme zum angegebenen Zielseiten-BLOB.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="c0fb9-112">Weitere Details zu diesem Feature finden Sie in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="c0fb9-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="c0fb9-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0fb9-113">EXAMPLES</span></span>

### <span data-ttu-id="c0fb9-114">Beispiel 1: Starten des inkrementellen Kopiervorgangs nach BLOB-Name und Momentaufnahmezeit</span><span class="sxs-lookup"><span data-stu-id="c0fb9-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="c0fb9-115">Dieser Befehl startet den inkrementellen Kopiervorgang nach BLOB-Name und Momentaufnahmezeit</span><span class="sxs-lookup"><span data-stu-id="c0fb9-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="c0fb9-116">Beispiel 2: Starten des inkrementellen Kopiervorgangs mithilfe des Quell-URI</span><span class="sxs-lookup"><span data-stu-id="c0fb9-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="c0fb9-117">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe des Quell-URI.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="c0fb9-118">Beispiel 3: Starten des inkrementellen Kopiervorgangs mithilfe der Containerpipeline aus GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c0fb9-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="c0fb9-119">Dieser Befehl startet den inkrementellen Kopiervorgang mithilfe der Containerpipeline aus "GetAzureStorageContainer".</span><span class="sxs-lookup"><span data-stu-id="c0fb9-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="c0fb9-120">Beispiel 4: Starten des inkrementellen Kopiervorgangs vom CloudPageBlob-Objekt zum Ziel-BLOB mit BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="c0fb9-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="c0fb9-121">Dieser Befehl startet den inkrementellen Kopiervorgang vom CloudPageBlob-Objekt zum Ziel-BLOB mit BLOB-Namen.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="c0fb9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0fb9-122">PARAMETERS</span></span>

### <span data-ttu-id="c0fb9-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="c0fb9-123">-AbsoluteUri</span></span>
<span data-ttu-id="c0fb9-124">Absoluter URI für die Quelle.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-124">Absolute Uri to the source.</span></span> <span data-ttu-id="c0fb9-125">Beachten Sie, dass die Anmeldeinformationen im URI angegeben werden sollten, wenn die Quelle eine erfordert.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="c0fb9-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0fb9-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c0fb9-127">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="c0fb9-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-128">-CloudBlob</span></span>
<span data-ttu-id="c0fb9-129">CloudBlob-Objekt aus der Azure Storage Client-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="c0fb9-130">Sie können das Cmdlet erstellen oder Get-AzStorageBlob verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fb9-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c0fb9-131">-CloudBlobContainer</span></span>
<span data-ttu-id="c0fb9-132">CloudBlobContainer-Objekt aus der Azure Storage Client-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="c0fb9-133">Sie können das Cmdlet erstellen oder Get-AzStorageContainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="c0fb9-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c0fb9-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c0fb9-135">Die Gesamtzahl paralleler asynchroner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="c0fb9-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-136">The default value is 10.</span></span>

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

### <span data-ttu-id="c0fb9-137">-Context</span><span class="sxs-lookup"><span data-stu-id="c0fb9-137">-Context</span></span>
<span data-ttu-id="c0fb9-138">Azure Storage-Quellkontext.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-138">Source Azure Storage Context.</span></span> <span data-ttu-id="c0fb9-139">Sie können sie über New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c0fb9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fb9-140">-DefaultProfile</span></span>
<span data-ttu-id="c0fb9-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0fb9-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-142">-DestBlob</span></span>
<span data-ttu-id="c0fb9-143">Ziel-BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="c0fb9-143">Destination blob name</span></span>

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

### <span data-ttu-id="c0fb9-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-144">-DestCloudBlob</span></span>
<span data-ttu-id="c0fb9-145">Ziel-CloudBlob-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0fb9-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fb9-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="c0fb9-146">-DestContainer</span></span>
<span data-ttu-id="c0fb9-147">Zielcontainername</span><span class="sxs-lookup"><span data-stu-id="c0fb9-147">Destination container name</span></span>

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

### <span data-ttu-id="c0fb9-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="c0fb9-148">-DestContext</span></span>
<span data-ttu-id="c0fb9-149">Azure Storage-Zielkontext.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="c0fb9-150">Sie können sie über New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c0fb9-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c0fb9-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c0fb9-152">Die Serverzeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="c0fb9-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-153">-SrcBlob</span></span>
<span data-ttu-id="c0fb9-154">Name des Blobs der Quellseite.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-154">Source page blob name.</span></span>

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

### <span data-ttu-id="c0fb9-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c0fb9-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="c0fb9-156">Quellseite-BLOB-Momentaufnahmezeit.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="c0fb9-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="c0fb9-157">-SrcContainer</span></span>
<span data-ttu-id="c0fb9-158">Name des Quellcontainers</span><span class="sxs-lookup"><span data-stu-id="c0fb9-158">Source Container name</span></span>

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

### <span data-ttu-id="c0fb9-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0fb9-159">-Confirm</span></span>
<span data-ttu-id="c0fb9-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0fb9-161">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0fb9-161">-WhatIf</span></span>
<span data-ttu-id="c0fb9-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0fb9-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0fb9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fb9-164">CommonParameters</span></span>
<span data-ttu-id="c0fb9-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fb9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fb9-166">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0fb9-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fb9-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0fb9-167">INPUTS</span></span>

### <span data-ttu-id="c0fb9-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="c0fb9-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="c0fb9-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="c0fb9-170">System.String</span><span class="sxs-lookup"><span data-stu-id="c0fb9-170">System.String</span></span>

### <span data-ttu-id="c0fb9-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c0fb9-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c0fb9-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0fb9-172">OUTPUTS</span></span>

### <span data-ttu-id="c0fb9-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c0fb9-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="c0fb9-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0fb9-174">NOTES</span></span>

## <span data-ttu-id="c0fb9-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0fb9-175">RELATED LINKS</span></span>
