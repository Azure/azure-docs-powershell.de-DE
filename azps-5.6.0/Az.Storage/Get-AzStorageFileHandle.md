---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: af5d807fcf7ad93536becd9c40df34b5e3b14220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942067"
---
# <span data-ttu-id="5bbac-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5bbac-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="5bbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bbac-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbac-103">Listet Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei auf.</span><span class="sxs-lookup"><span data-stu-id="5bbac-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="5bbac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bbac-104">SYNTAX</span></span>

### <span data-ttu-id="5bbac-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bbac-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5bbac-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="5bbac-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5bbac-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="5bbac-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5bbac-108">Datei</span><span class="sxs-lookup"><span data-stu-id="5bbac-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5bbac-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5bbac-109">DESCRIPTION</span></span>
<span data-ttu-id="5bbac-110">Das **Get-AzStorageFileHandle-Cmdlet** enthält Dateihandles einer Dateifreigabe, eines Dateiverzeichnisses oder einer Datei.</span><span class="sxs-lookup"><span data-stu-id="5bbac-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="5bbac-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5bbac-111">EXAMPLES</span></span>

### <span data-ttu-id="5bbac-112">Beispiel 1: Rekursiv alle Dateiziehpunkte für eine Dateifreigabe auflisten und nach ClientIp und OpenTime sortieren</span><span class="sxs-lookup"><span data-stu-id="5bbac-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="5bbac-113">Dieser Befehl listet Dateihandles für eine Dateifreigabe auf, und sortieren Sie die Ausgabe nach ClientIp und dann nach OpenTime.</span><span class="sxs-lookup"><span data-stu-id="5bbac-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="5bbac-114">Beispiel 2: Rekursives Auflisten von ersten 2 Dateihandles in einem Dateiverzeichnis</span><span class="sxs-lookup"><span data-stu-id="5bbac-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="5bbac-115">Mit diesem Befehl werden die ersten zwei Dateiziehpunkte in einem Dateiverzeichnis rekursiv aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bbac-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="5bbac-116">Beispiel 3: Auflisten der 3. bis 6. Dateihandles für eine Datei</span><span class="sxs-lookup"><span data-stu-id="5bbac-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="5bbac-117">Mit diesem Befehl werden die 3. bis 6. Dateihandles für eine Datei aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bbac-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="5bbac-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5bbac-118">PARAMETERS</span></span>

### <span data-ttu-id="5bbac-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5bbac-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5bbac-120">Die clientseitige maximale Ausführungszeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-120">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="5bbac-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5bbac-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5bbac-122">Die Gesamtanzahl gleichzeitiger asynchroner Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="5bbac-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="5bbac-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5bbac-123">The default value is 10.</span></span>

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

### <span data-ttu-id="5bbac-124">-Context</span><span class="sxs-lookup"><span data-stu-id="5bbac-124">-Context</span></span>
<span data-ttu-id="5bbac-125">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="5bbac-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbac-126">-DefaultProfile</span></span>
<span data-ttu-id="5bbac-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bbac-128">-Directory</span><span class="sxs-lookup"><span data-stu-id="5bbac-128">-Directory</span></span>
<span data-ttu-id="5bbac-129">Das CloudFileDirectory-Objekt hat den Basisordner angegeben, in dem die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="5bbac-130">-File</span></span>
<span data-ttu-id="5bbac-131">Das CloudFile-Objekt hat angegeben, dass die Datei Dateihandles auflisten soll.</span><span class="sxs-lookup"><span data-stu-id="5bbac-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-132">-Path</span><span class="sxs-lookup"><span data-stu-id="5bbac-132">-Path</span></span>
<span data-ttu-id="5bbac-133">Pfad zu einer vorhandenen Datei/einem vorhandenen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5bbac-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-134">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="5bbac-134">-Recursive</span></span>
<span data-ttu-id="5bbac-135">List behandelt Rekursiv.</span><span class="sxs-lookup"><span data-stu-id="5bbac-135">List handles Recursively.</span></span>
<span data-ttu-id="5bbac-136">Funktioniert nur im Dateiverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="5bbac-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="5bbac-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5bbac-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5bbac-138">Die Serverzeit für jede Anforderung in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-138">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="5bbac-139">-Teilen</span><span class="sxs-lookup"><span data-stu-id="5bbac-139">-Share</span></span>
<span data-ttu-id="5bbac-140">Das CloudFileShare-Objekt gibt die Freigabe an, in der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5bbac-141">-ShareName</span></span>
<span data-ttu-id="5bbac-142">Name der Dateifreigabe, in der die Dateien/Verzeichnisse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="5bbac-142">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5bbac-143">-IncludeTotalCount</span></span>
<span data-ttu-id="5bbac-144">Gibt die Anzahl der Objekte im Datenset (eine ganze Zahl) gefolgt von den -Objekten an.</span><span class="sxs-lookup"><span data-stu-id="5bbac-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="5bbac-145">Wenn das Cmdlet die Gesamtanzahl nicht ermitteln kann, gibt es "Unbekannte Gesamtanzahl" zurück.</span><span class="sxs-lookup"><span data-stu-id="5bbac-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="5bbac-146">Dieser Parameter führt zurzeit nichts aus.</span><span class="sxs-lookup"><span data-stu-id="5bbac-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5bbac-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="5bbac-147">-Skip</span></span>
<span data-ttu-id="5bbac-148">Ignoriert die ersten "n"-Objekte und ruft dann die verbleibenden Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="5bbac-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-149">-First</span><span class="sxs-lookup"><span data-stu-id="5bbac-149">-First</span></span>
<span data-ttu-id="5bbac-150">Ruft nur die ersten "n"-Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="5bbac-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbac-151">CommonParameters</span></span>
<span data-ttu-id="5bbac-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bbac-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbac-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbac-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbac-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5bbac-154">INPUTS</span></span>

### <span data-ttu-id="5bbac-155">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="5bbac-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="5bbac-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="5bbac-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="5bbac-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5bbac-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5bbac-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5bbac-158">OUTPUTS</span></span>

### <span data-ttu-id="5bbac-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="5bbac-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="5bbac-160">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5bbac-160">NOTES</span></span>

## <span data-ttu-id="5bbac-161">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5bbac-161">RELATED LINKS</span></span>
