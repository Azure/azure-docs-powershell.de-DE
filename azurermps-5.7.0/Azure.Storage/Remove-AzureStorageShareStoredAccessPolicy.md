---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: cb39d9800271d68f8ac78ebffc9ed3345209177c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478810"
---
# <span data-ttu-id="d18ce-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d18ce-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="d18ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d18ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d18ce-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="d18ce-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d18ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d18ce-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d18ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d18ce-105">DESCRIPTION</span></span>
<span data-ttu-id="d18ce-106">Das Cmdlet " **Remove-AzureStorageShareStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="d18ce-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="d18ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d18ce-107">EXAMPLES</span></span>

### <span data-ttu-id="d18ce-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Azure Storage-Freigabe</span><span class="sxs-lookup"><span data-stu-id="d18ce-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="d18ce-109">Dieser Befehl entfernt eine gespeicherte Zugriffsrichtlinie mit dem Namen GeneralPolicy aus ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="d18ce-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="d18ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d18ce-110">PARAMETERS</span></span>

### <span data-ttu-id="d18ce-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d18ce-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d18ce-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d18ce-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d18ce-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="d18ce-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d18ce-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d18ce-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d18ce-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d18ce-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d18ce-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="d18ce-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d18ce-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="d18ce-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d18ce-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d18ce-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d18ce-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d18ce-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d18ce-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d18ce-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d18ce-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d18ce-121">-Context</span></span>
<span data-ttu-id="d18ce-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d18ce-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d18ce-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="d18ce-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d18ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d18ce-124">-PassThru</span></span>
<span data-ttu-id="d18ce-125">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d18ce-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d18ce-126">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d18ce-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d18ce-127">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d18ce-127">-Policy</span></span>
<span data-ttu-id="d18ce-128">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d18ce-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d18ce-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d18ce-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d18ce-130">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d18ce-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d18ce-131">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d18ce-131">-ShareName</span></span>
<span data-ttu-id="d18ce-132">Gibt den Speicherfreigabe Namen an, für den dieses Cmdlet eine Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="d18ce-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="d18ce-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d18ce-133">-Confirm</span></span>
<span data-ttu-id="d18ce-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d18ce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d18ce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d18ce-135">-WhatIf</span></span>
<span data-ttu-id="d18ce-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d18ce-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d18ce-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d18ce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d18ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18ce-138">CommonParameters</span></span>
<span data-ttu-id="d18ce-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18ce-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d18ce-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18ce-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d18ce-141">INPUTS</span></span>

### <span data-ttu-id="d18ce-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d18ce-142">IStorageContext</span></span>

<span data-ttu-id="d18ce-143">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d18ce-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d18ce-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d18ce-144">OUTPUTS</span></span>

### <span data-ttu-id="d18ce-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d18ce-145">System.Boolean</span></span>

## <span data-ttu-id="d18ce-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d18ce-146">NOTES</span></span>

## <span data-ttu-id="d18ce-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d18ce-147">RELATED LINKS</span></span>

[<span data-ttu-id="d18ce-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d18ce-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d18ce-149">Neu – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d18ce-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d18ce-150">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d18ce-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d18ce-151">Satz-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d18ce-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
