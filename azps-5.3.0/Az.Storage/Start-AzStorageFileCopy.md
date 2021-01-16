---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376059"
---
# <span data-ttu-id="f295e-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f295e-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="f295e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f295e-102">SYNOPSIS</span></span>
<span data-ttu-id="f295e-103">Beginnt mit dem Kopieren einer Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="f295e-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="f295e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f295e-104">SYNTAX</span></span>

### <span data-ttu-id="f295e-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="f295e-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f295e-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f295e-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="f295e-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="f295e-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="f295e-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f295e-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="f295e-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="f295e-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="f295e-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="f295e-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f295e-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="f295e-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f295e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f295e-115">DESCRIPTION</span></span>
<span data-ttu-id="f295e-116">Das **Cmdlet "Start-AzStorageFileCopy"** beginnt mit dem Kopieren einer Quelldatei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="f295e-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="f295e-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f295e-117">EXAMPLES</span></span>

### <span data-ttu-id="f295e-118">Beispiel 1: Starten des Kopiervorgangs von Datei zu Datei mithilfe von Freigabename und Dateiname</span><span class="sxs-lookup"><span data-stu-id="f295e-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="f295e-119">Mit diesem Befehl wird ein Kopiervorgang von Datei zu Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="f295e-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="f295e-120">Der Befehl gibt den Freigabenamen und den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="f295e-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="f295e-121">Beispiel 2: Starten des Kopiervorgangs von BLOB zu Datei mithilfe des Containernamens und des BLOB-Namens</span><span class="sxs-lookup"><span data-stu-id="f295e-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="f295e-122">Dieser Befehl startet einen Kopiervorgang von BLOB in Datei.</span><span class="sxs-lookup"><span data-stu-id="f295e-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="f295e-123">Der Befehl gibt den Containernamen und den BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="f295e-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="f295e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f295e-124">PARAMETERS</span></span>

### <span data-ttu-id="f295e-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="f295e-125">-AbsoluteUri</span></span>
<span data-ttu-id="f295e-126">Gibt den URI der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="f295e-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="f295e-127">Wenn für den Quellspeicherort Anmeldeinformationen erforderlich sind, müssen Sie eine angeben.</span><span class="sxs-lookup"><span data-stu-id="f295e-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="f295e-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f295e-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f295e-129">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="f295e-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f295e-130">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f295e-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f295e-131">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f295e-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f295e-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f295e-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f295e-133">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="f295e-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f295e-134">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="f295e-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f295e-135">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f295e-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f295e-136">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="f295e-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f295e-137">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f295e-137">The default value is 10.</span></span>

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

### <span data-ttu-id="f295e-138">-Context</span><span class="sxs-lookup"><span data-stu-id="f295e-138">-Context</span></span>
<span data-ttu-id="f295e-139">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="f295e-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f295e-140">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f295e-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f295e-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f295e-141">-DefaultProfile</span></span>
<span data-ttu-id="f295e-142">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f295e-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f295e-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="f295e-143">-DestContext</span></span>
<span data-ttu-id="f295e-144">Gibt den Azure Storage-Kontext des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="f295e-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="f295e-145">Verwenden Sie **"New-AzStorageContext", um** einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f295e-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="f295e-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="f295e-146">-DestFile</span></span>
<span data-ttu-id="f295e-147">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f295e-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f295e-148">Sie können eine Clouddatei erstellen oder sie mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="f295e-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="f295e-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="f295e-149">-DestFilePath</span></span>
<span data-ttu-id="f295e-150">Gibt den Pfad der Zieldatei relativ zur Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="f295e-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="f295e-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="f295e-151">-DestShareName</span></span>
<span data-ttu-id="f295e-152">Gibt den Namen der Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="f295e-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="f295e-153">-Force</span><span class="sxs-lookup"><span data-stu-id="f295e-153">-Force</span></span>
<span data-ttu-id="f295e-154">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="f295e-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f295e-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f295e-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f295e-156">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f295e-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f295e-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="f295e-157">-SrcBlob</span></span>
<span data-ttu-id="f295e-158">Gibt ein **CloudBlob-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f295e-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="f295e-159">Sie können ein Cloud-BLOB erstellen oder eines mithilfe des cmdlets Get-AzStorageBlob abrufen.</span><span class="sxs-lookup"><span data-stu-id="f295e-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="f295e-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="f295e-160">-SrcBlobName</span></span>
<span data-ttu-id="f295e-161">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="f295e-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="f295e-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="f295e-162">-SrcContainer</span></span>
<span data-ttu-id="f295e-163">Gibt ein Cloud-BLOB-Containerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f295e-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="f295e-164">Sie können Cloud-BLOB-Container-Objekt erstellen oder das cmdlet Get-AzStorageContainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="f295e-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="f295e-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="f295e-165">-SrcContainerName</span></span>
<span data-ttu-id="f295e-166">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="f295e-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="f295e-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="f295e-167">-SrcFile</span></span>
<span data-ttu-id="f295e-168">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="f295e-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f295e-169">Sie können eine Clouddatei erstellen oder eine abrufen, indem Sie **"Get-AzStorageFile" verwenden.**</span><span class="sxs-lookup"><span data-stu-id="f295e-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="f295e-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="f295e-170">-SrcFilePath</span></span>
<span data-ttu-id="f295e-171">Gibt den Pfad der Quelldatei relativ zum Quellverzeichnis oder zur Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="f295e-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="f295e-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="f295e-172">-SrcShare</span></span>
<span data-ttu-id="f295e-173">Gibt ein Clouddateifreigabeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f295e-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="f295e-174">Sie können eine Clouddateifreigabe erstellen oder sie mithilfe des cmdlets Get-AzStorageShare abrufen.</span><span class="sxs-lookup"><span data-stu-id="f295e-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="f295e-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="f295e-175">-SrcShareName</span></span>
<span data-ttu-id="f295e-176">Gibt den Namen der Quellfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="f295e-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="f295e-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f295e-177">-Confirm</span></span>
<span data-ttu-id="f295e-178">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f295e-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f295e-179">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f295e-179">-WhatIf</span></span>
<span data-ttu-id="f295e-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f295e-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f295e-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f295e-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f295e-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f295e-182">CommonParameters</span></span>
<span data-ttu-id="f295e-183">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f295e-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f295e-184">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f295e-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f295e-185">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f295e-185">INPUTS</span></span>

### <span data-ttu-id="f295e-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f295e-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="f295e-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="f295e-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f295e-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f295e-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f295e-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f295e-189">OUTPUTS</span></span>

### <span data-ttu-id="f295e-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f295e-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="f295e-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f295e-191">NOTES</span></span>

## <span data-ttu-id="f295e-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f295e-192">RELATED LINKS</span></span>

[<span data-ttu-id="f295e-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f295e-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="f295e-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f295e-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="f295e-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f295e-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f295e-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f295e-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="f295e-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="f295e-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="f295e-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f295e-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
