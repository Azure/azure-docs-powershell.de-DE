---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd885e79fb4daf1eec9dd8958283be28e52f920f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474801"
---
# <span data-ttu-id="362c3-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="362c3-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="362c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="362c3-102">SYNOPSIS</span></span>
<span data-ttu-id="362c3-103">Löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="362c3-103">Deletes a directory.</span></span>

## <span data-ttu-id="362c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="362c3-104">SYNTAX</span></span>

### <span data-ttu-id="362c3-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="362c3-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="362c3-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="362c3-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="362c3-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="362c3-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="362c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="362c3-108">DESCRIPTION</span></span>
<span data-ttu-id="362c3-109">Das Cmdlet **Remove-AzureStorageDirectory** löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="362c3-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="362c3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="362c3-110">EXAMPLES</span></span>

### <span data-ttu-id="362c3-111">Beispiel 1: Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="362c3-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="362c3-112">Dieser Befehl löscht den Ordner "ContosoWorkingFolder" aus der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="362c3-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="362c3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="362c3-113">PARAMETERS</span></span>

### <span data-ttu-id="362c3-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="362c3-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="362c3-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="362c3-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="362c3-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="362c3-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="362c3-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="362c3-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="362c3-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="362c3-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="362c3-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="362c3-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="362c3-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="362c3-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="362c3-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="362c3-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="362c3-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="362c3-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="362c3-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="362c3-123">The default value is 10.</span></span>

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

### <span data-ttu-id="362c3-124">-Context</span><span class="sxs-lookup"><span data-stu-id="362c3-124">-Context</span></span>
<span data-ttu-id="362c3-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="362c3-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="362c3-126">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="362c3-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="362c3-127">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="362c3-127">-Directory</span></span>
<span data-ttu-id="362c3-128">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="362c3-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="362c3-129">Mit diesem Cmdlet wird der Ordner entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="362c3-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="362c3-130">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="362c3-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="362c3-131">Sie können auch das Cmdlet **Get-AzureStorageFile** verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="362c3-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="362c3-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="362c3-132">-PassThru</span></span>
<span data-ttu-id="362c3-133">Gibt an, dass, wenn dieses Cmdlet erfolgreich ist, der Wert $true zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="362c3-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="362c3-134">Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines unangemessenen Werts für den _path_ -Parameter nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="362c3-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="362c3-135">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="362c3-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="362c3-136">-Path</span><span class="sxs-lookup"><span data-stu-id="362c3-136">-Path</span></span>
<span data-ttu-id="362c3-137">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="362c3-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="362c3-138">Wenn der Ordner, den dieser Parameter angibt, leer ist, löscht dieses Cmdlet diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="362c3-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="362c3-139">Wenn der Ordner nicht leer ist, nimmt das Cmdlet keine Änderungen vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="362c3-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362c3-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="362c3-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="362c3-141">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="362c3-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="362c3-142">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="362c3-142">-Share</span></span>
<span data-ttu-id="362c3-143">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="362c3-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="362c3-144">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="362c3-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="362c3-145">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="362c3-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="362c3-146">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="362c3-146">This object contains the storage context.</span></span>
<span data-ttu-id="362c3-147">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="362c3-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="362c3-148">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="362c3-148">-ShareName</span></span>
<span data-ttu-id="362c3-149">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="362c3-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="362c3-150">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="362c3-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="362c3-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="362c3-151">-Confirm</span></span>
<span data-ttu-id="362c3-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="362c3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="362c3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="362c3-153">-WhatIf</span></span>
<span data-ttu-id="362c3-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="362c3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="362c3-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="362c3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="362c3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362c3-156">CommonParameters</span></span>
<span data-ttu-id="362c3-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="362c3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362c3-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="362c3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362c3-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="362c3-159">INPUTS</span></span>

## <span data-ttu-id="362c3-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="362c3-160">OUTPUTS</span></span>

## <span data-ttu-id="362c3-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="362c3-161">NOTES</span></span>

## <span data-ttu-id="362c3-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="362c3-162">RELATED LINKS</span></span>

[<span data-ttu-id="362c3-163">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="362c3-163">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="362c3-164">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="362c3-164">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="362c3-165">Neu – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="362c3-165">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
