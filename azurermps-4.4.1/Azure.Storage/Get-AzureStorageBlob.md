---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
gitcommit: https://github.com/Azure/azure-powershell/blob/f8503a90f782f51c8baa0360f98adb33f2a6f26f
ms.openlocfilehash: e05dc3ed962e7d1d4610663dd129c0977b784280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498122"
---
# <span data-ttu-id="2b593-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2b593-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="2b593-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b593-102">SYNOPSIS</span></span>
<span data-ttu-id="2b593-103">Listet BLOBs in einem Container auf.</span><span class="sxs-lookup"><span data-stu-id="2b593-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b593-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b593-104">SYNTAX</span></span>

### <span data-ttu-id="2b593-105">Blobname (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b593-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2b593-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="2b593-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2b593-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b593-107">DESCRIPTION</span></span>
<span data-ttu-id="2b593-108">Das Cmdlet " **Get-AzureStorageBlob** " listet BLOBs im angegebenen Container in einem Azure Storage-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="2b593-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="2b593-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b593-109">EXAMPLES</span></span>

### <span data-ttu-id="2b593-110">Beispiel 1: Abrufen eines BLOB nach BLOB-Namen</span><span class="sxs-lookup"><span data-stu-id="2b593-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="2b593-111">Dieser Befehl verwendet einen BLOB-Namen und Platzhalter, um einen BLOB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b593-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="2b593-112">Beispiel 2: Abrufen eines BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2b593-112">Example 2: Get a blob by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob
```

<span data-ttu-id="2b593-113">Dieser Befehl verwendet die Pipeline, um einen BLOB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b593-113">This command uses the pipeline to get a blob.</span></span>

### <span data-ttu-id="2b593-114">Beispiel 3: Abrufen eines BLOB Nachnamens Präfix</span><span class="sxs-lookup"><span data-stu-id="2b593-114">Example 3: Get a blob by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="2b593-115">Dieser Befehl verwendet ein Namenspräfix, um einen BLOB abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b593-115">This command uses a name prefix to get a blob.</span></span>

### <span data-ttu-id="2b593-116">Beispiel 4: Auflisten von BLOBs in mehreren Batches</span><span class="sxs-lookup"><span data-stu-id="2b593-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="2b593-117">In diesem Beispiel werden die *MaxCount* -und *ContinuationToken* -Parameter verwendet, um Azure-Speicher-BLOBs in mehreren Batches aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="2b593-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="2b593-118">Die ersten vier Befehle weisen Variablenwerte zu, die im Beispiel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2b593-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="2b593-119">Der fünfte Befehl gibt eine **do-while-** Anweisung an, die das Cmdlet **Get-AzureStorageBlob** zum Abrufen von BLOBs verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b593-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="2b593-120">Die Anweisung enthält das Fortsetzungstoken, das in der $Token Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2b593-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="2b593-121">$Token ändert den Wert während der Ausführung der Schleife.</span><span class="sxs-lookup"><span data-stu-id="2b593-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="2b593-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help About_Do` .</span><span class="sxs-lookup"><span data-stu-id="2b593-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="2b593-123">Der endgültige Befehl verwendet den Befehl **Echo** , um die Summe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2b593-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="2b593-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b593-124">PARAMETERS</span></span>

### <span data-ttu-id="2b593-125">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2b593-125">-Blob</span></span>
<span data-ttu-id="2b593-126">Gibt ein Name-oder Name-Muster an, das für eine Platzhaltersuche verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b593-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="2b593-127">Wenn kein BLOB-Name angegeben wird, listet das Cmdlet alle Blobs im angegebenen Container auf.</span><span class="sxs-lookup"><span data-stu-id="2b593-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="2b593-128">Wenn für diesen Parameter ein Wert angegeben wird, listet das Cmdlet alle Blobs mit Namen auf, die diesem Parameter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2b593-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="2b593-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2b593-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2b593-130">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2b593-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2b593-131">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="2b593-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2b593-132">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2b593-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2b593-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2b593-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2b593-134">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="2b593-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2b593-135">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="2b593-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2b593-136">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2b593-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2b593-137">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="2b593-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2b593-138">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2b593-138">The default value is 10.</span></span>

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

### <span data-ttu-id="2b593-139">-Container</span><span class="sxs-lookup"><span data-stu-id="2b593-139">-Container</span></span>
<span data-ttu-id="2b593-140">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="2b593-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b593-141">-Context</span><span class="sxs-lookup"><span data-stu-id="2b593-141">-Context</span></span>
<span data-ttu-id="2b593-142">Gibt das Azure-Speicherkonto an, aus dem Sie eine Liste von BLOBs abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b593-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="2b593-143">Sie können das New-AzureStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b593-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="2b593-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2b593-144">-ContinuationToken</span></span>
<span data-ttu-id="2b593-145">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="2b593-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="2b593-146">Verwenden Sie diesen Parameter und den *MaxCount* -Parameter, um BLOBs in mehreren Batches aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="2b593-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b593-147">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2b593-147">-MaxCount</span></span>
<span data-ttu-id="2b593-148">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b593-148">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="2b593-149">-Prefix</span><span class="sxs-lookup"><span data-stu-id="2b593-149">-Prefix</span></span>
<span data-ttu-id="2b593-150">Gibt ein Präfix für die BLOB-Namen an, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="2b593-150">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="2b593-151">Dieser Parameter unterstützt nicht die Verwendung regulärer Ausdrücke oder Platzhalterzeichen für die Suche.</span><span class="sxs-lookup"><span data-stu-id="2b593-151">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="2b593-152">Wenn der Container nur BLOBs mit dem Namen "My", "MyBlob1" und "MyBlob2" enthält und Sie "-prefix My \*" angeben, gibt das Cmdlet keine BLOBs zurück.</span><span class="sxs-lookup"><span data-stu-id="2b593-152">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="2b593-153">Wenn Sie jedoch "-prefix My" angeben, gibt das Cmdlet "My", "MyBlob1" und "MyBlob2" zurück.</span><span class="sxs-lookup"><span data-stu-id="2b593-153">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b593-154">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2b593-154">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2b593-155">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2b593-155">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2b593-156">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2b593-156">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2b593-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b593-157">CommonParameters</span></span>
<span data-ttu-id="2b593-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b593-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b593-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b593-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b593-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b593-160">INPUTS</span></span>

### <span data-ttu-id="2b593-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b593-161">IStorageContext</span></span>

<span data-ttu-id="2b593-162">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2b593-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2b593-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b593-163">OUTPUTS</span></span>

### <span data-ttu-id="2b593-164">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2b593-164">AzureStorageBlob</span></span>

## <span data-ttu-id="2b593-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b593-165">NOTES</span></span>


## <span data-ttu-id="2b593-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b593-166">RELATED LINKS</span></span>

[<span data-ttu-id="2b593-167">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2b593-167">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="2b593-168">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2b593-168">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="2b593-169">Satz-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2b593-169">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)


