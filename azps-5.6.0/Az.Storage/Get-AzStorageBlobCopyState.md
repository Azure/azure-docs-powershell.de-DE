---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 4bc06ca07c95986f75062a64a0f86475f7720ff1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944615"
---
# <span data-ttu-id="04add-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="04add-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="04add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04add-102">SYNOPSIS</span></span>
<span data-ttu-id="04add-103">Ruft den Kopierstatus eines Azure Storage-Blobs ab.</span><span class="sxs-lookup"><span data-stu-id="04add-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="04add-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04add-104">SYNTAX</span></span>

### <span data-ttu-id="04add-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="04add-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="04add-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="04add-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="04add-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="04add-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="04add-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04add-108">DESCRIPTION</span></span>
<span data-ttu-id="04add-109">Das **Get-AzStorageBlobCopyState-Cmdlet** ruft den Kopierstatus eines Azure Storage-Blobs ab.</span><span class="sxs-lookup"><span data-stu-id="04add-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="04add-110">Sie sollte auf dem Kopierzielblob ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="04add-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="04add-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04add-111">EXAMPLES</span></span>

### <span data-ttu-id="04add-112">Beispiel 1: Anzeigen des Kopierstatus eines Blobs</span><span class="sxs-lookup"><span data-stu-id="04add-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="04add-113">Dieser Befehl ruft den Kopierstatus des Blobs namens ContosoPlanning2015 im Container ContosoUploads ab.</span><span class="sxs-lookup"><span data-stu-id="04add-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="04add-114">Beispiel 2: Erhalten des Kopierstatus für einen Blob mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="04add-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="04add-115">Dieser Befehl ruft den Blob namens ContosoPlanning2015 im Container namens ContosoUploads mithilfe des **Get-AzStorageBlob-Cmdlets** ab und übergibt das Ergebnis dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04add-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="04add-116">Das **Get-AzStorageBlobCopyState-Cmdlet** ruft den Kopierstatus für dieses Blob ab.</span><span class="sxs-lookup"><span data-stu-id="04add-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="04add-117">Beispiel 3: Anzeigen des Kopierstatus für einen Blob in einem Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="04add-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="04add-118">Dieser Befehl ruft den Container mit dem **Get-AzStorageBlob-Cmdlet** ab und übergibt das Ergebnis dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04add-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="04add-119">Das **Get-AzStorageContainer-Cmdlet** ruft den Kopierstatus für das Blob mit dem Namen ContosoPlanning2015 in diesem Container ab.</span><span class="sxs-lookup"><span data-stu-id="04add-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="04add-120">Beispiel 4: Starten von Kopieren und Pipeline, um den Kopierstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="04add-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="04add-121">Der erste Befehl startet das Kopieren des Blobs "ContosoPlanning2015" in "ContosoPlanning2015_copy", und gibt das Destiantion-Blob-Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="04add-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="04add-122">Der zweite Befehl pipelinet das Destiantion-Blob-Objekt zu Get-AzStorageBlobCopyState, um den Blobkopiezustand zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="04add-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="04add-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="04add-123">PARAMETERS</span></span>

### <span data-ttu-id="04add-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="04add-124">-Blob</span></span>
<span data-ttu-id="04add-125">Gibt den Namen eines Blobs an.</span><span class="sxs-lookup"><span data-stu-id="04add-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="04add-126">Dieses Cmdlet ruft den Zustand des Blobkopievorgangs für den Azure Storage-Blob ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="04add-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="04add-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04add-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="04add-128">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="04add-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="04add-129">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04add-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="04add-130">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="04add-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="04add-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04add-131">-CloudBlob</span></span>
<span data-ttu-id="04add-132">Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="04add-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="04add-133">Um ein **CloudBlob-Objekt zu** erhalten, verwenden Sie das Get-AzStorageBlob Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04add-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="04add-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04add-134">-CloudBlobContainer</span></span>
<span data-ttu-id="04add-135">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client-Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="04add-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="04add-136">Dieses Cmdlet ruft den Kopierstatus eines Blobs im Container ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="04add-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="04add-137">Zum Abrufen eines **CloudBlobContainer-Objekts** verwenden Sie das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04add-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="04add-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="04add-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="04add-139">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="04add-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="04add-140">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="04add-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="04add-141">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="04add-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="04add-142">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="04add-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="04add-143">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="04add-143">The default value is 10.</span></span>

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

### <span data-ttu-id="04add-144">-Container</span><span class="sxs-lookup"><span data-stu-id="04add-144">-Container</span></span>
<span data-ttu-id="04add-145">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="04add-145">Specifies the name of a container.</span></span>
<span data-ttu-id="04add-146">Dieses Cmdlet ruft den Kopierstatus für einen Blob im Container ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="04add-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="04add-147">-Context</span><span class="sxs-lookup"><span data-stu-id="04add-147">-Context</span></span>
<span data-ttu-id="04add-148">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="04add-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="04add-149">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04add-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04add-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04add-150">-DefaultProfile</span></span>
<span data-ttu-id="04add-151">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04add-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04add-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04add-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="04add-153">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="04add-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="04add-154">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="04add-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="04add-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="04add-155">-WaitForComplete</span></span>
<span data-ttu-id="04add-156">Gibt an, dass dieses Cmdlet wartet, bis die Kopie fertig ist.</span><span class="sxs-lookup"><span data-stu-id="04add-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="04add-157">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="04add-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="04add-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04add-158">CommonParameters</span></span>
<span data-ttu-id="04add-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04add-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04add-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04add-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04add-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04add-161">INPUTS</span></span>

### <span data-ttu-id="04add-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04add-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="04add-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04add-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="04add-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04add-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04add-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04add-165">OUTPUTS</span></span>

### <span data-ttu-id="04add-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="04add-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="04add-167">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="04add-167">NOTES</span></span>

## <span data-ttu-id="04add-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="04add-168">RELATED LINKS</span></span>

[<span data-ttu-id="04add-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04add-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="04add-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="04add-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


