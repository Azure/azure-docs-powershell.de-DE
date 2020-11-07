---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 0777c24aa5cb9b505ffc3495c9a9220da912f055
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658865"
---
# <span data-ttu-id="d2f36-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d2f36-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="d2f36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2f36-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f36-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="d2f36-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="d2f36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f36-104">SYNTAX</span></span>

### <span data-ttu-id="d2f36-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2f36-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f36-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="d2f36-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2f36-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d2f36-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f36-108">Datei</span><span class="sxs-lookup"><span data-stu-id="d2f36-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2f36-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2f36-109">DESCRIPTION</span></span>
<span data-ttu-id="d2f36-110">Das Cmdlet " **Get-AzStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="d2f36-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="d2f36-111">Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="d2f36-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="d2f36-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2f36-112">EXAMPLES</span></span>

### <span data-ttu-id="d2f36-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="d2f36-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="d2f36-114">Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d2f36-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="d2f36-115">Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="d2f36-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="d2f36-116">In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="d2f36-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="d2f36-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2f36-117">PARAMETERS</span></span>

### <span data-ttu-id="d2f36-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f36-118">-AsJob</span></span>
<span data-ttu-id="d2f36-119">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="d2f36-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d2f36-120">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="d2f36-120">-CheckMd5</span></span>
<span data-ttu-id="d2f36-121">Gibt an, ob die MD5-Summe für die heruntergeladene Datei überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2f36-121">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="d2f36-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2f36-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d2f36-123">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="d2f36-124">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="d2f36-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="d2f36-125">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d2f36-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d2f36-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d2f36-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d2f36-127">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-127">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="d2f36-128">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="d2f36-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="d2f36-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d2f36-129">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="d2f36-130">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d2f36-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="d2f36-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d2f36-131">The default value is 10.</span></span>

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

### <span data-ttu-id="d2f36-132">-Context</span><span class="sxs-lookup"><span data-stu-id="d2f36-132">-Context</span></span>
<span data-ttu-id="d2f36-133">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-133">Specifies an Azure Storage context.</span></span> <span data-ttu-id="d2f36-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f36-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d2f36-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f36-135">-DefaultProfile</span></span>
<span data-ttu-id="d2f36-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2f36-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f36-137">-Ziel</span><span class="sxs-lookup"><span data-stu-id="d2f36-137">-Destination</span></span>
<span data-ttu-id="d2f36-138">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-138">Specifies the destination path.</span></span>
<span data-ttu-id="d2f36-139">Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d2f36-139">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="d2f36-140">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d2f36-140">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d2f36-141">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d2f36-141">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d2f36-142">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f36-142">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d2f36-143">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d2f36-143">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d2f36-144">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d2f36-144">-Directory</span></span>
<span data-ttu-id="d2f36-145">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-145">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d2f36-146">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d2f36-146">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="d2f36-147">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2f36-147">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d2f36-148">Sie können auch das Get-AzStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d2f36-148">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f36-149">-Datei</span><span class="sxs-lookup"><span data-stu-id="d2f36-149">-File</span></span>
<span data-ttu-id="d2f36-150">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-150">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="d2f36-151">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d2f36-151">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="d2f36-152">Verwenden Sie das Get-AzStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2f36-152">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f36-153">-Force</span><span class="sxs-lookup"><span data-stu-id="d2f36-153">-Force</span></span>
<span data-ttu-id="d2f36-154">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d2f36-154">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d2f36-155">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d2f36-155">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d2f36-156">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f36-156">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d2f36-157">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d2f36-157">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d2f36-158">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f36-158">-PassThru</span></span>
<span data-ttu-id="d2f36-159">Gibt an, dass dieses Cmdlet das **AzureStorageFile** -Objekt zurückgibt, das heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="d2f36-159">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="d2f36-160">-Path</span><span class="sxs-lookup"><span data-stu-id="d2f36-160">-Path</span></span>
<span data-ttu-id="d2f36-161">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-161">Specifies the path of a file.</span></span>
<span data-ttu-id="d2f36-162">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d2f36-162">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="d2f36-163">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d2f36-163">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d2f36-164">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2f36-164">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d2f36-165">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-165">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="d2f36-166">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d2f36-166">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d2f36-167">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="d2f36-167">-Share</span></span>
<span data-ttu-id="d2f36-168">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-168">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d2f36-169">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d2f36-169">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="d2f36-170">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2f36-170">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d2f36-171">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="d2f36-171">This object contains the storage context.</span></span>
<span data-ttu-id="d2f36-172">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-172">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f36-173">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d2f36-173">-ShareName</span></span>
<span data-ttu-id="d2f36-174">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="d2f36-174">Specifies the name of the file share.</span></span>
<span data-ttu-id="d2f36-175">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d2f36-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="d2f36-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2f36-176">-Confirm</span></span>
<span data-ttu-id="d2f36-177">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2f36-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f36-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f36-178">-WhatIf</span></span>
<span data-ttu-id="d2f36-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f36-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f36-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2f36-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f36-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f36-181">CommonParameters</span></span>
<span data-ttu-id="d2f36-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f36-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f36-183">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f36-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f36-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2f36-184">INPUTS</span></span>

### <span data-ttu-id="d2f36-185">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d2f36-185">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d2f36-186">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d2f36-186">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d2f36-187">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="d2f36-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="d2f36-188">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2f36-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d2f36-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2f36-189">OUTPUTS</span></span>

### <span data-ttu-id="d2f36-190">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="d2f36-190">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="d2f36-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2f36-191">NOTES</span></span>

## <span data-ttu-id="d2f36-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2f36-192">RELATED LINKS</span></span>

[<span data-ttu-id="d2f36-193">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d2f36-193">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="d2f36-194">Satz-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d2f36-194">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


