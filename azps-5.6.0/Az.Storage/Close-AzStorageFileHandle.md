---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 71985cc978425c343e535e6455172f61e5397934
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937312"
---
# <span data-ttu-id="14c6e-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="14c6e-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="14c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="14c6e-103">Schließt die Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="14c6e-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="14c6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14c6e-104">SYNTAX</span></span>

### <span data-ttu-id="14c6e-105">ShareNameCloseAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="14c6e-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14c6e-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="14c6e-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14c6e-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="14c6e-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14c6e-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="14c6e-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14c6e-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="14c6e-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14c6e-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="14c6e-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14c6e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14c6e-111">DESCRIPTION</span></span>
<span data-ttu-id="14c6e-112">Das **Cmdlet Close-AzStorageFileHandle** schließt dateiziehpunkte einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="14c6e-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="14c6e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14c6e-113">EXAMPLES</span></span>

### <span data-ttu-id="14c6e-114">Beispiel 1: Listet alle Dateifreigaben des aktuellen Speicherkontos auf, und schließen Sie alle Dateiziehpunkte der Dateifreigaben rekursiv.</span><span class="sxs-lookup"><span data-stu-id="14c6e-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="14c6e-115">Mit diesem Befehl werden alle Dateifreigaben des aktuellen Speicherkontos aufgeführt, und alle Dateiziehpunkte der Dateifreigaben werden rekursiv geschlossen.</span><span class="sxs-lookup"><span data-stu-id="14c6e-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="14c6e-116">Beispiel 2: Schließen Sie alle Dateiziehpunkte in einem Dateiverzeichnis rekursiv, und zeigen Sie die Anzahl der Ziehpunkte für geschlossene Dateien an.</span><span class="sxs-lookup"><span data-stu-id="14c6e-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="14c6e-117">Mit diesem Befehl werden alle Dateiziehpunkte in einem Dateiverzeichnis geschlossen und die Anzahl der geschlossenen Dateihandles angezeigt.</span><span class="sxs-lookup"><span data-stu-id="14c6e-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="14c6e-118">Beispiel 3: Schließen aller Dateiziehpunkte, die vor 1 Tag in einem Dateiverzeichnis geöffnet wurden</span><span class="sxs-lookup"><span data-stu-id="14c6e-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="14c6e-119">Mit diesem Befehl werden alle Dateiziehpunkte in einem Dateiverzeichnis rekursiv aufgeführt, die Ziehpunkte, die vor einem Tag geöffnet wurden, herausfiltert und dann geschlossen.</span><span class="sxs-lookup"><span data-stu-id="14c6e-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="14c6e-120">Beispiel 4: Schließen aller Dateiziehpunkte für eine Datei</span><span class="sxs-lookup"><span data-stu-id="14c6e-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="14c6e-121">Mit diesem Befehl werden alle Dateihandles für eine Datei geschlossen.</span><span class="sxs-lookup"><span data-stu-id="14c6e-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="14c6e-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="14c6e-122">PARAMETERS</span></span>

### <span data-ttu-id="14c6e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14c6e-123">-AsJob</span></span>
<span data-ttu-id="14c6e-124">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="14c6e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14c6e-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14c6e-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="14c6e-126">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-126">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="14c6e-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="14c6e-127">-CloseAll</span></span>
<span data-ttu-id="14c6e-128">Erzwingen Sie das Schließen aller Dateiziehpunkte.</span><span class="sxs-lookup"><span data-stu-id="14c6e-128">Force close all File handles.</span></span>

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

### <span data-ttu-id="14c6e-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="14c6e-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="14c6e-130">Die Gesamtanzahl gleichzeitiger asynchroner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="14c6e-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="14c6e-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="14c6e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="14c6e-132">-Context</span><span class="sxs-lookup"><span data-stu-id="14c6e-132">-Context</span></span>
<span data-ttu-id="14c6e-133">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="14c6e-133">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="14c6e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c6e-134">-DefaultProfile</span></span>
<span data-ttu-id="14c6e-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c6e-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="14c6e-136">-Directory</span></span>
<span data-ttu-id="14c6e-137">Das CloudFileDirectory-Objekt hat den Basisordner angegeben, in dem die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c6e-138">-Datei</span><span class="sxs-lookup"><span data-stu-id="14c6e-138">-File</span></span>
<span data-ttu-id="14c6e-139">Das CloudFile-Objekt hat angegeben, dass die Datei den Handle schließen soll.</span><span class="sxs-lookup"><span data-stu-id="14c6e-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c6e-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="14c6e-140">-FileHandle</span></span>
<span data-ttu-id="14c6e-141">Das zu schließende Dateihandle.</span><span class="sxs-lookup"><span data-stu-id="14c6e-141">The File Handle to close.</span></span>

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

### <span data-ttu-id="14c6e-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14c6e-142">-PassThru</span></span>
<span data-ttu-id="14c6e-143">Gibt die Anzahl geschlossener Dateiziehpunkte zurück.</span><span class="sxs-lookup"><span data-stu-id="14c6e-143">Return the count of closed file handles.</span></span>

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

### <span data-ttu-id="14c6e-144">-Path</span><span class="sxs-lookup"><span data-stu-id="14c6e-144">-Path</span></span>
<span data-ttu-id="14c6e-145">Pfad zu einer vorhandenen Datei/einem vorhandenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="14c6e-145">Path to an existing file/directory.</span></span>

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

### <span data-ttu-id="14c6e-146">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="14c6e-146">-Recursive</span></span>
<span data-ttu-id="14c6e-147">List behandelt Rekursiv.</span><span class="sxs-lookup"><span data-stu-id="14c6e-147">List handles Recursively.</span></span>
<span data-ttu-id="14c6e-148">Funktioniert nur im Dateiverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="14c6e-148">Only works on File Directory.</span></span>

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

### <span data-ttu-id="14c6e-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14c6e-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="14c6e-150">Die Serverzeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="14c6e-151">-Teilen</span><span class="sxs-lookup"><span data-stu-id="14c6e-151">-Share</span></span>
<span data-ttu-id="14c6e-152">Das CloudFileShare-Objekt gibt die Freigabe an, in der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14c6e-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="14c6e-153">-ShareName</span></span>
<span data-ttu-id="14c6e-154">Name der Dateifreigabe, in der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="14c6e-154">Name of the file share where the files/directories would be listed.</span></span>

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

### <span data-ttu-id="14c6e-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14c6e-155">-Confirm</span></span>
<span data-ttu-id="14c6e-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14c6e-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14c6e-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14c6e-157">-WhatIf</span></span>
<span data-ttu-id="14c6e-158">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14c6e-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14c6e-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14c6e-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14c6e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c6e-160">CommonParameters</span></span>
<span data-ttu-id="14c6e-161">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c6e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c6e-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c6e-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c6e-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14c6e-163">INPUTS</span></span>

### <span data-ttu-id="14c6e-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="14c6e-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="14c6e-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="14c6e-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="14c6e-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14c6e-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="14c6e-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14c6e-167">OUTPUTS</span></span>

### <span data-ttu-id="14c6e-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="14c6e-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="14c6e-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="14c6e-169">NOTES</span></span>

## <span data-ttu-id="14c6e-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="14c6e-170">RELATED LINKS</span></span>
