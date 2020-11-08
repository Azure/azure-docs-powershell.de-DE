---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165955"
---
# <span data-ttu-id="5536b-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5536b-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="5536b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5536b-102">SYNOPSIS</span></span>
<span data-ttu-id="5536b-103">Beginnt mit dem Kopieren einer Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="5536b-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="5536b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5536b-104">SYNTAX</span></span>

### <span data-ttu-id="5536b-105">Containername</span><span class="sxs-lookup"><span data-stu-id="5536b-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5536b-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5536b-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="5536b-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="5536b-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="5536b-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5536b-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="5536b-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="5536b-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="5536b-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="5536b-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5536b-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="5536b-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5536b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5536b-115">DESCRIPTION</span></span>
<span data-ttu-id="5536b-116">Das Cmdlet **Start-AzStorageFileCopy** beginnt mit dem Kopieren einer Quelldatei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="5536b-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="5536b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5536b-117">EXAMPLES</span></span>

### <span data-ttu-id="5536b-118">Beispiel 1: Starten des Kopiervorgangs aus einer Datei in eine Datei mithilfe von Freigabename und Dateinamen</span><span class="sxs-lookup"><span data-stu-id="5536b-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="5536b-119">Mit diesem Befehl wird ein Kopiervorgang aus Datei in Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="5536b-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="5536b-120">Der Befehl gibt den Freigabenamen und den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="5536b-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="5536b-121">Beispiel 2: Starten des Kopiervorgangs von einem BLOB in eine Datei mithilfe von Containername und BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="5536b-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="5536b-122">Mit diesem Befehl wird ein Kopiervorgang von BLOB in Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="5536b-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="5536b-123">Der Befehl gibt Containername und BLOB-Name an.</span><span class="sxs-lookup"><span data-stu-id="5536b-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="5536b-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="5536b-124">PARAMETERS</span></span>

### <span data-ttu-id="5536b-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="5536b-125">-AbsoluteUri</span></span>
<span data-ttu-id="5536b-126">Gibt den URI der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="5536b-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="5536b-127">Wenn für den Quellspeicherort Anmeldeinformationen erforderlich sind, müssen Sie einen angeben.</span><span class="sxs-lookup"><span data-stu-id="5536b-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="5536b-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5536b-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5536b-129">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5536b-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5536b-130">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="5536b-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5536b-131">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5536b-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5536b-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5536b-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5536b-133">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="5536b-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5536b-134">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="5536b-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5536b-135">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="5536b-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5536b-136">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="5536b-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5536b-137">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5536b-137">The default value is 10.</span></span>

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

### <span data-ttu-id="5536b-138">-Context</span><span class="sxs-lookup"><span data-stu-id="5536b-138">-Context</span></span>
<span data-ttu-id="5536b-139">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5536b-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5536b-140">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5536b-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5536b-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5536b-141">-DefaultProfile</span></span>
<span data-ttu-id="5536b-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5536b-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5536b-143">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="5536b-143">-DestContext</span></span>
<span data-ttu-id="5536b-144">Gibt den Azure-Speicherkontext des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="5536b-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="5536b-145">Verwenden Sie **New-AzStorageContext** , um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5536b-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="5536b-146">-Destdatei</span><span class="sxs-lookup"><span data-stu-id="5536b-146">-DestFile</span></span>
<span data-ttu-id="5536b-147">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5536b-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="5536b-148">Mithilfe des Get-AzStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="5536b-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="5536b-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="5536b-149">-DestFilePath</span></span>
<span data-ttu-id="5536b-150">Gibt den Pfad der Ziel Datei relativ zur Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="5536b-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="5536b-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="5536b-151">-DestShareName</span></span>
<span data-ttu-id="5536b-152">Gibt den Namen der Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="5536b-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="5536b-153">-Force</span><span class="sxs-lookup"><span data-stu-id="5536b-153">-Force</span></span>
<span data-ttu-id="5536b-154">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5536b-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5536b-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5536b-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5536b-156">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="5536b-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5536b-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="5536b-157">-SrcBlob</span></span>
<span data-ttu-id="5536b-158">Gibt ein **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5536b-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="5536b-159">Mithilfe des Get-AzStorageBlob-Cmdlets können Sie ein Cloud-BLOB erstellen oder ein BLOB abrufen.</span><span class="sxs-lookup"><span data-stu-id="5536b-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="5536b-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="5536b-160">-SrcBlobName</span></span>
<span data-ttu-id="5536b-161">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="5536b-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="5536b-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="5536b-162">-SrcContainer</span></span>
<span data-ttu-id="5536b-163">Gibt ein Cloud-BLOB-Containerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="5536b-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="5536b-164">Sie können ein Cloud-BLOB-Containerobjekt erstellen oder das Get-AzStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="5536b-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="5536b-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="5536b-165">-SrcContainerName</span></span>
<span data-ttu-id="5536b-166">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="5536b-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="5536b-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="5536b-167">-SrcFile</span></span>
<span data-ttu-id="5536b-168">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5536b-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="5536b-169">Mithilfe von **Get-AzStorageFile** können Sie eine Cloud-Datei erstellen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="5536b-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="5536b-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="5536b-170">-SrcFilePath</span></span>
<span data-ttu-id="5536b-171">Gibt den Pfad der Quelldatei relativ zum Quellverzeichnis oder zur Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="5536b-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="5536b-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="5536b-172">-SrcShare</span></span>
<span data-ttu-id="5536b-173">Gibt ein Cloud-Dateifreigabe Objekt an.</span><span class="sxs-lookup"><span data-stu-id="5536b-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="5536b-174">Mithilfe des Get-AzStorageShare-Cmdlets können Sie eine Cloud-Dateifreigabe erstellen oder eine freigeben.</span><span class="sxs-lookup"><span data-stu-id="5536b-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="5536b-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="5536b-175">-SrcShareName</span></span>
<span data-ttu-id="5536b-176">Gibt den Namen der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="5536b-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="5536b-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5536b-177">-Confirm</span></span>
<span data-ttu-id="5536b-178">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5536b-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5536b-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5536b-179">-WhatIf</span></span>
<span data-ttu-id="5536b-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5536b-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5536b-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5536b-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5536b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5536b-182">CommonParameters</span></span>
<span data-ttu-id="5536b-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5536b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5536b-184">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5536b-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5536b-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5536b-185">INPUTS</span></span>

### <span data-ttu-id="5536b-186">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5536b-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="5536b-187">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="5536b-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="5536b-188">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5536b-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5536b-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5536b-189">OUTPUTS</span></span>

### <span data-ttu-id="5536b-190">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="5536b-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="5536b-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="5536b-191">NOTES</span></span>

## <span data-ttu-id="5536b-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5536b-192">RELATED LINKS</span></span>

[<span data-ttu-id="5536b-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5536b-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="5536b-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5536b-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="5536b-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="5536b-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="5536b-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5536b-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="5536b-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="5536b-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="5536b-198">Stopp-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5536b-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
