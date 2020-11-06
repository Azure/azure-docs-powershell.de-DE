---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: bc83da1cd177585b76d68eb0b55cdd15120ff22e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496741"
---
# <span data-ttu-id="a173a-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a173a-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="a173a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a173a-102">SYNOPSIS</span></span>
<span data-ttu-id="a173a-103">Erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="a173a-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a173a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a173a-104">SYNTAX</span></span>

### <span data-ttu-id="a173a-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="a173a-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="a173a-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="a173a-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a173a-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="a173a-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a173a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a173a-108">DESCRIPTION</span></span>
<span data-ttu-id="a173a-109">Das Cmdlet **New-AzureStorageDirectory** erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="a173a-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="a173a-110">Dieses Cmdlet gibt ein **CloudFileDirectory** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a173a-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="a173a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a173a-111">EXAMPLES</span></span>

### <span data-ttu-id="a173a-112">Beispiel 1: Erstellen eines Ordners in einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="a173a-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a173a-113">Dieser Befehl erstellt einen Ordner mit dem Namen ContosoWorkingFolder in der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a173a-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a173a-114">Beispiel 2: Erstellen eines Ordners in einer Dateifreigabe, die in einem Dateifreigabe Objekt angegeben ist</span><span class="sxs-lookup"><span data-stu-id="a173a-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="a173a-115">Dieser Befehl verwendet das Cmdlet " **Get-AzureStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a173a-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a173a-116">Das aktuelle Cmdlet erstellt den Ordner mit dem Namen ContosoWorkingFolder in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a173a-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="a173a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a173a-117">PARAMETERS</span></span>

### <span data-ttu-id="a173a-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a173a-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a173a-119">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a173a-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a173a-120">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="a173a-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a173a-121">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a173a-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a173a-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a173a-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a173a-123">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="a173a-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a173a-124">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="a173a-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a173a-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a173a-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a173a-126">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a173a-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a173a-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a173a-127">The default value is 10.</span></span>

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

### <span data-ttu-id="a173a-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a173a-128">-Context</span></span>
<span data-ttu-id="a173a-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a173a-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a173a-130">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a173a-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a173a-131">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="a173a-131">-Directory</span></span>
<span data-ttu-id="a173a-132">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a173a-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="a173a-133">Mit diesem Cmdlet wird der Ordner an dem Speicherort erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a173a-133">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="a173a-134">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a173a-134">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="a173a-135">Sie können auch das Get-AzureStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a173a-135">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="a173a-136">-Path</span><span class="sxs-lookup"><span data-stu-id="a173a-136">-Path</span></span>
<span data-ttu-id="a173a-137">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="a173a-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="a173a-138">Dieses Cmdlet erstellt einen Ordner für den von diesem Cmdlet festgelegten Pfad.</span><span class="sxs-lookup"><span data-stu-id="a173a-138">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a173a-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a173a-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a173a-140">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="a173a-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a173a-141">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="a173a-141">-Share</span></span>
<span data-ttu-id="a173a-142">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a173a-142">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a173a-143">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a173a-143">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="a173a-144">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a173a-144">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a173a-145">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="a173a-145">This object contains the storage context.</span></span>
<span data-ttu-id="a173a-146">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="a173a-146">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a173a-147">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="a173a-147">-ShareName</span></span>
<span data-ttu-id="a173a-148">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="a173a-148">Specifies the name of the file share.</span></span>
<span data-ttu-id="a173a-149">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a173a-149">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="a173a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a173a-150">CommonParameters</span></span>
<span data-ttu-id="a173a-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a173a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a173a-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a173a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a173a-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a173a-153">INPUTS</span></span>

### <span data-ttu-id="a173a-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a173a-154">IStorageContext</span></span>

<span data-ttu-id="a173a-155">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a173a-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a173a-156">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="a173a-156">CloudFileDirectory</span></span>

<span data-ttu-id="a173a-157">Der Parameter "Verzeichnis" akzeptiert den Wert vom Typ "CloudFileDirectory" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a173a-157">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="a173a-158">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a173a-158">String</span></span>

<span data-ttu-id="a173a-159">Der Parameter "Path" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a173a-159">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="a173a-160">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a173a-160">CloudFileShare</span></span>

<span data-ttu-id="a173a-161">Der Parameter "Share" akzeptiert den Wert vom Typ "CloudFileShare" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a173a-161">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="a173a-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a173a-162">OUTPUTS</span></span>

## <span data-ttu-id="a173a-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="a173a-163">NOTES</span></span>

## <span data-ttu-id="a173a-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a173a-164">RELATED LINKS</span></span>

[<span data-ttu-id="a173a-165">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="a173a-165">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="a173a-166">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a173a-166">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a173a-167">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a173a-167">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a173a-168">Neu – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a173a-168">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="a173a-169">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="a173a-169">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)
