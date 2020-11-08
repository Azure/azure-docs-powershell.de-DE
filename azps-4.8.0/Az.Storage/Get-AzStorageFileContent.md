---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010386"
---
# <span data-ttu-id="849d1-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="849d1-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="849d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="849d1-102">SYNOPSIS</span></span>
<span data-ttu-id="849d1-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="849d1-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="849d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="849d1-104">SYNTAX</span></span>

### <span data-ttu-id="849d1-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="849d1-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="849d1-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="849d1-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="849d1-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="849d1-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="849d1-108">Datei</span><span class="sxs-lookup"><span data-stu-id="849d1-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="849d1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="849d1-109">DESCRIPTION</span></span>
<span data-ttu-id="849d1-110">Das Cmdlet " **Get-AzStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="849d1-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="849d1-111">Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="849d1-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="849d1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="849d1-112">EXAMPLES</span></span>

### <span data-ttu-id="849d1-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="849d1-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="849d1-114">Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="849d1-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="849d1-115">Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="849d1-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="849d1-116">In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="849d1-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="849d1-117">Beispiel 3: Laden Sie eine Azure-Datei in eine lokale Datei herunter, und der automatische Systtem Sie die Azure-Datei SMB-Eigenschaften (Datei Attributtes, dateierstellungszeit, Datei zum letzten Schreib Zeitpunkt) in der lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="849d1-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="849d1-118">In diesem Beispiel wird eine Azure-Datei in eine lokale Datei heruntergeladen und die perserves SMB-Eigenschaften (Datei Attributtes, dateierstellungszeit, Datei zum letzten Schreib Zeitpunkt) in der lokalen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="849d1-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="849d1-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="849d1-119">PARAMETERS</span></span>

### <span data-ttu-id="849d1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="849d1-120">-AsJob</span></span>
<span data-ttu-id="849d1-121">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="849d1-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="849d1-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="849d1-122">-CheckMd5</span></span>
<span data-ttu-id="849d1-123">Gibt an, ob die MD5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="849d1-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="849d1-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="849d1-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="849d1-125">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="849d1-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="849d1-126">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="849d1-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="849d1-127">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="849d1-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="849d1-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="849d1-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="849d1-129">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="849d1-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="849d1-130">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="849d1-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="849d1-131">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="849d1-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="849d1-132">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="849d1-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="849d1-133">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="849d1-133">The default value is 10.</span></span>

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

### <span data-ttu-id="849d1-134">-Context</span><span class="sxs-lookup"><span data-stu-id="849d1-134">-Context</span></span>
<span data-ttu-id="849d1-135">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="849d1-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="849d1-136">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="849d1-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="849d1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849d1-137">-DefaultProfile</span></span>
<span data-ttu-id="849d1-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="849d1-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849d1-139">-Ziel</span><span class="sxs-lookup"><span data-stu-id="849d1-139">-Destination</span></span>
<span data-ttu-id="849d1-140">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="849d1-140">Specifies the destination path.</span></span>
<span data-ttu-id="849d1-141">Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="849d1-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="849d1-142">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="849d1-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="849d1-143">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="849d1-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="849d1-144">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="849d1-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="849d1-145">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="849d1-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="849d1-146">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="849d1-146">-Directory</span></span>
<span data-ttu-id="849d1-147">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="849d1-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="849d1-148">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="849d1-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="849d1-149">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="849d1-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="849d1-150">Sie können auch das Get-AzStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="849d1-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="849d1-151">-Datei</span><span class="sxs-lookup"><span data-stu-id="849d1-151">-File</span></span>
<span data-ttu-id="849d1-152">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="849d1-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="849d1-153">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="849d1-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="849d1-154">Verwenden Sie das Get-AzStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="849d1-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="849d1-155">-Force</span><span class="sxs-lookup"><span data-stu-id="849d1-155">-Force</span></span>
<span data-ttu-id="849d1-156">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="849d1-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="849d1-157">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="849d1-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="849d1-158">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="849d1-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="849d1-159">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="849d1-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="849d1-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="849d1-160">-PassThru</span></span>
<span data-ttu-id="849d1-161">Gibt an, dass dieses Cmdlet das **AzureStorageFile** -Objekt zurückgibt, das heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="849d1-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="849d1-162">-Path</span><span class="sxs-lookup"><span data-stu-id="849d1-162">-Path</span></span>
<span data-ttu-id="849d1-163">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="849d1-163">Specifies the path of a file.</span></span>
<span data-ttu-id="849d1-164">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="849d1-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="849d1-165">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="849d1-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="849d1-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="849d1-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="849d1-167">Speichern Sie die SMB-Eigenschaften der Quelldatei (Datei Attributtes, dateierstellungszeit, Datei zum letzten Schreib Zeitpunkt) in der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="849d1-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="849d1-168">Dieser Parameter steht nur unter Windows zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="849d1-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="849d1-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="849d1-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="849d1-170">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="849d1-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="849d1-171">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="849d1-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="849d1-172">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="849d1-172">-Share</span></span>
<span data-ttu-id="849d1-173">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="849d1-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="849d1-174">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="849d1-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="849d1-175">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="849d1-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="849d1-176">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="849d1-176">This object contains the storage context.</span></span>
<span data-ttu-id="849d1-177">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="849d1-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="849d1-178">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="849d1-178">-ShareName</span></span>
<span data-ttu-id="849d1-179">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="849d1-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="849d1-180">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="849d1-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="849d1-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="849d1-181">-Confirm</span></span>
<span data-ttu-id="849d1-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="849d1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="849d1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849d1-183">-WhatIf</span></span>
<span data-ttu-id="849d1-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="849d1-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849d1-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="849d1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="849d1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849d1-186">CommonParameters</span></span>
<span data-ttu-id="849d1-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849d1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849d1-188">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849d1-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849d1-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="849d1-189">INPUTS</span></span>

### <span data-ttu-id="849d1-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="849d1-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="849d1-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="849d1-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="849d1-192">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="849d1-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="849d1-193">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="849d1-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="849d1-194">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="849d1-194">OUTPUTS</span></span>

### <span data-ttu-id="849d1-195">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="849d1-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="849d1-196">Notizen</span><span class="sxs-lookup"><span data-stu-id="849d1-196">NOTES</span></span>

## <span data-ttu-id="849d1-197">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="849d1-197">RELATED LINKS</span></span>

[<span data-ttu-id="849d1-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="849d1-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="849d1-199">Satz-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="849d1-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


