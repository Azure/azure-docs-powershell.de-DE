---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: fba71dbac836fb6cc6551982945135e8e9410744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478817"
---
# <span data-ttu-id="0595d-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="0595d-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="0595d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0595d-102">SYNOPSIS</span></span>
<span data-ttu-id="0595d-103">Ruft den Kopierstatus eines Azure Storage-BLOBs ab.</span><span class="sxs-lookup"><span data-stu-id="0595d-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0595d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0595d-104">SYNTAX</span></span>

### <span data-ttu-id="0595d-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="0595d-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0595d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0595d-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0595d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0595d-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0595d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0595d-108">DESCRIPTION</span></span>
<span data-ttu-id="0595d-109">Das Cmdlet " **Get-AzureStorageBlobCopyState** " Ruft den Kopierstatus eines Azure Storage-BLOBs ab.</span><span class="sxs-lookup"><span data-stu-id="0595d-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="0595d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0595d-110">EXAMPLES</span></span>

### <span data-ttu-id="0595d-111">Beispiel 1: Abrufen des Kopierstatus eines BLOB</span><span class="sxs-lookup"><span data-stu-id="0595d-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="0595d-112">Dieser Befehl ruft den Kopierstatus des BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads ab.</span><span class="sxs-lookup"><span data-stu-id="0595d-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="0595d-113">Beispiel 2: Abrufen des Kopierstatus für ein BLOB mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="0595d-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="0595d-114">Dieser Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads mit dem Cmdlet **Get-AzureStorageBlob** ab und übergibt dann das Ergebnis mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0595d-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0595d-115">Das Cmdlet " **Get-AzureStorageBlobCopyState** " Ruft den Kopierstatus für diesen BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="0595d-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="0595d-116">Beispiel 3: Abrufen des Kopierstatus für ein BLOB in einem Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="0595d-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="0595d-117">Dieser Befehl ruft den mit dem Cmdlet **Get-AzureStorageBlob** benannten Container ab und übergibt dann das Ergebnis an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0595d-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="0595d-118">Das Cmdlet " **Get-AzureStorageContainer** " Ruft den Kopierstatus für das BLOB mit dem Namen ContosoPlanning2015 in diesem Container ab.</span><span class="sxs-lookup"><span data-stu-id="0595d-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="0595d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="0595d-119">PARAMETERS</span></span>

### <span data-ttu-id="0595d-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0595d-120">-Blob</span></span>
<span data-ttu-id="0595d-121">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="0595d-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="0595d-122">Dieses Cmdlet ruft den Zustand des BLOB-Kopiervorgangs für das Azure Storage-BLOB ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0595d-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0595d-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0595d-124">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="0595d-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0595d-125">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="0595d-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0595d-126">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0595d-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0595d-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0595d-127">-CloudBlob</span></span>
<span data-ttu-id="0595d-128">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="0595d-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0595d-129">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0595d-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0595d-130">-CloudBlobContainer</span></span>
<span data-ttu-id="0595d-131">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="0595d-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0595d-132">Dieses Cmdlet ruft den Kopierstatus eines BLOB im Container ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0595d-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="0595d-133">Verwenden Sie das Get-AzureStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0595d-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0595d-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0595d-135">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="0595d-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0595d-136">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="0595d-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0595d-137">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="0595d-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0595d-138">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="0595d-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0595d-139">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="0595d-139">The default value is 10.</span></span>

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

### <span data-ttu-id="0595d-140">-Container</span><span class="sxs-lookup"><span data-stu-id="0595d-140">-Container</span></span>
<span data-ttu-id="0595d-141">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="0595d-141">Specifies the name of a container.</span></span>
<span data-ttu-id="0595d-142">Dieses Cmdlet ruft den Kopierstatus für ein BLOB im Container ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0595d-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-143">-Context</span><span class="sxs-lookup"><span data-stu-id="0595d-143">-Context</span></span>
<span data-ttu-id="0595d-144">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="0595d-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0595d-145">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0595d-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0595d-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0595d-147">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="0595d-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0595d-148">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0595d-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0595d-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0595d-149">-WaitForComplete</span></span>
<span data-ttu-id="0595d-150">Gibt an, dass das Cmdlet auf die Fertigstellung der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="0595d-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="0595d-151">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="0595d-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0595d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0595d-152">CommonParameters</span></span>
<span data-ttu-id="0595d-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0595d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0595d-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0595d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0595d-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0595d-155">INPUTS</span></span>

### <span data-ttu-id="0595d-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0595d-156">IStorageContext</span></span>

<span data-ttu-id="0595d-157">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0595d-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="0595d-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0595d-158">OUTPUTS</span></span>

### <span data-ttu-id="0595d-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="0595d-159">CopyState</span></span>

## <span data-ttu-id="0595d-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="0595d-160">NOTES</span></span>

## <span data-ttu-id="0595d-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0595d-161">RELATED LINKS</span></span>

[<span data-ttu-id="0595d-162">Anfang-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0595d-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="0595d-163">Stopp-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0595d-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


