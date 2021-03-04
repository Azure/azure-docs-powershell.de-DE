---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2b3bea343e5d4e2267c2bec14d60564392914a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922651"
---
# <span data-ttu-id="ab625-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ab625-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="ab625-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab625-102">SYNOPSIS</span></span>
<span data-ttu-id="ab625-103">Beginnt mit dem Kopieren einer Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="ab625-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="ab625-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab625-104">SYNTAX</span></span>

### <span data-ttu-id="ab625-105">Containername</span><span class="sxs-lookup"><span data-stu-id="ab625-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab625-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ab625-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="ab625-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="ab625-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="ab625-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab625-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="ab625-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="ab625-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ab625-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="ab625-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab625-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="ab625-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab625-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab625-115">DESCRIPTION</span></span>
<span data-ttu-id="ab625-116">Das **Cmdlet Start-AzStorageFileCopy** beginnt mit dem Kopieren einer Quelldatei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="ab625-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="ab625-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab625-117">EXAMPLES</span></span>

### <span data-ttu-id="ab625-118">Beispiel 1: Starten des Kopiervorgangs von Datei zu Datei mithilfe von Freigabename und Dateinamen</span><span class="sxs-lookup"><span data-stu-id="ab625-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="ab625-119">Mit diesem Befehl wird ein Kopiervorgang von Datei zu Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="ab625-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="ab625-120">Der Befehl gibt den Namen der Freigabe und den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="ab625-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="ab625-121">Beispiel 2: Starten des Kopiervorgangs von Blob in Datei mithilfe von Containername und Blobname</span><span class="sxs-lookup"><span data-stu-id="ab625-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="ab625-122">Mit diesem Befehl wird ein Kopiervorgang von Blob in Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="ab625-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="ab625-123">Der Befehl gibt den Containernamen und den Blobnamen an.</span><span class="sxs-lookup"><span data-stu-id="ab625-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="ab625-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ab625-124">PARAMETERS</span></span>

### <span data-ttu-id="ab625-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="ab625-125">-AbsoluteUri</span></span>
<span data-ttu-id="ab625-126">Gibt den URI der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="ab625-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="ab625-127">Wenn der Quellspeicherort eine Anmeldeinformationen erfordert, müssen Sie eine angeben.</span><span class="sxs-lookup"><span data-stu-id="ab625-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab625-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ab625-129">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="ab625-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ab625-130">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab625-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ab625-131">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ab625-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ab625-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ab625-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ab625-133">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="ab625-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ab625-134">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="ab625-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ab625-135">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="ab625-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ab625-136">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="ab625-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ab625-137">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="ab625-137">The default value is 10.</span></span>

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

### <span data-ttu-id="ab625-138">-Context</span><span class="sxs-lookup"><span data-stu-id="ab625-138">-Context</span></span>
<span data-ttu-id="ab625-139">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="ab625-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ab625-140">Verwenden Sie das cmdlet New-AzStorageContext, um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab625-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab625-141">-DefaultProfile</span></span>
<span data-ttu-id="ab625-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab625-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab625-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="ab625-143">-DestContext</span></span>
<span data-ttu-id="ab625-144">Gibt den Azure Storage-Kontext des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="ab625-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="ab625-145">Verwenden Sie **New-AzStorageContext,** um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab625-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="ab625-146">-DestFile</span></span>
<span data-ttu-id="ab625-147">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ab625-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ab625-148">Sie können eine Clouddatei erstellen oder mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab625-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="ab625-149">-DestFilePath</span></span>
<span data-ttu-id="ab625-150">Gibt den Pfad der Zieldatei relativ zur Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab625-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="ab625-151">-DestShareName</span></span>
<span data-ttu-id="ab625-152">Gibt den Namen der Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab625-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-153">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ab625-153">-Force</span></span>
<span data-ttu-id="ab625-154">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ab625-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab625-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ab625-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ab625-156">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="ab625-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ab625-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="ab625-157">-SrcBlob</span></span>
<span data-ttu-id="ab625-158">Gibt ein **CloudBlob-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ab625-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ab625-159">Sie können ein Cloudblob erstellen oder mithilfe des cmdlets Get-AzStorageBlob abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab625-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="ab625-160">-SrcBlobName</span></span>
<span data-ttu-id="ab625-161">Gibt den Namen des Quellblobs an.</span><span class="sxs-lookup"><span data-stu-id="ab625-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="ab625-162">-SrcContainer</span></span>
<span data-ttu-id="ab625-163">Gibt ein Cloud-Blob-Containerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="ab625-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="ab625-164">Sie können cloudblob-Containerobjekt erstellen oder das Get-AzStorageContainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab625-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="ab625-165">-SrcContainerName</span></span>
<span data-ttu-id="ab625-166">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="ab625-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="ab625-167">-SrcFile</span></span>
<span data-ttu-id="ab625-168">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="ab625-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ab625-169">Sie können eine Clouddatei erstellen oder eine abrufen, indem Sie **Get-AzStorageFile verwenden.**</span><span class="sxs-lookup"><span data-stu-id="ab625-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="ab625-170">-SrcFilePath</span></span>
<span data-ttu-id="ab625-171">Gibt den Pfad der Quelldatei relativ zum Quellverzeichnis oder zur Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab625-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="ab625-172">-SrcShare</span></span>
<span data-ttu-id="ab625-173">Gibt ein Clouddateifreigabeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="ab625-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="ab625-174">Sie können eine Clouddateifreigabe erstellen oder mithilfe des cmdlets Get-AzStorageShare abrufen.</span><span class="sxs-lookup"><span data-stu-id="ab625-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="ab625-175">-SrcShareName</span></span>
<span data-ttu-id="ab625-176">Gibt den Namen der Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="ab625-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab625-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab625-177">-Confirm</span></span>
<span data-ttu-id="ab625-178">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab625-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab625-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab625-179">-WhatIf</span></span>
<span data-ttu-id="ab625-180">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab625-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab625-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab625-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab625-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab625-182">CommonParameters</span></span>
<span data-ttu-id="ab625-183">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab625-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab625-184">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab625-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab625-185">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab625-185">INPUTS</span></span>

### <span data-ttu-id="ab625-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ab625-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ab625-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="ab625-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ab625-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab625-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab625-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab625-189">OUTPUTS</span></span>

### <span data-ttu-id="ab625-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="ab625-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="ab625-191">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ab625-191">NOTES</span></span>

## <span data-ttu-id="ab625-192">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ab625-192">RELATED LINKS</span></span>

[<span data-ttu-id="ab625-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ab625-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ab625-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab625-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="ab625-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ab625-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ab625-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ab625-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="ab625-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="ab625-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="ab625-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ab625-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
