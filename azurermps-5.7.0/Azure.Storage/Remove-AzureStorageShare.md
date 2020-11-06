---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
ms.openlocfilehash: c929a7e3e685fd870c57ff942262a0c5ac4a9966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478813"
---
# <span data-ttu-id="fe1ad-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe1ad-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="fe1ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fe1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1ad-103">Löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe1ad-104">SYNTAX</span></span>

### <span data-ttu-id="fe1ad-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe1ad-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe1ad-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="fe1ad-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe1ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="fe1ad-108">Das Cmdlet **Remove-AzureStorageShare** löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="fe1ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="fe1ad-110">Beispiel 1: Entfernen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="fe1ad-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="fe1ad-111">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="fe1ad-112">Beispiel 2: Entfernen einer Dateifreigabe und aller zugehörigen Snapshots</span><span class="sxs-lookup"><span data-stu-id="fe1ad-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="fe1ad-113">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06 und alle zugehörigen Snapshots.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="fe1ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe1ad-114">PARAMETERS</span></span>

### <span data-ttu-id="fe1ad-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe1ad-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fe1ad-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fe1ad-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fe1ad-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fe1ad-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fe1ad-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fe1ad-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fe1ad-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fe1ad-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fe1ad-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fe1ad-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-124">The default value is 10.</span></span>

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

### <span data-ttu-id="fe1ad-125">-Context</span><span class="sxs-lookup"><span data-stu-id="fe1ad-125">-Context</span></span>
<span data-ttu-id="fe1ad-126">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fe1ad-127">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="fe1ad-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="fe1ad-128">-Force</span><span class="sxs-lookup"><span data-stu-id="fe1ad-128">-Force</span></span>
<span data-ttu-id="fe1ad-129">Erzwingen Sie die Freigabe für alle Snapshots und alle Inhalte.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-129">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="fe1ad-130">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="fe1ad-130">-IncludeAllSnapshot</span></span>
<span data-ttu-id="fe1ad-131">Entfernen der Dateifreigabe für alle Snapshots</span><span class="sxs-lookup"><span data-stu-id="fe1ad-131">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="fe1ad-132">-Name</span><span class="sxs-lookup"><span data-stu-id="fe1ad-132">-Name</span></span>
<span data-ttu-id="fe1ad-133">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-133">Specifies the name of the file share.</span></span>
<span data-ttu-id="fe1ad-134">Dieses Cmdlet löscht die Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-134">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1ad-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe1ad-135">-PassThru</span></span>
<span data-ttu-id="fe1ad-136">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-136">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fe1ad-137">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-137">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fe1ad-138">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fe1ad-138">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fe1ad-139">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-139">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fe1ad-140">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="fe1ad-140">-Share</span></span>
<span data-ttu-id="fe1ad-141">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-141">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fe1ad-142">Dieses Cmdlet entfernt das Objekt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-142">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="fe1ad-143">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-143">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="fe1ad-144">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-144">This object contains the storage context.</span></span>
<span data-ttu-id="fe1ad-145">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-145">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fe1ad-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fe1ad-146">-Confirm</span></span>
<span data-ttu-id="fe1ad-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe1ad-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1ad-148">-WhatIf</span></span>
<span data-ttu-id="fe1ad-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1ad-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe1ad-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1ad-151">CommonParameters</span></span>
<span data-ttu-id="fe1ad-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1ad-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1ad-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1ad-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fe1ad-154">INPUTS</span></span>

### <span data-ttu-id="fe1ad-155">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe1ad-155">IStorageContext</span></span>

<span data-ttu-id="fe1ad-156">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-156">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fe1ad-157">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="fe1ad-157">String</span></span>

<span data-ttu-id="fe1ad-158">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-158">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="fe1ad-159">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fe1ad-159">CloudFileShare</span></span>

<span data-ttu-id="fe1ad-160">Der Parameter "Share" akzeptiert den Wert vom Typ "CloudFileShare" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fe1ad-160">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="fe1ad-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fe1ad-161">OUTPUTS</span></span>

## <span data-ttu-id="fe1ad-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="fe1ad-162">NOTES</span></span>

## <span data-ttu-id="fe1ad-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fe1ad-163">RELATED LINKS</span></span>

[<span data-ttu-id="fe1ad-164">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe1ad-164">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="fe1ad-165">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe1ad-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="fe1ad-166">Neu – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="fe1ad-166">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
