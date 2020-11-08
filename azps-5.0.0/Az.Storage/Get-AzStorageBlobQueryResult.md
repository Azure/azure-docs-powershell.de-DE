---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176220"
---
# <span data-ttu-id="bf1c5-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="bf1c5-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="bf1c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1c5-103">Wendet eine einfache SQL-Anweisung (Structured Query Language) auf den Inhalt eines BLOBs an und speichert nur die abgefragte Teilmenge der Daten in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="bf1c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1c5-104">SYNTAX</span></span>

### <span data-ttu-id="bf1c5-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf1c5-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf1c5-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="bf1c5-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf1c5-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="bf1c5-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf1c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="bf1c5-109">Das Cmdlet " **Get-AzStorageBlobQueryResult** " wendet eine einfache SQL-Anweisung (Structured Query Language) auf den Inhalt eines BLOBs an und speichert die abgefragte Teilmenge der Daten in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="bf1c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf1c5-110">EXAMPLES</span></span>

### <span data-ttu-id="bf1c5-111">Beispiel 1: Abfragen eines BLOBs</span><span class="sxs-lookup"><span data-stu-id="bf1c5-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="bf1c5-112">Dieser Befehl fragt eine BLOB-succsssfully mit der Eingabekonfiguration als CSV ab und gibt die Ausgabekonfiguration als JSON aus und speichert die Ausgabe in der lokalen Datei "c:\resultfile.jsein".</span><span class="sxs-lookup"><span data-stu-id="bf1c5-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="bf1c5-113">Beispiel 2: Abfragen eines BLOB-Snapshots</span><span class="sxs-lookup"><span data-stu-id="bf1c5-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="bf1c5-114">Dieser Befehl ruft zunächst ein BLOB-Objekt für den BLOB-Snapshot ab, fragt dann den BLOB-Snapshot ab und zeigt den Fehler "Ergebnis einbeziehen" an.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="bf1c5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1c5-115">PARAMETERS</span></span>

### <span data-ttu-id="bf1c5-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="bf1c5-116">-Blob</span></span>
<span data-ttu-id="bf1c5-117">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="bf1c5-117">Blob name</span></span>

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

### <span data-ttu-id="bf1c5-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="bf1c5-118">-BlobBaseClient</span></span>
<span data-ttu-id="bf1c5-119">BlobBaseClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf1c5-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="bf1c5-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="bf1c5-120">-BlobContainerClient</span></span>
<span data-ttu-id="bf1c5-121">BlobContainerClient-Objekt</span><span class="sxs-lookup"><span data-stu-id="bf1c5-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="bf1c5-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf1c5-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf1c5-123">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="bf1c5-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf1c5-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf1c5-125">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="bf1c5-126">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-126">The default value is 10.</span></span>

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

### <span data-ttu-id="bf1c5-127">-Container</span><span class="sxs-lookup"><span data-stu-id="bf1c5-127">-Container</span></span>
<span data-ttu-id="bf1c5-128">Container Name</span><span class="sxs-lookup"><span data-stu-id="bf1c5-128">Container name</span></span>

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

### <span data-ttu-id="bf1c5-129">-Context</span><span class="sxs-lookup"><span data-stu-id="bf1c5-129">-Context</span></span>
<span data-ttu-id="bf1c5-130">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="bf1c5-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="bf1c5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1c5-131">-DefaultProfile</span></span>
<span data-ttu-id="bf1c5-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf1c5-133">-Force</span><span class="sxs-lookup"><span data-stu-id="bf1c5-133">-Force</span></span>
<span data-ttu-id="bf1c5-134">Erzwingen, dass die vorhandene Datei überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="bf1c5-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf1c5-135">-InputTextConfiguration</span></span>
<span data-ttu-id="bf1c5-136">Die Konfiguration, die zum Behandeln des Abfrageeingabe Texts verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="bf1c5-137">Erstellen Sie ein Konfigurationsobjekt, das mit New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="bf1c5-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf1c5-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="bf1c5-139">Die Konfiguration, die zum Behandeln des Abfrageausgabe Texts verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="bf1c5-140">Erstellen Sie ein Konfigurationsobjekt, das mit New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="bf1c5-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf1c5-141">-PassThru</span></span>
<span data-ttu-id="bf1c5-142">Gibt zurück, ob der angegebene BLOB erfolgreich abgefragt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="bf1c5-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="bf1c5-143">-QueryString</span></span>
<span data-ttu-id="bf1c5-144">Abfragezeichenfolge, weitere Details finden Sie unter: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="bf1c5-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="bf1c5-145">-Ergebnisdatei</span><span class="sxs-lookup"><span data-stu-id="bf1c5-145">-ResultFile</span></span>
<span data-ttu-id="bf1c5-146">Lokaler Dateipfad zum Speichern des Abfrageergebnisses</span><span class="sxs-lookup"><span data-stu-id="bf1c5-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="bf1c5-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf1c5-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf1c5-148">Der Servertimeout für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="bf1c5-149">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="bf1c5-149">-SnapshotTime</span></span>
<span data-ttu-id="bf1c5-150">BLOB-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="bf1c5-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="bf1c5-151">-Versions-Nr</span><span class="sxs-lookup"><span data-stu-id="bf1c5-151">-VersionId</span></span>
<span data-ttu-id="bf1c5-152">BLOB-Versions-Nr</span><span class="sxs-lookup"><span data-stu-id="bf1c5-152">Blob VersionId</span></span>

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

### <span data-ttu-id="bf1c5-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf1c5-153">-Confirm</span></span>
<span data-ttu-id="bf1c5-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf1c5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf1c5-155">-WhatIf</span></span>
<span data-ttu-id="bf1c5-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf1c5-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf1c5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1c5-158">CommonParameters</span></span>
<span data-ttu-id="bf1c5-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1c5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1c5-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1c5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1c5-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf1c5-161">INPUTS</span></span>

### <span data-ttu-id="bf1c5-162">Azure. Storage. BLOBs. Specialized. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="bf1c5-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="bf1c5-163">Azure. Storage. BLOBs. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="bf1c5-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="bf1c5-164">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf1c5-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bf1c5-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf1c5-165">OUTPUTS</span></span>

### <span data-ttu-id="bf1c5-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf1c5-166">System.Boolean</span></span>

## <span data-ttu-id="bf1c5-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf1c5-167">NOTES</span></span>

## <span data-ttu-id="bf1c5-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf1c5-168">RELATED LINKS</span></span>
