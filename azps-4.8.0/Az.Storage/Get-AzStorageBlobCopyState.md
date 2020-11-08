---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007739"
---
# <span data-ttu-id="1a84d-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="1a84d-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="1a84d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a84d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a84d-103">Ruft den Kopierstatus eines Azure Storage-BLOBs ab.</span><span class="sxs-lookup"><span data-stu-id="1a84d-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="1a84d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a84d-104">SYNTAX</span></span>

### <span data-ttu-id="1a84d-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a84d-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1a84d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="1a84d-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="1a84d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="1a84d-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1a84d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a84d-108">DESCRIPTION</span></span>
<span data-ttu-id="1a84d-109">Das Cmdlet " **Get-AzStorageBlobCopyState** " Ruft den Kopierstatus eines Azure Storage-BLOBs ab.</span><span class="sxs-lookup"><span data-stu-id="1a84d-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="1a84d-110">Sie sollte auf dem BLOB für das Kopieren des Ziels ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1a84d-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="1a84d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a84d-111">EXAMPLES</span></span>

### <span data-ttu-id="1a84d-112">Beispiel 1: Abrufen des Kopierstatus eines BLOB</span><span class="sxs-lookup"><span data-stu-id="1a84d-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="1a84d-113">Dieser Befehl ruft den Kopierstatus des BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads ab.</span><span class="sxs-lookup"><span data-stu-id="1a84d-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="1a84d-114">Beispiel 2: Abrufen des Kopierstatus für ein BLOB mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="1a84d-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="1a84d-115">Dieser Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads mit dem Cmdlet **Get-AzStorageBlob** ab und übergibt dann das Ergebnis mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a84d-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1a84d-116">Das Cmdlet " **Get-AzStorageBlobCopyState** " Ruft den Kopierstatus für diesen BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="1a84d-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="1a84d-117">Beispiel 3: Abrufen des Kopierstatus für ein BLOB in einem Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="1a84d-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="1a84d-118">Dieser Befehl ruft den mit dem Cmdlet **Get-AzStorageBlob** benannten Container ab und übergibt dann das Ergebnis an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a84d-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="1a84d-119">Das Cmdlet " **Get-AzStorageContainer** " Ruft den Kopierstatus für das BLOB mit dem Namen ContosoPlanning2015 in diesem Container ab.</span><span class="sxs-lookup"><span data-stu-id="1a84d-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="1a84d-120">Beispiel 4: Kopieren und Pipeline starten, um den Kopierstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="1a84d-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="1a84d-121">Mit dem ersten Befehl wird BLOB "ContosoPlanning2015" in "ContosoPlanning2015_copy" kopiert, und das destiantion-BLOB-Objekt wird ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="1a84d-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="1a84d-122">Der zweite Befehl Pipeline das destiantion-BLOB-Objekt zu Get-AzStorageBlobCopyState, um den BLOB-Kopier Zustand abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1a84d-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="1a84d-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a84d-123">PARAMETERS</span></span>

### <span data-ttu-id="1a84d-124">-BLOB</span><span class="sxs-lookup"><span data-stu-id="1a84d-124">-Blob</span></span>
<span data-ttu-id="1a84d-125">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="1a84d-126">Dieses Cmdlet ruft den Zustand des BLOB-Kopiervorgangs für das Azure Storage-BLOB ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1a84d-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a84d-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a84d-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a84d-128">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a84d-129">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="1a84d-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a84d-130">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1a84d-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a84d-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1a84d-131">-CloudBlob</span></span>
<span data-ttu-id="1a84d-132">Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="1a84d-133">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a84d-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84d-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1a84d-134">-CloudBlobContainer</span></span>
<span data-ttu-id="1a84d-135">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="1a84d-136">Dieses Cmdlet ruft den Kopierstatus eines BLOB im Container ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1a84d-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="1a84d-137">Verwenden Sie das Get-AzStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a84d-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84d-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a84d-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a84d-139">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a84d-140">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="1a84d-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a84d-141">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="1a84d-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a84d-142">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="1a84d-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a84d-143">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1a84d-143">The default value is 10.</span></span>

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

### <span data-ttu-id="1a84d-144">-Container</span><span class="sxs-lookup"><span data-stu-id="1a84d-144">-Container</span></span>
<span data-ttu-id="1a84d-145">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-145">Specifies the name of a container.</span></span>
<span data-ttu-id="1a84d-146">Dieses Cmdlet ruft den Kopierstatus für ein BLOB im Container ab, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1a84d-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a84d-147">-Context</span><span class="sxs-lookup"><span data-stu-id="1a84d-147">-Context</span></span>
<span data-ttu-id="1a84d-148">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1a84d-149">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a84d-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a84d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a84d-150">-DefaultProfile</span></span>
<span data-ttu-id="1a84d-151">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a84d-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a84d-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a84d-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a84d-153">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1a84d-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1a84d-154">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1a84d-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1a84d-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="1a84d-155">-WaitForComplete</span></span>
<span data-ttu-id="1a84d-156">Gibt an, dass das Cmdlet auf die Fertigstellung der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="1a84d-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="1a84d-157">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="1a84d-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="1a84d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a84d-158">CommonParameters</span></span>
<span data-ttu-id="1a84d-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a84d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a84d-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a84d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a84d-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a84d-161">INPUTS</span></span>

### <span data-ttu-id="1a84d-162">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="1a84d-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="1a84d-163">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="1a84d-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="1a84d-164">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a84d-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a84d-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a84d-165">OUTPUTS</span></span>

### <span data-ttu-id="1a84d-166">Microsoft. Azure. Storage. BLOB. CopyState</span><span class="sxs-lookup"><span data-stu-id="1a84d-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="1a84d-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a84d-167">NOTES</span></span>

## <span data-ttu-id="1a84d-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a84d-168">RELATED LINKS</span></span>

[<span data-ttu-id="1a84d-169">Anfang-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1a84d-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="1a84d-170">Stopp-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="1a84d-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


