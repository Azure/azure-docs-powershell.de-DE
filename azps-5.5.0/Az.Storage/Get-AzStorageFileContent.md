---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143889"
---
# <span data-ttu-id="8b531-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b531-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="8b531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b531-102">SYNOPSIS</span></span>
<span data-ttu-id="8b531-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="8b531-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="8b531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b531-104">SYNTAX</span></span>

### <span data-ttu-id="8b531-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b531-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="8b531-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="8b531-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="8b531-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8b531-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="8b531-108">Datei</span><span class="sxs-lookup"><span data-stu-id="8b531-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="8b531-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b531-109">DESCRIPTION</span></span>
<span data-ttu-id="8b531-110">Das **Cmdlet "Get-AzStorageFileContent"** lädt den Inhalt einer Datei herunter und speichert ihn dann an einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="8b531-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="8b531-111">Dieses Cmdlet gibt den Inhalt der Datei nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="8b531-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="8b531-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b531-112">EXAMPLES</span></span>

### <span data-ttu-id="8b531-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="8b531-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="8b531-114">Mit diesem Befehl wird eine Datei mit dem Namen "CurrentDataFile" im Ordner "ContosoWorkingFolder" aus der Dateifreigabe "ContosoShare06" in den aktuellen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8b531-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="8b531-115">Beispiel 2: Herunterladen der Dateien unter "Beispieldateifreigabe"</span><span class="sxs-lookup"><span data-stu-id="8b531-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="8b531-116">In diesem Beispiel werden die Dateien unter "Beispieldateifreigabe" heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8b531-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="8b531-117">Beispiel 3: Laden Sie eine Azure-Datei in eine lokale Datei herunter, und reservieren Sie die Azure File -SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="8b531-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="8b531-118">In diesem Beispiel wird eine Azure-Datei in eine lokale Datei heruntergeladen, und die Azure File -SMB-Eigenschaften ("File Attributtes", "File Creation Time", "File Last Write Time") werden in der lokalen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8b531-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="8b531-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b531-119">PARAMETERS</span></span>

### <span data-ttu-id="8b531-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b531-120">-AsJob</span></span>
<span data-ttu-id="8b531-121">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="8b531-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="8b531-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="8b531-122">-CheckMd5</span></span>
<span data-ttu-id="8b531-123">Gibt an, ob die Md5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b531-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="8b531-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b531-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b531-125">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="8b531-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="8b531-126">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b531-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="8b531-127">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8b531-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b531-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b531-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b531-129">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="8b531-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="8b531-130">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="8b531-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="8b531-131">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8b531-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="8b531-132">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8b531-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="8b531-133">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8b531-133">The default value is 10.</span></span>

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

### <span data-ttu-id="8b531-134">-Context</span><span class="sxs-lookup"><span data-stu-id="8b531-134">-Context</span></span>
<span data-ttu-id="8b531-135">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="8b531-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="8b531-136">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b531-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8b531-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b531-137">-DefaultProfile</span></span>
<span data-ttu-id="8b531-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b531-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b531-139">-Destination</span><span class="sxs-lookup"><span data-stu-id="8b531-139">-Destination</span></span>
<span data-ttu-id="8b531-140">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="8b531-140">Specifies the destination path.</span></span>
<span data-ttu-id="8b531-141">Dieses Cmdlet lädt die Dateiinhalte an den von diesem Parameter angegebenen Speicherort herunter.</span><span class="sxs-lookup"><span data-stu-id="8b531-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="8b531-142">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="8b531-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="8b531-143">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und den Parameter *"Force"* angeben, überschreibt das Cmdlet die Datei.</span><span class="sxs-lookup"><span data-stu-id="8b531-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="8b531-144">Wenn Sie einen Pfad für eine vorhandene Datei und nicht "Erzwingen" *angeben,* werden Sie vom Cmdlet vor dem Fortlauf dazu aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8b531-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="8b531-145">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure -Speicherdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b531-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b531-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="8b531-146">-Directory</span></span>
<span data-ttu-id="8b531-147">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8b531-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8b531-148">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8b531-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="8b531-149">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b531-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="8b531-150">Sie können das cmdlet Get-AzStorageFile auch zum Abrufen eines Verzeichnisses verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b531-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="8b531-151">-File</span><span class="sxs-lookup"><span data-stu-id="8b531-151">-File</span></span>
<span data-ttu-id="8b531-152">Gibt eine Datei als **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8b531-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="8b531-153">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8b531-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="8b531-154">Verwenden Sie zum Abrufen eines **CloudFile-Objekts** das Get-AzStorageFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b531-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="8b531-155">-Force</span><span class="sxs-lookup"><span data-stu-id="8b531-155">-Force</span></span>
<span data-ttu-id="8b531-156">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="8b531-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="8b531-157">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und den Parameter *"Force"* angeben, überschreibt das Cmdlet die Datei.</span><span class="sxs-lookup"><span data-stu-id="8b531-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="8b531-158">Wenn Sie einen Pfad für eine vorhandene Datei und nicht "Erzwingen" *angeben,* werden Sie vom Cmdlet vor dem Fortlauf dazu aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8b531-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="8b531-159">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure -Speicherdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b531-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="8b531-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b531-160">-PassThru</span></span>
<span data-ttu-id="8b531-161">Gibt an, dass dieses Cmdlet das **heruntergeladene "AzureStorageFile"-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8b531-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="8b531-162">-Path</span><span class="sxs-lookup"><span data-stu-id="8b531-162">-Path</span></span>
<span data-ttu-id="8b531-163">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="8b531-163">Specifies the path of a file.</span></span>
<span data-ttu-id="8b531-164">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8b531-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="8b531-165">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8b531-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b531-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="8b531-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="8b531-167">Behalten Sie die Eigenschaften des Quelldatei-SMB (File Attributtes, File Creation Time, File Last Write Time) in der Zieldatei bei.</span><span class="sxs-lookup"><span data-stu-id="8b531-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="8b531-168">Dieser Parameter ist nur unter Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b531-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="8b531-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b531-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b531-170">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8b531-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="8b531-171">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8b531-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="8b531-172">-Teilen</span><span class="sxs-lookup"><span data-stu-id="8b531-172">-Share</span></span>
<span data-ttu-id="8b531-173">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8b531-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8b531-174">Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Dateifreigabe herunter.</span><span class="sxs-lookup"><span data-stu-id="8b531-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="8b531-175">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b531-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="8b531-176">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="8b531-176">This object contains the storage context.</span></span>
<span data-ttu-id="8b531-177">Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="8b531-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="8b531-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8b531-178">-ShareName</span></span>
<span data-ttu-id="8b531-179">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8b531-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="8b531-180">Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Dateifreigabe herunter.</span><span class="sxs-lookup"><span data-stu-id="8b531-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="8b531-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b531-181">-Confirm</span></span>
<span data-ttu-id="8b531-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b531-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b531-183">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8b531-183">-WhatIf</span></span>
<span data-ttu-id="8b531-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b531-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b531-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b531-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b531-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b531-186">CommonParameters</span></span>
<span data-ttu-id="8b531-187">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b531-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b531-188">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b531-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b531-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b531-189">INPUTS</span></span>

### <span data-ttu-id="8b531-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8b531-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="8b531-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8b531-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="8b531-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="8b531-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8b531-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b531-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b531-194">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b531-194">OUTPUTS</span></span>

### <span data-ttu-id="8b531-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8b531-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="8b531-196">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b531-196">NOTES</span></span>

## <span data-ttu-id="8b531-197">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b531-197">RELATED LINKS</span></span>

[<span data-ttu-id="8b531-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="8b531-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="8b531-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8b531-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


