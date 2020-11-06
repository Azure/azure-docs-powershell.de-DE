---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageFile.md
ms.openlocfilehash: 9055f447093a0e10242824e1e2381523e0b0e81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500661"
---
# <span data-ttu-id="8625b-101">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8625b-101">Remove-AzureStorageFile</span></span>

## <span data-ttu-id="8625b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8625b-102">SYNOPSIS</span></span>
<span data-ttu-id="8625b-103">Löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8625b-103">Deletes a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8625b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8625b-104">SYNTAX</span></span>

### <span data-ttu-id="8625b-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="8625b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8625b-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="8625b-106">Share</span></span>
```
Remove-AzureStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8625b-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8625b-107">Directory</span></span>
```
Remove-AzureStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8625b-108">Datei</span><span class="sxs-lookup"><span data-stu-id="8625b-108">File</span></span>
```
Remove-AzureStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8625b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8625b-109">DESCRIPTION</span></span>
<span data-ttu-id="8625b-110">Das Cmdlet **Remove-AzureStorageFile** löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8625b-110">The **Remove-AzureStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="8625b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8625b-111">EXAMPLES</span></span>

### <span data-ttu-id="8625b-112">Beispiel 1: Löschen einer Datei aus einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="8625b-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="8625b-113">Dieser Befehl löscht die Datei mit dem Namen ContosoFile22 aus der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8625b-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="8625b-114">Beispiel 2: Abrufen einer Datei aus einer Dateifreigabe mithilfe eines Dateifreigabe Objekts</span><span class="sxs-lookup"><span data-stu-id="8625b-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | Remove-AzureStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="8625b-115">Dieser Befehl verwendet das Cmdlet " **Get-AzureStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8625b-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8625b-116">Der aktuelle Befehl löscht die Datei mit dem Namen ContosoFile22 aus ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="8625b-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="8625b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8625b-117">PARAMETERS</span></span>

### <span data-ttu-id="8625b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8625b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8625b-119">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="8625b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8625b-120">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="8625b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8625b-121">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8625b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8625b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8625b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8625b-123">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="8625b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8625b-124">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="8625b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8625b-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8625b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8625b-126">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8625b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8625b-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8625b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="8625b-128">-Context</span><span class="sxs-lookup"><span data-stu-id="8625b-128">-Context</span></span>
<span data-ttu-id="8625b-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8625b-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8625b-130">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="8625b-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8625b-131">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8625b-131">-Directory</span></span>
<span data-ttu-id="8625b-132">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8625b-132">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8625b-133">Dieses Cmdlet entfernt eine Datei aus dem Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8625b-133">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="8625b-134">-Datei</span><span class="sxs-lookup"><span data-stu-id="8625b-134">-File</span></span>
<span data-ttu-id="8625b-135">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8625b-135">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="8625b-136">Dieses Cmdlet entfernt die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8625b-136">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="8625b-137">Verwenden Sie das Get-AzureStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8625b-137">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8625b-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8625b-138">-PassThru</span></span>
<span data-ttu-id="8625b-139">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="8625b-139">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8625b-140">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8625b-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8625b-141">-Path</span><span class="sxs-lookup"><span data-stu-id="8625b-141">-Path</span></span>
<span data-ttu-id="8625b-142">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="8625b-142">Specifies the path of a file.</span></span>
<span data-ttu-id="8625b-143">Dieses Cmdlet löscht die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8625b-143">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8625b-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8625b-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8625b-145">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8625b-145">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8625b-146">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="8625b-146">-Share</span></span>
<span data-ttu-id="8625b-147">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8625b-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8625b-148">Mit diesem Cmdlet wird die Datei in der Freigabe, die dieser Parameter angibt, entfernt.</span><span class="sxs-lookup"><span data-stu-id="8625b-148">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="8625b-149">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8625b-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="8625b-150">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="8625b-150">This object contains the storage context.</span></span>
<span data-ttu-id="8625b-151">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="8625b-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="8625b-152">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="8625b-152">-ShareName</span></span>
<span data-ttu-id="8625b-153">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8625b-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="8625b-154">Mit diesem Cmdlet wird die Datei in der Freigabe, die dieser Parameter angibt, entfernt.</span><span class="sxs-lookup"><span data-stu-id="8625b-154">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="8625b-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8625b-155">-Confirm</span></span>
<span data-ttu-id="8625b-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8625b-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8625b-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8625b-157">-WhatIf</span></span>
<span data-ttu-id="8625b-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8625b-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8625b-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8625b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8625b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8625b-160">CommonParameters</span></span>
<span data-ttu-id="8625b-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8625b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8625b-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8625b-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8625b-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8625b-163">INPUTS</span></span>

### <span data-ttu-id="8625b-164">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8625b-164">IStorageContext</span></span>

<span data-ttu-id="8625b-165">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8625b-165">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8625b-166">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8625b-166">CloudFileDirectory</span></span>

<span data-ttu-id="8625b-167">Der Parameter "Verzeichnis" akzeptiert den Wert vom Typ "CloudFileDirectory" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8625b-167">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="8625b-168">Clouddatei</span><span class="sxs-lookup"><span data-stu-id="8625b-168">CloudFile</span></span>

<span data-ttu-id="8625b-169">Der Parameter "Datei" akzeptiert den Wert vom Typ "clouddatei" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8625b-169">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="8625b-170">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8625b-170">CloudFileShare</span></span>

<span data-ttu-id="8625b-171">Der Parameter "Share" akzeptiert den Wert vom Typ "CloudFileShare" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8625b-171">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="8625b-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8625b-172">OUTPUTS</span></span>

## <span data-ttu-id="8625b-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="8625b-173">NOTES</span></span>

## <span data-ttu-id="8625b-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8625b-174">RELATED LINKS</span></span>

[<span data-ttu-id="8625b-175">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8625b-175">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="8625b-176">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="8625b-176">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="8625b-177">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8625b-177">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
