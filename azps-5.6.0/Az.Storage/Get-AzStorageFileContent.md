---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 33fcfabb50b0b4af73fe7111c587ac88e746598e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933371"
---
# <span data-ttu-id="2ce7c-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ce7c-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="2ce7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ce7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce7c-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="2ce7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ce7c-104">SYNTAX</span></span>

### <span data-ttu-id="2ce7c-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ce7c-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2ce7c-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="2ce7c-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2ce7c-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="2ce7c-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="2ce7c-108">Datei</span><span class="sxs-lookup"><span data-stu-id="2ce7c-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="2ce7c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ce7c-109">DESCRIPTION</span></span>
<span data-ttu-id="2ce7c-110">Das **Get-AzStorageFileContent-Cmdlet** lädt den Inhalt einer Datei herunter und speichert sie dann an einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="2ce7c-111">Dieses Cmdlet gibt den Inhalt der Datei nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="2ce7c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2ce7c-112">EXAMPLES</span></span>

### <span data-ttu-id="2ce7c-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="2ce7c-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="2ce7c-114">Mit diesem Befehl wird eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="2ce7c-115">Beispiel 2: Lädt die Dateien unter Beispieldateifreigabe herunter.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="2ce7c-116">In diesem Beispiel werden die Dateien unter Beispieldateifreigabe heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="2ce7c-117">Beispiel 3: Laden Sie eine Azure-Datei in eine lokale Datei herunter, und speichern Sie die Azure File SMB-Eigenschaften (Dateiattate, Dateierstellungszeit, Letzte Schreibzeit der Datei) in der lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="2ce7c-118">In diesem Beispiel wird eine Azure-Datei in eine lokale Datei heruntergeladen und die Azure File SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der lokalen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="2ce7c-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2ce7c-119">PARAMETERS</span></span>

### <span data-ttu-id="2ce7c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ce7c-120">-AsJob</span></span>
<span data-ttu-id="2ce7c-121">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="2ce7c-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="2ce7c-122">-CheckMd5</span></span>
<span data-ttu-id="2ce7c-123">Gibt an, ob die Md5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="2ce7c-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ce7c-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2ce7c-125">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="2ce7c-126">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="2ce7c-127">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2ce7c-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2ce7c-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2ce7c-129">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="2ce7c-130">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="2ce7c-131">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="2ce7c-132">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="2ce7c-133">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-133">The default value is 10.</span></span>

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

### <span data-ttu-id="2ce7c-134">-Context</span><span class="sxs-lookup"><span data-stu-id="2ce7c-134">-Context</span></span>
<span data-ttu-id="2ce7c-135">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="2ce7c-136">Verwenden Sie das cmdlet New-AzStorageContext, um einen Kontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2ce7c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce7c-137">-DefaultProfile</span></span>
<span data-ttu-id="2ce7c-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce7c-139">-Ziel</span><span class="sxs-lookup"><span data-stu-id="2ce7c-139">-Destination</span></span>
<span data-ttu-id="2ce7c-140">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-140">Specifies the destination path.</span></span>
<span data-ttu-id="2ce7c-141">Dieses Cmdlet lädt den Dateiinhalt an den Von diesem Parameter angegebenen Speicherort herunter.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="2ce7c-142">Wenn Sie den Pfad einer datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2ce7c-143">Wenn Sie einen Pfad einer bereits vorhandenen  Datei angeben und den Parameter Erzwingen angeben, überschreibt das Cmdlet die Datei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2ce7c-144">Wenn Sie einen Pfad einer vorhandenen Datei angeben und nicht Erzwingen *angeben,* werden Sie vom Cmdlet aufgefordert, bevor es fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="2ce7c-145">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure-Speicherdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2ce7c-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="2ce7c-146">-Directory</span></span>
<span data-ttu-id="2ce7c-147">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="2ce7c-148">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="2ce7c-149">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="2ce7c-150">Sie können auch das cmdlet Get-AzStorageFile, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="2ce7c-151">-Datei</span><span class="sxs-lookup"><span data-stu-id="2ce7c-151">-File</span></span>
<span data-ttu-id="2ce7c-152">Gibt eine Datei als **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="2ce7c-153">Dieses Cmdlet ruft die Datei ab, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="2ce7c-154">Zum Abrufen eines **CloudFile-Objekts** verwenden Sie das Get-AzStorageFile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="2ce7c-155">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2ce7c-155">-Force</span></span>
<span data-ttu-id="2ce7c-156">Wenn Sie den Pfad einer datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="2ce7c-157">Wenn Sie einen Pfad einer bereits vorhandenen  Datei angeben und den Parameter Erzwingen angeben, überschreibt das Cmdlet die Datei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="2ce7c-158">Wenn Sie einen Pfad einer vorhandenen Datei angeben und nicht Erzwingen *angeben,* werden Sie vom Cmdlet aufgefordert, bevor es fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="2ce7c-159">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure-Speicherdatei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="2ce7c-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ce7c-160">-PassThru</span></span>
<span data-ttu-id="2ce7c-161">Gibt an, dass dieses Cmdlet das **heruntergeladene AzureStorageFile-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="2ce7c-162">-Path</span><span class="sxs-lookup"><span data-stu-id="2ce7c-162">-Path</span></span>
<span data-ttu-id="2ce7c-163">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-163">Specifies the path of a file.</span></span>
<span data-ttu-id="2ce7c-164">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="2ce7c-165">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2ce7c-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="2ce7c-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="2ce7c-167">Behalten Sie die Quelleigenschaften von File SMB (File Attributtes, File Creation Time, File Last Write Time) in der Zieldatei bei.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="2ce7c-168">Dieser Parameter ist nur unter Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="2ce7c-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2ce7c-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2ce7c-170">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="2ce7c-171">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2ce7c-172">-Teilen</span><span class="sxs-lookup"><span data-stu-id="2ce7c-172">-Share</span></span>
<span data-ttu-id="2ce7c-173">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="2ce7c-174">Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Freigabe herunter.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="2ce7c-175">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="2ce7c-176">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-176">This object contains the storage context.</span></span>
<span data-ttu-id="2ce7c-177">Wenn Sie diesen Parameter angeben, geben Sie den Parameter *Kontext nicht* an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="2ce7c-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2ce7c-178">-ShareName</span></span>
<span data-ttu-id="2ce7c-179">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="2ce7c-180">Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Freigabe herunter.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="2ce7c-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ce7c-181">-Confirm</span></span>
<span data-ttu-id="2ce7c-182">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce7c-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce7c-183">-WhatIf</span></span>
<span data-ttu-id="2ce7c-184">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce7c-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce7c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce7c-186">CommonParameters</span></span>
<span data-ttu-id="2ce7c-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce7c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce7c-188">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce7c-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce7c-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2ce7c-189">INPUTS</span></span>

### <span data-ttu-id="2ce7c-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2ce7c-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="2ce7c-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="2ce7c-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="2ce7c-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="2ce7c-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="2ce7c-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2ce7c-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2ce7c-194">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2ce7c-194">OUTPUTS</span></span>

### <span data-ttu-id="2ce7c-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="2ce7c-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="2ce7c-196">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2ce7c-196">NOTES</span></span>

## <span data-ttu-id="2ce7c-197">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2ce7c-197">RELATED LINKS</span></span>

[<span data-ttu-id="2ce7c-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="2ce7c-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="2ce7c-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2ce7c-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


