---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: d0ca5bcc01d8cf34ce22e0e91e99f0144900231c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499885"
---
# <span data-ttu-id="b8b9f-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9f-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="b8b9f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b8b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b9f-103">Legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8b9f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8b9f-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b9f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8b9f-105">DESCRIPTION</span></span>
<span data-ttu-id="b8b9f-106">Das Cmdlet " **Set-AzureStorageContainerStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="b8b9f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8b9f-107">EXAMPLES</span></span>

### <span data-ttu-id="b8b9f-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="b8b9f-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="b8b9f-109">Dieser Befehl legt eine Zugriffsrichtlinie mit dem Namen Policy06 für den Speichercontainer mit dem Namen MyContainer fest.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="b8b9f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8b9f-110">PARAMETERS</span></span>

### <span data-ttu-id="b8b9f-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8b9f-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8b9f-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8b9f-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8b9f-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8b9f-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8b9f-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8b9f-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8b9f-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8b9f-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8b9f-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8b9f-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b8b9f-121">-Container</span><span class="sxs-lookup"><span data-stu-id="b8b9f-121">-Container</span></span>
<span data-ttu-id="b8b9f-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-123">-Context</span><span class="sxs-lookup"><span data-stu-id="b8b9f-123">-Context</span></span>
<span data-ttu-id="b8b9f-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b8b9f-125">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b8b9f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b8b9f-126">-ExpiryTime</span></span>
<span data-ttu-id="b8b9f-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b8b9f-128">-NoExpiryTime</span></span>
<span data-ttu-id="b8b9f-129">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="b8b9f-130">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="b8b9f-130">-NoStartTime</span></span>
<span data-ttu-id="b8b9f-131">Legt fest, wie lange die Startzeit $Null werden soll.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="b8b9f-132">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="b8b9f-132">-Permission</span></span>
<span data-ttu-id="b8b9f-133">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf den Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-133">Specifies permissions in the stored access policy to access the storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-134">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b8b9f-134">-Policy</span></span>
<span data-ttu-id="b8b9f-135">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-135">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8b9f-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8b9f-137">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8b9f-138">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8b9f-139">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8b9f-140">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="b8b9f-140">-StartTime</span></span>
<span data-ttu-id="b8b9f-141">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-141">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b8b9f-142">-Confirm</span></span>
<span data-ttu-id="b8b9f-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b9f-144">-WhatIf</span></span>
<span data-ttu-id="b8b9f-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8b9f-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b9f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b9f-147">CommonParameters</span></span>
<span data-ttu-id="b8b9f-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b9f-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8b9f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b9f-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b8b9f-150">INPUTS</span></span>

### <span data-ttu-id="b8b9f-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b8b9f-151">String</span></span>

<span data-ttu-id="b8b9f-152">Der Parameter "Container" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-152">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="b8b9f-153">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8b9f-153">IStorageContext</span></span>

<span data-ttu-id="b8b9f-154">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8b9f-154">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b8b9f-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b8b9f-155">OUTPUTS</span></span>

### <span data-ttu-id="b8b9f-156">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b9f-156">System.String</span></span>

## <span data-ttu-id="b8b9f-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="b8b9f-157">NOTES</span></span>

## <span data-ttu-id="b8b9f-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b8b9f-158">RELATED LINKS</span></span>

[<span data-ttu-id="b8b9f-159">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9f-159">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8b9f-160">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8b9f-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b8b9f-161">Neu – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9f-161">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="b8b9f-162">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b8b9f-162">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
