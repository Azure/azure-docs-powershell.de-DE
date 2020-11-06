---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: c5e071ddb5316f223260d3e6f239df4e75612332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498578"
---
# <span data-ttu-id="b6379-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6379-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="b6379-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6379-102">SYNOPSIS</span></span>
<span data-ttu-id="b6379-103">Beginnt mit dem Kopieren einer Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="b6379-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6379-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6379-104">SYNTAX</span></span>

### <span data-ttu-id="b6379-105">Containername</span><span class="sxs-lookup"><span data-stu-id="b6379-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6379-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b6379-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="b6379-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="b6379-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6379-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="b6379-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6379-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="b6379-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="b6379-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="b6379-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6379-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="b6379-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6379-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="b6379-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6379-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6379-115">DESCRIPTION</span></span>
<span data-ttu-id="b6379-116">Das Cmdlet **Start-AzureStorageFileCopy** beginnt mit dem Kopieren einer Quelldatei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="b6379-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="b6379-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6379-117">EXAMPLES</span></span>

### <span data-ttu-id="b6379-118">Beispiel 1: Starten des Kopiervorgangs aus einer Datei in eine Datei mithilfe von Freigabename und Dateinamen</span><span class="sxs-lookup"><span data-stu-id="b6379-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="b6379-119">Mit diesem Befehl wird ein Kopiervorgang aus Datei in Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="b6379-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="b6379-120">Der Befehl gibt den Freigabenamen und den Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="b6379-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="b6379-121">Beispiel 2: Starten des Kopiervorgangs von einem BLOB in eine Datei mithilfe von Containername und BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="b6379-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="b6379-122">Mit diesem Befehl wird ein Kopiervorgang von BLOB in Datei gestartet.</span><span class="sxs-lookup"><span data-stu-id="b6379-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="b6379-123">Der Befehl gibt Containername und BLOB-Name an.</span><span class="sxs-lookup"><span data-stu-id="b6379-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="b6379-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6379-124">PARAMETERS</span></span>

### <span data-ttu-id="b6379-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="b6379-125">-AbsoluteUri</span></span>
<span data-ttu-id="b6379-126">Gibt den URI der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="b6379-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="b6379-127">Wenn für den Quellspeicherort Anmeldeinformationen erforderlich sind, müssen Sie einen angeben.</span><span class="sxs-lookup"><span data-stu-id="b6379-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="b6379-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6379-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b6379-129">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b6379-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6379-130">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="b6379-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6379-131">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b6379-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6379-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b6379-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b6379-133">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="b6379-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b6379-134">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="b6379-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b6379-135">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b6379-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b6379-136">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="b6379-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b6379-137">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b6379-137">The default value is 10.</span></span>

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

### <span data-ttu-id="b6379-138">-Context</span><span class="sxs-lookup"><span data-stu-id="b6379-138">-Context</span></span>
<span data-ttu-id="b6379-139">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b6379-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b6379-140">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6379-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b6379-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6379-141">-DefaultProfile</span></span>
<span data-ttu-id="b6379-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6379-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6379-143">-Destcontext</span><span class="sxs-lookup"><span data-stu-id="b6379-143">-DestContext</span></span>
<span data-ttu-id="b6379-144">Gibt den Azure-Speicherkontext des Ziels an.</span><span class="sxs-lookup"><span data-stu-id="b6379-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="b6379-145">Verwenden Sie **New-AzureStorageContext** , um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b6379-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

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

### <span data-ttu-id="b6379-146">-Destdatei</span><span class="sxs-lookup"><span data-stu-id="b6379-146">-DestFile</span></span>
<span data-ttu-id="b6379-147">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6379-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="b6379-148">Mithilfe des Get-AzureStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="b6379-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6379-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="b6379-149">-DestFilePath</span></span>
<span data-ttu-id="b6379-150">Gibt den Pfad der Ziel Datei relativ zur Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="b6379-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="b6379-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="b6379-151">-DestShareName</span></span>
<span data-ttu-id="b6379-152">Gibt den Namen der Zielfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="b6379-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="b6379-153">-Force</span><span class="sxs-lookup"><span data-stu-id="b6379-153">-Force</span></span>
<span data-ttu-id="b6379-154">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b6379-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6379-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6379-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b6379-156">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b6379-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b6379-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="b6379-157">-SrcBlob</span></span>
<span data-ttu-id="b6379-158">Gibt ein **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6379-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="b6379-159">Mithilfe des Get-AzureStorageBlob-Cmdlets können Sie ein Cloud-BLOB erstellen oder ein BLOB abrufen.</span><span class="sxs-lookup"><span data-stu-id="b6379-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6379-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="b6379-160">-SrcBlobName</span></span>
<span data-ttu-id="b6379-161">Gibt den Namen des Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="b6379-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="b6379-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="b6379-162">-SrcContainer</span></span>
<span data-ttu-id="b6379-163">Gibt ein Cloud-BLOB-Containerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b6379-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="b6379-164">Sie können ein Cloud-BLOB-Containerobjekt erstellen oder das Get-AzureStorageContainer-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6379-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6379-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="b6379-165">-SrcContainerName</span></span>
<span data-ttu-id="b6379-166">Gibt den Namen des Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="b6379-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="b6379-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="b6379-167">-SrcFile</span></span>
<span data-ttu-id="b6379-168">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6379-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="b6379-169">Mithilfe von **Get-AzureStorageFile** können Sie eine Cloud-Datei erstellen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="b6379-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6379-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="b6379-170">-SrcFilePath</span></span>
<span data-ttu-id="b6379-171">Gibt den Pfad der Quelldatei relativ zum Quellverzeichnis oder zur Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="b6379-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="b6379-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="b6379-172">-SrcShare</span></span>
<span data-ttu-id="b6379-173">Gibt ein Cloud-Dateifreigabe Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6379-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="b6379-174">Mithilfe des Get-AzureStorageShare-Cmdlets können Sie eine Cloud-Dateifreigabe erstellen oder eine freigeben.</span><span class="sxs-lookup"><span data-stu-id="b6379-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6379-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="b6379-175">-SrcShareName</span></span>
<span data-ttu-id="b6379-176">Gibt den Namen der Quell Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="b6379-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="b6379-177">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6379-177">-Confirm</span></span>
<span data-ttu-id="b6379-178">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6379-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6379-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6379-179">-WhatIf</span></span>
<span data-ttu-id="b6379-180">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6379-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6379-181">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6379-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6379-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6379-182">CommonParameters</span></span>
<span data-ttu-id="b6379-183">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6379-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6379-184">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6379-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6379-185">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6379-185">INPUTS</span></span>

### <span data-ttu-id="b6379-186">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b6379-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b6379-187">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="b6379-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="b6379-188">Parameter: srcfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6379-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="b6379-189">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6379-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b6379-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6379-190">OUTPUTS</span></span>

### <span data-ttu-id="b6379-191">System. void</span><span class="sxs-lookup"><span data-stu-id="b6379-191">System.Void</span></span>

## <span data-ttu-id="b6379-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6379-192">NOTES</span></span>

## <span data-ttu-id="b6379-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6379-193">RELATED LINKS</span></span>

[<span data-ttu-id="b6379-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b6379-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b6379-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b6379-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="b6379-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="b6379-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="b6379-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b6379-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b6379-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="b6379-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="b6379-199">Stopp-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="b6379-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
