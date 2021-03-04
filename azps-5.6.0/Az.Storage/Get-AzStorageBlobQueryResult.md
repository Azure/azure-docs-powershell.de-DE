---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: 7a790610d9ff3334494276eee7bb85af5b9ba3fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944602"
---
# <span data-ttu-id="56f08-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="56f08-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="56f08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f08-102">SYNOPSIS</span></span>
<span data-ttu-id="56f08-103">Wendet eine einfache strukturierte Abfragesprache (SQL) auf den Inhalt eines Blobs an, und speichern Sie nur die abgefragte Teilmenge der Daten in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="56f08-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="56f08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="56f08-104">SYNTAX</span></span>

### <span data-ttu-id="56f08-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="56f08-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56f08-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="56f08-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56f08-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="56f08-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56f08-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56f08-108">DESCRIPTION</span></span>
<span data-ttu-id="56f08-109">Das **Get-AzStorageBlobQueryResult-Cmdlet** wendet eine einfache strukturierte Abfragesprache (SQL)-Anweisung auf den Inhalt eines Blobs an, und speichern Sie die abgefragte Teilmenge der Daten in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="56f08-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="56f08-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="56f08-110">EXAMPLES</span></span>

### <span data-ttu-id="56f08-111">Beispiel 1: Abfragen eines Blobs</span><span class="sxs-lookup"><span data-stu-id="56f08-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="56f08-112">Mit diesem Befehl wird ein Blob erfolgreich mit der Eingabekonfiguration als CSV und der Ausgabekonfiguration als json abgefragt, und die Ausgabe wird in der lokalen Datei "c:\resultfile.json" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="56f08-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="56f08-113">Beispiel 2: Abfragen einer Blobmomentaufnahme</span><span class="sxs-lookup"><span data-stu-id="56f08-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="56f08-114">Dieser Befehl ruft zuerst ein Blobobjekt für die Blobmomentaufnahme ab, fragt dann die Blobmomentaufnahme ab und zeigt den Abfragefehler des Ergebnisses an.</span><span class="sxs-lookup"><span data-stu-id="56f08-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="56f08-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="56f08-115">PARAMETERS</span></span>

### <span data-ttu-id="56f08-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="56f08-116">-Blob</span></span>
<span data-ttu-id="56f08-117">Blobname</span><span class="sxs-lookup"><span data-stu-id="56f08-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="56f08-118">-BlobBaseClient</span></span>
<span data-ttu-id="56f08-119">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="56f08-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="56f08-120">-BlobContainerClient</span></span>
<span data-ttu-id="56f08-121">BlobContainerClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="56f08-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="56f08-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="56f08-123">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="56f08-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="56f08-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="56f08-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="56f08-125">Die Gesamtanzahl gleichzeitiger asynchroner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="56f08-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="56f08-126">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="56f08-126">The default value is 10.</span></span>

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

### <span data-ttu-id="56f08-127">-Container</span><span class="sxs-lookup"><span data-stu-id="56f08-127">-Container</span></span>
<span data-ttu-id="56f08-128">Containername</span><span class="sxs-lookup"><span data-stu-id="56f08-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-129">-Context</span><span class="sxs-lookup"><span data-stu-id="56f08-129">-Context</span></span>
<span data-ttu-id="56f08-130">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="56f08-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="56f08-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f08-131">-DefaultProfile</span></span>
<span data-ttu-id="56f08-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="56f08-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f08-133">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="56f08-133">-Force</span></span>
<span data-ttu-id="56f08-134">Erzwingen Sie, dass die vorhandene Datei überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="56f08-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="56f08-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f08-135">-InputTextConfiguration</span></span>
<span data-ttu-id="56f08-136">Die Konfiguration, die zum Bearbeiten des Abfrageeingabetexts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56f08-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="56f08-137">Erstellen Sie das Konfigurationsobjekt mit New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="56f08-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f08-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="56f08-139">Die Konfiguration, die zum Bearbeiten des Abfrageausgabetexts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="56f08-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="56f08-140">Erstellen Sie das Konfigurationsobjekt mit New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="56f08-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56f08-141">-PassThru</span></span>
<span data-ttu-id="56f08-142">Gibt zurück, ob der angegebene Blob erfolgreich abgefragt wurde.</span><span class="sxs-lookup"><span data-stu-id="56f08-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="56f08-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="56f08-143">-QueryString</span></span>
<span data-ttu-id="56f08-144">Abfragezeichenfolge, weitere Details finden Sie unter: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="56f08-144">Query string, see more details in: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="56f08-145">-ResultFile</span></span>
<span data-ttu-id="56f08-146">Lokaler Dateipfad zum Speichern des Abfrageergebnisses.</span><span class="sxs-lookup"><span data-stu-id="56f08-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="56f08-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="56f08-148">Die Serverzeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="56f08-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="56f08-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="56f08-149">-SnapshotTime</span></span>
<span data-ttu-id="56f08-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="56f08-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="56f08-151">-VersionId</span></span>
<span data-ttu-id="56f08-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="56f08-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f08-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56f08-153">-Confirm</span></span>
<span data-ttu-id="56f08-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56f08-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f08-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f08-155">-WhatIf</span></span>
<span data-ttu-id="56f08-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56f08-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f08-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56f08-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f08-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f08-158">CommonParameters</span></span>
<span data-ttu-id="56f08-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f08-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f08-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f08-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f08-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="56f08-161">INPUTS</span></span>

### <span data-ttu-id="56f08-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="56f08-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="56f08-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="56f08-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="56f08-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="56f08-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="56f08-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="56f08-165">OUTPUTS</span></span>

### <span data-ttu-id="56f08-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56f08-166">System.Boolean</span></span>

## <span data-ttu-id="56f08-167">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="56f08-167">NOTES</span></span>

## <span data-ttu-id="56f08-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="56f08-168">RELATED LINKS</span></span>
