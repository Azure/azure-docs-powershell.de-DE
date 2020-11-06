---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07ca74b29dad61c1cf909f13aefbf35b2048d4aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475201"
---
# <span data-ttu-id="f29f4-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f29f4-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="f29f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f29f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f29f4-103">Löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="f29f4-103">Deletes a file share.</span></span>

## <span data-ttu-id="f29f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f29f4-104">SYNTAX</span></span>

### <span data-ttu-id="f29f4-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="f29f4-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29f4-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="f29f4-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f29f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f29f4-107">DESCRIPTION</span></span>
<span data-ttu-id="f29f4-108">Das Cmdlet **Remove-AzureStorageShare** löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="f29f4-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="f29f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f29f4-109">EXAMPLES</span></span>

### <span data-ttu-id="f29f4-110">Beispiel 1: Entfernen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="f29f4-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="f29f4-111">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="f29f4-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="f29f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f29f4-112">PARAMETERS</span></span>

### <span data-ttu-id="f29f4-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f29f4-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f29f4-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f29f4-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="f29f4-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f29f4-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f29f4-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f29f4-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f29f4-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f29f4-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f29f4-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="f29f4-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f29f4-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f29f4-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f29f4-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="f29f4-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f29f4-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f29f4-122">The default value is 10.</span></span>

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

### <span data-ttu-id="f29f4-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f29f4-123">-Context</span></span>
<span data-ttu-id="f29f4-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f29f4-125">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="f29f4-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f29f4-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f29f4-126">-Force</span></span>
<span data-ttu-id="f29f4-127">Erzwingen des Entfernens der Freigabe und des gesamten Inhalts</span><span class="sxs-lookup"><span data-stu-id="f29f4-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="f29f4-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f29f4-128">-Name</span></span>
<span data-ttu-id="f29f4-129">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="f29f4-130">Dieses Cmdlet löscht die Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f29f4-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="f29f4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f29f4-131">-PassThru</span></span>
<span data-ttu-id="f29f4-132">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="f29f4-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f29f4-133">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f29f4-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f29f4-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f29f4-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f29f4-135">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f29f4-136">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="f29f4-136">-Share</span></span>
<span data-ttu-id="f29f4-137">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f29f4-138">Dieses Cmdlet entfernt das Objekt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f29f4-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="f29f4-139">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f29f4-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="f29f4-140">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="f29f4-140">This object contains the storage context.</span></span>
<span data-ttu-id="f29f4-141">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="f29f4-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="f29f4-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f29f4-142">-Confirm</span></span>
<span data-ttu-id="f29f4-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f29f4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f29f4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29f4-144">-WhatIf</span></span>
<span data-ttu-id="f29f4-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f29f4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29f4-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f29f4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f29f4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29f4-147">CommonParameters</span></span>
<span data-ttu-id="f29f4-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29f4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29f4-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29f4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29f4-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f29f4-150">INPUTS</span></span>

## <span data-ttu-id="f29f4-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f29f4-151">OUTPUTS</span></span>

## <span data-ttu-id="f29f4-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="f29f4-152">NOTES</span></span>

## <span data-ttu-id="f29f4-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f29f4-153">RELATED LINKS</span></span>

[<span data-ttu-id="f29f4-154">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f29f4-154">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="f29f4-155">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f29f4-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f29f4-156">Neu – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="f29f4-156">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
