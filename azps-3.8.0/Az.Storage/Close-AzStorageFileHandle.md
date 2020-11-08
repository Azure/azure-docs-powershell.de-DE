---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 6f288a124d0a024fc4b961409a17f9e0fe736c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995966"
---
# <span data-ttu-id="01440-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="01440-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="01440-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01440-102">SYNOPSIS</span></span>
<span data-ttu-id="01440-103">Schließt Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="01440-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="01440-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01440-104">SYNTAX</span></span>

### <span data-ttu-id="01440-105">ShareNameCloseAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="01440-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01440-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="01440-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01440-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="01440-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01440-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="01440-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01440-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="01440-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01440-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="01440-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01440-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01440-111">DESCRIPTION</span></span>
<span data-ttu-id="01440-112">Mit dem Cmdlet " **Close-AzStorageFileHandle** " werden Dateihandles einer Dateifreigabe oder eines Dateiverzeichnisses oder einer Datei geschlossen.</span><span class="sxs-lookup"><span data-stu-id="01440-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="01440-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01440-113">EXAMPLES</span></span>

### <span data-ttu-id="01440-114">Beispiel 1: Listet alle Dateifreigaben des aktuellen speicherkontos auf und schließt alle Dateihandles der Dateifreigaben rekursiv.</span><span class="sxs-lookup"><span data-stu-id="01440-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="01440-115">Dieser Befehl listet alle Dateifreigaben des aktuellen speicherkontos auf und schließt alle Dateihandles der Dateifreigaben rekursiv.</span><span class="sxs-lookup"><span data-stu-id="01440-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="01440-116">Beispiel 2: Schließen Sie alle Dateihandles in einem Dateiverzeichnis rekursiv, und zeigen Sie die Anzahl der geschlossenen Dateihandles an.</span><span class="sxs-lookup"><span data-stu-id="01440-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="01440-117">Mit diesem Befehl werden alle Dateihandles in einem Dateiverzeichnis geschlossen und die Anzahl der geschlossenen Dateihandles angezeigt.</span><span class="sxs-lookup"><span data-stu-id="01440-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="01440-118">Beispiel 3: Schließen Sie alle Dateihandles, die vor 1 Tag in einem Dateiverzeichnis geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="01440-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="01440-119">Dieser Befehl listet alle Dateihandles in einem Dateiverzeichnis rekursiv auf, filtert die Handles, die vor 1 Tag geöffnet sind, und schließt Sie dann.</span><span class="sxs-lookup"><span data-stu-id="01440-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="01440-120">Beispiel 4: Schließen aller Dateihandles für eine Datei</span><span class="sxs-lookup"><span data-stu-id="01440-120">Example 4: Close all file handles on a file</span></span> 
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="01440-121">Mit diesem Befehl werden alle Dateihandles für eine Datei geschlossen.</span><span class="sxs-lookup"><span data-stu-id="01440-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="01440-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="01440-122">PARAMETERS</span></span>

### <span data-ttu-id="01440-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01440-123">-AsJob</span></span>
<span data-ttu-id="01440-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01440-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01440-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01440-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="01440-126">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="01440-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="01440-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="01440-127">-CloseAll</span></span>
<span data-ttu-id="01440-128">Erzwingen, dass alle Dateihandles geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="01440-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01440-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="01440-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="01440-130">Der Gesamtumfang der gleichzeitigen asynchronen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="01440-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="01440-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="01440-131">The default value is 10.</span></span>

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

### <span data-ttu-id="01440-132">-Context</span><span class="sxs-lookup"><span data-stu-id="01440-132">-Context</span></span>
<span data-ttu-id="01440-133">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="01440-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01440-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01440-134">-DefaultProfile</span></span>
<span data-ttu-id="01440-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01440-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01440-136">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="01440-136">-Directory</span></span>
<span data-ttu-id="01440-137">Das CloudFileDirectory-Objekt hat den Basisordner angegeben, in dem die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="01440-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01440-138">-Datei</span><span class="sxs-lookup"><span data-stu-id="01440-138">-File</span></span>
<span data-ttu-id="01440-139">Das clouddatei-Objekt hat die Datei zum Schließen des Handles angegeben.</span><span class="sxs-lookup"><span data-stu-id="01440-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01440-140">-Handle</span><span class="sxs-lookup"><span data-stu-id="01440-140">-FileHandle</span></span>
<span data-ttu-id="01440-141">Das zu schließende Datei handle.</span><span class="sxs-lookup"><span data-stu-id="01440-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01440-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01440-142">-PassThru</span></span>
<span data-ttu-id="01440-143">Gibt die Anzahl der geschlossenen Dateihandles zurück.</span><span class="sxs-lookup"><span data-stu-id="01440-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="01440-144">-Path</span><span class="sxs-lookup"><span data-stu-id="01440-144">-Path</span></span>
<span data-ttu-id="01440-145">Pfad zu einer vorhandenen Datei/einem vorhandenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="01440-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01440-146">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="01440-146">-Recursive</span></span>
<span data-ttu-id="01440-147">Listen Handles rekursiv.</span><span class="sxs-lookup"><span data-stu-id="01440-147">List handles Recursively.</span></span>
<span data-ttu-id="01440-148">Funktioniert nur im Dateiverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="01440-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01440-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="01440-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="01440-150">Der Servertimeout für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="01440-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="01440-151">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="01440-151">-Share</span></span>
<span data-ttu-id="01440-152">CloudFileShare-Objekt hat die Freigabe angegeben, auf der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="01440-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01440-153">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="01440-153">-ShareName</span></span>
<span data-ttu-id="01440-154">Name der Dateifreigabe, in der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="01440-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01440-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01440-155">-Confirm</span></span>
<span data-ttu-id="01440-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01440-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01440-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01440-157">-WhatIf</span></span>
<span data-ttu-id="01440-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01440-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01440-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01440-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01440-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01440-160">CommonParameters</span></span>
<span data-ttu-id="01440-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01440-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01440-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01440-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01440-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01440-163">INPUTS</span></span>

### <span data-ttu-id="01440-164">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="01440-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="01440-165">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="01440-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="01440-166">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01440-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01440-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01440-167">OUTPUTS</span></span>

### <span data-ttu-id="01440-168">Microsoft. Azure. Storage. File. CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="01440-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="01440-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="01440-169">NOTES</span></span>

## <span data-ttu-id="01440-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01440-170">RELATED LINKS</span></span>
