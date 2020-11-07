---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 5d73923dd3de630673d9228461397ec1789bd268
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826492"
---
# <span data-ttu-id="bd63c-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bd63c-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="bd63c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd63c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd63c-103">Listet Verzeichnisse und Dateien für einen Pfad auf.</span><span class="sxs-lookup"><span data-stu-id="bd63c-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="bd63c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd63c-104">SYNTAX</span></span>

### <span data-ttu-id="bd63c-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd63c-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bd63c-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="bd63c-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd63c-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="bd63c-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd63c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd63c-108">DESCRIPTION</span></span>
<span data-ttu-id="bd63c-109">Das Cmdlet " **Get-AzStorageFile** " listet Verzeichnisse und Dateien für die von Ihnen angegebene Freigabe oder das Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="bd63c-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="bd63c-110">Geben Sie den *path* -Parameter an, um eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd63c-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="bd63c-111">Dieses Cmdlet gibt **AzureStorageFile** -und **AzureStorageDirectory** -Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="bd63c-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="bd63c-112">Sie können die **IsDirectory** -Eigenschaft verwenden, um zwischen Ordnern und Dateien zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="bd63c-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="bd63c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd63c-113">EXAMPLES</span></span>

### <span data-ttu-id="bd63c-114">Beispiel 1: Auflisten von Verzeichnissen in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="bd63c-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="bd63c-115">Dieser Befehl listet nur die Verzeichnisse in der Freigabe-ContosoShare06 auf.</span><span class="sxs-lookup"><span data-stu-id="bd63c-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="bd63c-116">Sie ruft zunächst beide Dateien und Verzeichnisse ab, übergibt Sie mithilfe des Pipelineoperators an den **Where** -Operator und verwirft dann alle Objekte, deren Typ nicht "CloudFileDirectory" ist.</span><span class="sxs-lookup"><span data-stu-id="bd63c-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="bd63c-117">Beispiel 2: Auflisten eines Dateiverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="bd63c-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="bd63c-118">Dieser Befehl listet die Dateien und Ordner im Verzeichnis ContosoWorkingFolder unter der Freigabe ContosoShare06 auf.</span><span class="sxs-lookup"><span data-stu-id="bd63c-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="bd63c-119">Zuerst wird die Verzeichnisinstanz abgerufen und anschließend an das Cmdlet " **Get-AzStorageFile** " weitergeleitet, um das Verzeichnis aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="bd63c-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="bd63c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd63c-120">PARAMETERS</span></span>

### <span data-ttu-id="bd63c-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd63c-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bd63c-122">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bd63c-123">Wenn der vorherige Aufruf innerhalb des angegebenen Intervalls fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="bd63c-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bd63c-124">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bd63c-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bd63c-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bd63c-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bd63c-126">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bd63c-127">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="bd63c-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bd63c-128">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="bd63c-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bd63c-129">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="bd63c-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bd63c-130">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="bd63c-130">The default value is 10.</span></span>

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

### <span data-ttu-id="bd63c-131">-Context</span><span class="sxs-lookup"><span data-stu-id="bd63c-131">-Context</span></span>
<span data-ttu-id="bd63c-132">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bd63c-133">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd63c-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bd63c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd63c-134">-DefaultProfile</span></span>
<span data-ttu-id="bd63c-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd63c-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd63c-136">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="bd63c-136">-Directory</span></span>
<span data-ttu-id="bd63c-137">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="bd63c-138">Dieses Cmdlet ruft den Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bd63c-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="bd63c-139">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd63c-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="bd63c-140">Sie können auch das Cmdlet **Get-AzStorageFile** verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bd63c-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63c-141">-Path</span><span class="sxs-lookup"><span data-stu-id="bd63c-141">-Path</span></span>
<span data-ttu-id="bd63c-142">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="bd63c-143">Wenn Sie den *path* -Parameter nicht angeben, listet **Get-AzStorageFile** die Verzeichnisse und Dateien in der angegebenen Dateifreigabe oder dem angegebenen Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="bd63c-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="bd63c-144">Wenn Sie den *path* -Parameter einbeziehen, gibt **Get-AzStorageFile** eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bd63c-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd63c-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bd63c-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bd63c-146">Gibt das dienstseitige Timeoutintervall für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="bd63c-147">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="bd63c-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="bd63c-148">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="bd63c-148">-Share</span></span>
<span data-ttu-id="bd63c-149">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="bd63c-150">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bd63c-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="bd63c-151">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd63c-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="bd63c-152">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="bd63c-152">This object contains the Storage context.</span></span>
<span data-ttu-id="bd63c-153">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd63c-154">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="bd63c-154">-ShareName</span></span>
<span data-ttu-id="bd63c-155">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="bd63c-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="bd63c-156">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="bd63c-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="bd63c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd63c-157">CommonParameters</span></span>
<span data-ttu-id="bd63c-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd63c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd63c-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd63c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd63c-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd63c-160">INPUTS</span></span>

### <span data-ttu-id="bd63c-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="bd63c-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="bd63c-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="bd63c-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="bd63c-163">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bd63c-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bd63c-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd63c-164">OUTPUTS</span></span>

### <span data-ttu-id="bd63c-165">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="bd63c-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="bd63c-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd63c-166">NOTES</span></span>

## <span data-ttu-id="bd63c-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd63c-167">RELATED LINKS</span></span>

[<span data-ttu-id="bd63c-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bd63c-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="bd63c-169">Neu – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bd63c-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="bd63c-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="bd63c-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="bd63c-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="bd63c-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="bd63c-172">Satz-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="bd63c-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


