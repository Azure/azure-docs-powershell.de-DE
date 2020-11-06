---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3b84deae0307114efa274cdfa6fc708d1b268ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475685"
---
# <span data-ttu-id="25a61-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="25a61-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="25a61-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25a61-102">SYNOPSIS</span></span>
<span data-ttu-id="25a61-103">Listet Verzeichnisse und Dateien für einen Pfad auf.</span><span class="sxs-lookup"><span data-stu-id="25a61-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="25a61-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25a61-104">SYNTAX</span></span>

### <span data-ttu-id="25a61-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="25a61-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="25a61-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="25a61-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="25a61-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="25a61-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="25a61-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25a61-108">DESCRIPTION</span></span>
<span data-ttu-id="25a61-109">Das Cmdlet " **Get-AzureStorageFile** " listet Verzeichnisse und Dateien für die von Ihnen angegebene Freigabe oder das Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="25a61-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="25a61-110">Geben Sie den *path* -Parameter an, um eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25a61-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="25a61-111">Dieses Cmdlet gibt **AzureStorageFile** -und **AzureStorageDirectory** -Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="25a61-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="25a61-112">Sie können die **IsDirectory** -Eigenschaft verwenden, um zwischen Ordnern und Dateien zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="25a61-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="25a61-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25a61-113">EXAMPLES</span></span>

### <span data-ttu-id="25a61-114">Beispiel 1: Auflisten von Verzeichnissen in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="25a61-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "share1" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="25a61-115">Dieser Befehl listet nur die Verzeichnisse in der Freigabe-ContosoShare06 auf.</span><span class="sxs-lookup"><span data-stu-id="25a61-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="25a61-116">Sie ruft zunächst beide Dateien und Verzeichnisse ab, übergibt Sie mithilfe des Pipelineoperators an den **Where** -Operator und verwirft dann alle Objekte, deren Typ nicht "CloudFileDirectory" ist.</span><span class="sxs-lookup"><span data-stu-id="25a61-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="25a61-117">Beispiel 2: Auflisten eines Dateiverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="25a61-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="25a61-118">Dieser Befehl listet die Dateien und Ordner im Verzeichnis ContosoWorkingFolder unter der Freigabe ContosoShare06 auf.</span><span class="sxs-lookup"><span data-stu-id="25a61-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="25a61-119">Zuerst wird die Verzeichnisinstanz abgerufen und anschließend an das Cmdlet " **Get-AzureStorageFile** " weitergeleitet, um das Verzeichnis aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="25a61-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="25a61-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="25a61-120">PARAMETERS</span></span>

### <span data-ttu-id="25a61-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="25a61-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="25a61-122">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="25a61-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="25a61-123">Wenn der vorherige Aufruf innerhalb des angegebenen Intervalls fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="25a61-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="25a61-124">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="25a61-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="25a61-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="25a61-126">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="25a61-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="25a61-127">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="25a61-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="25a61-128">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="25a61-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="25a61-129">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="25a61-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="25a61-130">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="25a61-130">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-131">-Context</span><span class="sxs-lookup"><span data-stu-id="25a61-131">-Context</span></span>
<span data-ttu-id="25a61-132">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="25a61-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="25a61-133">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25a61-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-134">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="25a61-134">-Directory</span></span>
<span data-ttu-id="25a61-135">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="25a61-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="25a61-136">Dieses Cmdlet ruft den Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="25a61-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="25a61-137">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25a61-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="25a61-138">Sie können auch das Cmdlet **Get-AzureStorageFile** verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25a61-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-139">-Path</span><span class="sxs-lookup"><span data-stu-id="25a61-139">-Path</span></span>
<span data-ttu-id="25a61-140">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="25a61-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="25a61-141">Wenn Sie den *path* -Parameter nicht angeben, listet **Get-AzureStorageFile** die Verzeichnisse und Dateien in der angegebenen Dateifreigabe oder dem angegebenen Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="25a61-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="25a61-142">Wenn Sie den *path* -Parameter einbeziehen, gibt **Get-AzureStorageFile** eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="25a61-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="25a61-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="25a61-144">Gibt das dienstseitige Timeoutintervall für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="25a61-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="25a61-145">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="25a61-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-146">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="25a61-146">-Share</span></span>
<span data-ttu-id="25a61-147">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="25a61-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="25a61-148">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="25a61-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="25a61-149">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="25a61-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="25a61-150">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="25a61-150">This object contains the Storage context.</span></span>
<span data-ttu-id="25a61-151">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="25a61-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-152">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="25a61-152">-ShareName</span></span>
<span data-ttu-id="25a61-153">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="25a61-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="25a61-154">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="25a61-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25a61-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a61-155">CommonParameters</span></span>
<span data-ttu-id="25a61-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25a61-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a61-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25a61-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a61-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25a61-158">INPUTS</span></span>

## <span data-ttu-id="25a61-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25a61-159">OUTPUTS</span></span>

## <span data-ttu-id="25a61-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="25a61-160">NOTES</span></span>

## <span data-ttu-id="25a61-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25a61-161">RELATED LINKS</span></span>

[<span data-ttu-id="25a61-162">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="25a61-162">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="25a61-163">Neu – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="25a61-163">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="25a61-164">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="25a61-164">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="25a61-165">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="25a61-165">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="25a61-166">Satz-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="25a61-166">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


