---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24a61f071e806588976f601df69aa66dbbafc164
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475565"
---
# <span data-ttu-id="cf652-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf652-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="cf652-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf652-102">SYNOPSIS</span></span>
<span data-ttu-id="cf652-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="cf652-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="cf652-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf652-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf652-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf652-105">DESCRIPTION</span></span>
<span data-ttu-id="cf652-106">Das Cmdlet " **Remove-AzureStorageShareStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="cf652-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="cf652-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf652-107">EXAMPLES</span></span>

### <span data-ttu-id="cf652-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Azure Storage-Freigabe</span><span class="sxs-lookup"><span data-stu-id="cf652-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="cf652-109">Dieser Befehl entfernt eine gespeicherte Zugriffsrichtlinie mit dem Namen GeneralPolicy aus ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="cf652-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="cf652-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf652-110">PARAMETERS</span></span>

### <span data-ttu-id="cf652-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf652-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf652-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="cf652-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf652-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="cf652-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf652-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="cf652-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf652-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf652-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf652-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="cf652-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf652-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="cf652-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf652-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="cf652-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf652-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="cf652-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf652-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="cf652-120">The default value is 10.</span></span>

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

### <span data-ttu-id="cf652-121">-Context</span><span class="sxs-lookup"><span data-stu-id="cf652-121">-Context</span></span>
<span data-ttu-id="cf652-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cf652-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cf652-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cf652-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cf652-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf652-124">-PassThru</span></span>
<span data-ttu-id="cf652-125">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="cf652-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cf652-126">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cf652-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cf652-127">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="cf652-127">-Policy</span></span>
<span data-ttu-id="cf652-128">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="cf652-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf652-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf652-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf652-130">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="cf652-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cf652-131">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="cf652-131">-ShareName</span></span>
<span data-ttu-id="cf652-132">Gibt den Speicherfreigabe Namen an, für den dieses Cmdlet eine Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf652-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf652-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf652-133">-Confirm</span></span>
<span data-ttu-id="cf652-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf652-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf652-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf652-135">-WhatIf</span></span>
<span data-ttu-id="cf652-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf652-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf652-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf652-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf652-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf652-138">CommonParameters</span></span>
<span data-ttu-id="cf652-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf652-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf652-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf652-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf652-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf652-141">INPUTS</span></span>

## <span data-ttu-id="cf652-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf652-142">OUTPUTS</span></span>

## <span data-ttu-id="cf652-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf652-143">NOTES</span></span>

## <span data-ttu-id="cf652-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf652-144">RELATED LINKS</span></span>

[<span data-ttu-id="cf652-145">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf652-145">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="cf652-146">Neu – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf652-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="cf652-147">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cf652-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="cf652-148">Satz-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cf652-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
