---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290585"
---
# <span data-ttu-id="88e8f-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e8f-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="88e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="88e8f-103">Listet Verzeichnisse und Dateien für einen Pfad auf.</span><span class="sxs-lookup"><span data-stu-id="88e8f-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="88e8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88e8f-104">SYNTAX</span></span>

### <span data-ttu-id="88e8f-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="88e8f-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="88e8f-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="88e8f-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="88e8f-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="88e8f-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="88e8f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88e8f-108">DESCRIPTION</span></span>
<span data-ttu-id="88e8f-109">Das **Cmdlet "Get-AzStorageFile"** listet Verzeichnisse und Dateien für die von Ihnen festgelegte Freigabe oder das Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="88e8f-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="88e8f-110">Geben Sie den *Parameter "Path"* an, um eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88e8f-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="88e8f-111">Dieses Cmdlet gibt **die Objekte "AzureStorageFile"** und **"AzureStorageDirectory"** zurück.</span><span class="sxs-lookup"><span data-stu-id="88e8f-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="88e8f-112">Sie können die Eigenschaft **"IsDirectory"** verwenden, um zwischen Ordnern und Dateien zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="88e8f-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="88e8f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88e8f-113">EXAMPLES</span></span>

### <span data-ttu-id="88e8f-114">Beispiel 1: Listenverzeichnisse in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="88e8f-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="88e8f-115">Mit diesem Befehl werden nur die Verzeichnisse im Freigabeverzeichnis "ContosoShare06" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="88e8f-116">Es ruft zuerst Dateien und Verzeichnisse ab,  übergibt sie mithilfe des Pipelineoperators an den where-Operator und verwirft dann alle Objekte, deren Typ nicht "AzureStorageFileDirectory" ist.</span><span class="sxs-lookup"><span data-stu-id="88e8f-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="88e8f-117">Beispiel 2: Auflisten eines Dateiverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="88e8f-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="88e8f-118">Mit diesem Befehl werden die Dateien und Ordner im Verzeichnis "ContosoWorkingFolder" unter der Freigabe "ContosoShare06" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="88e8f-119">Zuerst ruft sie die Verzeichnisinstanz ab und pipelineiert sie dann an das **Cmdlet "Get-AzStorageFile",** um das Verzeichnis auflisten.</span><span class="sxs-lookup"><span data-stu-id="88e8f-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="88e8f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88e8f-120">PARAMETERS</span></span>

### <span data-ttu-id="88e8f-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88e8f-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="88e8f-122">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="88e8f-123">Wenn der vorherige Aufruf innerhalb des angegebenen Intervalls fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="88e8f-124">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="88e8f-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="88e8f-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="88e8f-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="88e8f-126">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="88e8f-127">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="88e8f-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="88e8f-128">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="88e8f-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="88e8f-129">Mit diesem Parameter können Sie Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite vermeiden, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="88e8f-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="88e8f-130">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="88e8f-130">The default value is 10.</span></span>

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

### <span data-ttu-id="88e8f-131">-Context</span><span class="sxs-lookup"><span data-stu-id="88e8f-131">-Context</span></span>
<span data-ttu-id="88e8f-132">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="88e8f-133">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e8f-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="88e8f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e8f-134">-DefaultProfile</span></span>
<span data-ttu-id="88e8f-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88e8f-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e8f-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="88e8f-136">-Directory</span></span>
<span data-ttu-id="88e8f-137">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="88e8f-138">Dieses Cmdlet ruft den Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="88e8f-139">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e8f-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="88e8f-140">Sie können auch das **Cmdlet "Get-AzStorageFile"** verwenden, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88e8f-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="88e8f-141">-Path</span><span class="sxs-lookup"><span data-stu-id="88e8f-141">-Path</span></span>
<span data-ttu-id="88e8f-142">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="88e8f-143">Wenn Sie den Parameter *"Path"* weglassen, listet **"Get-AzStorageFile"** die Verzeichnisse und Dateien in der angegebenen Dateifreigabe oder dem angegebenen Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="88e8f-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="88e8f-144">Wenn Sie den Parameter *"Path"* angeben, gibt **"Get-AzStorageFile"** eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="88e8f-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="88e8f-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88e8f-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="88e8f-146">Gibt das dienstseitige Timeoutintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="88e8f-147">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="88e8f-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="88e8f-148">-Teilen</span><span class="sxs-lookup"><span data-stu-id="88e8f-148">-Share</span></span>
<span data-ttu-id="88e8f-149">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="88e8f-150">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="88e8f-151">Verwenden Sie zum Abrufen **eines CloudFileShare-Objekts** das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e8f-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="88e8f-152">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="88e8f-152">This object contains the Storage context.</span></span>
<span data-ttu-id="88e8f-153">Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="88e8f-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="88e8f-154">-ShareName</span></span>
<span data-ttu-id="88e8f-155">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="88e8f-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="88e8f-156">Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="88e8f-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="88e8f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e8f-157">CommonParameters</span></span>
<span data-ttu-id="88e8f-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e8f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e8f-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e8f-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e8f-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88e8f-160">INPUTS</span></span>

### <span data-ttu-id="88e8f-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="88e8f-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="88e8f-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="88e8f-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="88e8f-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e8f-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88e8f-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88e8f-164">OUTPUTS</span></span>

### <span data-ttu-id="88e8f-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e8f-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="88e8f-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88e8f-166">NOTES</span></span>

## <span data-ttu-id="88e8f-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88e8f-167">RELATED LINKS</span></span>

[<span data-ttu-id="88e8f-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="88e8f-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="88e8f-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="88e8f-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="88e8f-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="88e8f-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="88e8f-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="88e8f-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="88e8f-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="88e8f-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


