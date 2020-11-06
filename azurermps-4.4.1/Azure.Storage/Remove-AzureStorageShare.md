---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 66662899694f7b1fb93dd109e1dccefee5e00182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503361"
---
# <span data-ttu-id="4fda3-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fda3-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="4fda3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fda3-102">SYNOPSIS</span></span>
<span data-ttu-id="4fda3-103">Löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="4fda3-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fda3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fda3-104">SYNTAX</span></span>

### <span data-ttu-id="4fda3-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="4fda3-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fda3-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="4fda3-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-Force] [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fda3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fda3-107">DESCRIPTION</span></span>
<span data-ttu-id="4fda3-108">Das Cmdlet **Remove-AzureStorageShare** löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="4fda3-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="4fda3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fda3-109">EXAMPLES</span></span>

### <span data-ttu-id="4fda3-110">Beispiel 1: Entfernen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="4fda3-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4fda3-111">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4fda3-111">This command removes the file share named ContosoShare06.</span></span>

## <span data-ttu-id="4fda3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fda3-112">PARAMETERS</span></span>

### <span data-ttu-id="4fda3-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fda3-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4fda3-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4fda3-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="4fda3-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4fda3-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4fda3-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4fda3-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4fda3-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4fda3-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4fda3-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4fda3-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4fda3-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4fda3-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4fda3-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4fda3-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4fda3-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4fda3-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4fda3-123">-Context</span><span class="sxs-lookup"><span data-stu-id="4fda3-123">-Context</span></span>
<span data-ttu-id="4fda3-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fda3-125">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4fda3-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fda3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4fda3-126">-Force</span></span>
<span data-ttu-id="4fda3-127">Erzwingen des Entfernens der Freigabe und des gesamten Inhalts</span><span class="sxs-lookup"><span data-stu-id="4fda3-127">Force to remove the share and all content in it</span></span>

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

### <span data-ttu-id="4fda3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4fda3-128">-Name</span></span>
<span data-ttu-id="4fda3-129">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-129">Specifies the name of the file share.</span></span>
<span data-ttu-id="4fda3-130">Dieses Cmdlet löscht die Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4fda3-130">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fda3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fda3-131">-PassThru</span></span>
<span data-ttu-id="4fda3-132">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="4fda3-132">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4fda3-133">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4fda3-133">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4fda3-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fda3-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4fda3-135">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4fda3-136">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="4fda3-136">-Share</span></span>
<span data-ttu-id="4fda3-137">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-137">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4fda3-138">Dieses Cmdlet entfernt das Objekt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4fda3-138">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="4fda3-139">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fda3-139">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="4fda3-140">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="4fda3-140">This object contains the storage context.</span></span>
<span data-ttu-id="4fda3-141">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="4fda3-141">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="4fda3-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4fda3-142">-Confirm</span></span>
<span data-ttu-id="4fda3-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fda3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fda3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fda3-144">-WhatIf</span></span>
<span data-ttu-id="4fda3-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fda3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fda3-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fda3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fda3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fda3-147">CommonParameters</span></span>
<span data-ttu-id="4fda3-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fda3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fda3-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fda3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fda3-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fda3-150">INPUTS</span></span>

### <span data-ttu-id="4fda3-151">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fda3-151">IStorageContext</span></span>

<span data-ttu-id="4fda3-152">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4fda3-152">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4fda3-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4fda3-153">String</span></span>

<span data-ttu-id="4fda3-154">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4fda3-154">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="4fda3-155">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4fda3-155">CloudFileShare</span></span>

<span data-ttu-id="4fda3-156">Der Parameter "Share" akzeptiert den Wert vom Typ "CloudFileShare" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4fda3-156">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="4fda3-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fda3-157">OUTPUTS</span></span>

## <span data-ttu-id="4fda3-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fda3-158">NOTES</span></span>

## <span data-ttu-id="4fda3-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fda3-159">RELATED LINKS</span></span>

[<span data-ttu-id="4fda3-160">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fda3-160">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4fda3-161">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fda3-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4fda3-162">Neu – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fda3-162">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
