---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290603"
---
# <span data-ttu-id="83ae2-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="83ae2-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="83ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="83ae2-103">Ruft den Kopierstatus eines Azure Storage-BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="83ae2-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="83ae2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83ae2-104">SYNTAX</span></span>

### <span data-ttu-id="83ae2-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="83ae2-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="83ae2-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="83ae2-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="83ae2-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="83ae2-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="83ae2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83ae2-108">DESCRIPTION</span></span>
<span data-ttu-id="83ae2-109">Das **Cmdlet "Get-AzStorageBlobCopyState"** ruft den Kopierstatus eines Azure Storage-BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="83ae2-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="83ae2-110">Sie sollte für den Kopierziel-BLOB ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="83ae2-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="83ae2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83ae2-111">EXAMPLES</span></span>

### <span data-ttu-id="83ae2-112">Beispiel 1: Anzeigen des Kopierstatus eines BLOB</span><span class="sxs-lookup"><span data-stu-id="83ae2-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="83ae2-113">Dieser Befehl ruft den Kopierstatus des BLOB namens "ContosoPlanning2015" im Container "ContosoUploads" ab.</span><span class="sxs-lookup"><span data-stu-id="83ae2-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="83ae2-114">Beispiel 2: Erhalten des Kopierstatus für ein BLOB mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="83ae2-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="83ae2-115">Dieser Befehl ruft das BLOB namens "ContosoPlanning2015" im Container "ContosoUploads" mithilfe des **Cmdlets "Get-AzStorageBlob"** ab und übergibt dann das Ergebnis mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83ae2-116">Das **Cmdlet "Get-AzStorageBlobCopyState"** ruft den Kopierstatus für dieses BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="83ae2-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="83ae2-117">Beispiel 3: Anzeigen des Kopierstatus für ein BLOB in einem Container mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="83ae2-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="83ae2-118">Dieser Befehl ruft den Container mit dem **Cmdlet "Get-AzStorageBlob"** benannt und übergibt das Ergebnis dann an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="83ae2-119">Das **Cmdlet "Get-AzStorageContainer"** ruft den Kopierstatus für das BLOB namens "ContosoPlanning2015" in diesem Container ab.</span><span class="sxs-lookup"><span data-stu-id="83ae2-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="83ae2-120">Beispiel 4: Starten von "Kopieren und Pipeline", um den Kopierstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="83ae2-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="83ae2-121">Der erste Befehl startet das Kopieren des BLOB "ContosoPlanning2015" in "ContosoPlanning2015_copy" und gibt das Desdelikations-BLOB-Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="83ae2-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="83ae2-122">Die zweite Befehlspipeline des Deslikations-BLOB-Objekts zu "Get-AzStorageBlobCopyState", um den Blob Copy-Zustand zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="83ae2-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="83ae2-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83ae2-123">PARAMETERS</span></span>

### <span data-ttu-id="83ae2-124">-BLOB</span><span class="sxs-lookup"><span data-stu-id="83ae2-124">-Blob</span></span>
<span data-ttu-id="83ae2-125">Gibt den Namen eines BLOB an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="83ae2-126">Dieses Cmdlet ruft den Zustand des BLOB-Kopiervorgangs für den Azure Storage-BLOB ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="83ae2-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="83ae2-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83ae2-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="83ae2-128">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="83ae2-129">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83ae2-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="83ae2-130">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="83ae2-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="83ae2-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="83ae2-131">-CloudBlob</span></span>
<span data-ttu-id="83ae2-132">Gibt ein **CloudBlob-Objekt** aus der Azure Storage -Clientbibliothek an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="83ae2-133">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="83ae2-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="83ae2-134">-CloudBlobContainer</span></span>
<span data-ttu-id="83ae2-135">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="83ae2-136">Dieses Cmdlet ruft den Kopierstatus eines BLOB im Container ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="83ae2-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="83ae2-137">Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="83ae2-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="83ae2-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="83ae2-139">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="83ae2-140">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="83ae2-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="83ae2-141">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="83ae2-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="83ae2-142">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="83ae2-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="83ae2-143">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="83ae2-143">The default value is 10.</span></span>

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

### <span data-ttu-id="83ae2-144">-Container</span><span class="sxs-lookup"><span data-stu-id="83ae2-144">-Container</span></span>
<span data-ttu-id="83ae2-145">Gibt den Namen eines Containers an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-145">Specifies the name of a container.</span></span>
<span data-ttu-id="83ae2-146">Dieses Cmdlet ruft den Kopierstatus für ein BLOB im Container ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="83ae2-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="83ae2-147">-Context</span><span class="sxs-lookup"><span data-stu-id="83ae2-147">-Context</span></span>
<span data-ttu-id="83ae2-148">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="83ae2-149">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="83ae2-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ae2-150">-DefaultProfile</span></span>
<span data-ttu-id="83ae2-151">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83ae2-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83ae2-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="83ae2-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="83ae2-153">Gibt das intervallseitige Dienstzeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="83ae2-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="83ae2-154">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="83ae2-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="83ae2-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="83ae2-155">-WaitForComplete</span></span>
<span data-ttu-id="83ae2-156">Zeigt an, dass dieses Cmdlet auf den Abschluss der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="83ae2-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="83ae2-157">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="83ae2-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="83ae2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ae2-158">CommonParameters</span></span>
<span data-ttu-id="83ae2-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ae2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ae2-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ae2-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ae2-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83ae2-161">INPUTS</span></span>

### <span data-ttu-id="83ae2-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="83ae2-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="83ae2-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="83ae2-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="83ae2-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="83ae2-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="83ae2-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83ae2-165">OUTPUTS</span></span>

### <span data-ttu-id="83ae2-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="83ae2-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="83ae2-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83ae2-167">NOTES</span></span>

## <span data-ttu-id="83ae2-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83ae2-168">RELATED LINKS</span></span>

[<span data-ttu-id="83ae2-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="83ae2-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="83ae2-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="83ae2-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


