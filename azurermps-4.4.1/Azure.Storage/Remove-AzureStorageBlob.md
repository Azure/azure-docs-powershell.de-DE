---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageBlob.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d81f4d90a738aef54e33f886320b4cf99d45296b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662988"
---
# <span data-ttu-id="78918-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="78918-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="78918-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78918-102">SYNOPSIS</span></span>
<span data-ttu-id="78918-103">Entfernt das angegebene Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="78918-103">Removes the specified storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78918-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78918-104">SYNTAX</span></span>

### <span data-ttu-id="78918-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="78918-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78918-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="78918-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78918-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="78918-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78918-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78918-108">DESCRIPTION</span></span>
<span data-ttu-id="78918-109">Das Cmdlet **Remove-AzureStorageBlob** entfernt das angegebene BLOB aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="78918-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="78918-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78918-110">EXAMPLES</span></span>

### <span data-ttu-id="78918-111">Beispiel 1: Entfernen eines Speicher-BLOBs nach Name</span><span class="sxs-lookup"><span data-stu-id="78918-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="78918-112">Mit diesem Befehl wird ein BLOB entfernt, das mit dem Namen identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="78918-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="78918-113">Beispiel 2: Entfernen eines Speicher-BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="78918-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="78918-114">Dieser Befehl verwendet die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="78918-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="78918-115">Beispiel 3: Entfernen von Speicher-BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="78918-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="78918-116">Dieser Befehl verwendet das Sternchen (\*)-Platzhalterzeichen und die Pipeline, um das BLOB oder die BLOBs abzurufen und dann zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="78918-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="78918-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="78918-117">PARAMETERS</span></span>

### <span data-ttu-id="78918-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="78918-118">-Blob</span></span>
<span data-ttu-id="78918-119">Gibt den Namen des zu entfernenden BLOB an.</span><span class="sxs-lookup"><span data-stu-id="78918-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="78918-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78918-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="78918-121">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="78918-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="78918-122">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="78918-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="78918-123">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="78918-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="78918-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="78918-124">-CloudBlob</span></span>
<span data-ttu-id="78918-125">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="78918-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="78918-126">Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="78918-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="78918-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="78918-127">-CloudBlobContainer</span></span>
<span data-ttu-id="78918-128">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="78918-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="78918-129">Sie können das Get-AzureStorageContainer-Cmdlet verwenden, um es abzurufen.</span><span class="sxs-lookup"><span data-stu-id="78918-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="78918-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="78918-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="78918-131">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="78918-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="78918-132">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="78918-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="78918-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="78918-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="78918-134">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="78918-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="78918-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="78918-135">The default value is 10.</span></span>

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

### <span data-ttu-id="78918-136">-Container</span><span class="sxs-lookup"><span data-stu-id="78918-136">-Container</span></span>
<span data-ttu-id="78918-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="78918-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="78918-138">-Context</span><span class="sxs-lookup"><span data-stu-id="78918-138">-Context</span></span>
<span data-ttu-id="78918-139">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="78918-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="78918-140">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78918-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="78918-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="78918-141">-DeleteSnapshot</span></span>
<span data-ttu-id="78918-142">Gibt an, dass alle Snapshots gelöscht werden, aber nicht das Basis-BLOB.</span><span class="sxs-lookup"><span data-stu-id="78918-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="78918-143">Wenn dieser Parameter nicht angegeben wird, werden das Basis-BLOB und dessen Snapshots zusammen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="78918-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="78918-144">Der Benutzer wird aufgefordert, den Löschvorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="78918-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="78918-145">-Force</span><span class="sxs-lookup"><span data-stu-id="78918-145">-Force</span></span>
<span data-ttu-id="78918-146">Gibt an, dass dieses Cmdlet das BLOB und seinen Snapshot ohne Bestätigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="78918-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="78918-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78918-147">-PassThru</span></span>
<span data-ttu-id="78918-148">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="78918-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="78918-149">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78918-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="78918-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78918-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="78918-151">Gibt das Azure-Profil für das zu lesende Cmdlet an.</span><span class="sxs-lookup"><span data-stu-id="78918-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="78918-152">Wenn keine Angabe erfolgt, liest das Cmdlet aus dem Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="78918-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="78918-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78918-153">-Confirm</span></span>
<span data-ttu-id="78918-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78918-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78918-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78918-155">-WhatIf</span></span>
<span data-ttu-id="78918-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78918-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78918-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78918-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78918-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78918-158">CommonParameters</span></span>
<span data-ttu-id="78918-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78918-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78918-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78918-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78918-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78918-161">INPUTS</span></span>

### <span data-ttu-id="78918-162">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="78918-162">IStorageContext</span></span>

<span data-ttu-id="78918-163">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="78918-163">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="78918-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78918-164">OUTPUTS</span></span>

### <span data-ttu-id="78918-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78918-165">System.Boolean</span></span>

## <span data-ttu-id="78918-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="78918-166">NOTES</span></span>

## <span data-ttu-id="78918-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78918-167">RELATED LINKS</span></span>

[<span data-ttu-id="78918-168">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="78918-168">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="78918-169">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="78918-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="78918-170">Satz-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="78918-170">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)
