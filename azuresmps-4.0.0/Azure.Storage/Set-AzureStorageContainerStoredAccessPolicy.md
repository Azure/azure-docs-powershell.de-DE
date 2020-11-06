---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1bdded3834806e33f4605f626b78fe06bc370bf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475786"
---
# <span data-ttu-id="49806-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49806-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="49806-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49806-102">SYNOPSIS</span></span>
<span data-ttu-id="49806-103">Legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="49806-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="49806-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49806-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49806-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49806-105">DESCRIPTION</span></span>
<span data-ttu-id="49806-106">Das Cmdlet " **Set-AzureStorageContainerStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="49806-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="49806-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49806-107">EXAMPLES</span></span>

### <span data-ttu-id="49806-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="49806-108">Example 1: Set a stored access policy in a storage container</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06"
```

<span data-ttu-id="49806-109">Dieser Befehl legt eine Zugriffsrichtlinie mit dem Namen Policy06 für den Speichercontainer mit dem Namen MyContainer fest.</span><span class="sxs-lookup"><span data-stu-id="49806-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="49806-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="49806-110">PARAMETERS</span></span>

### <span data-ttu-id="49806-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="49806-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="49806-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="49806-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="49806-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="49806-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="49806-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="49806-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="49806-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="49806-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="49806-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="49806-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="49806-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="49806-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="49806-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="49806-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="49806-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="49806-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="49806-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="49806-120">The default value is 10.</span></span>

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

### <span data-ttu-id="49806-121">-Container</span><span class="sxs-lookup"><span data-stu-id="49806-121">-Container</span></span>
<span data-ttu-id="49806-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="49806-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="49806-123">-Context</span><span class="sxs-lookup"><span data-stu-id="49806-123">-Context</span></span>
<span data-ttu-id="49806-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="49806-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="49806-125">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="49806-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="49806-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49806-126">-ExpiryTime</span></span>
<span data-ttu-id="49806-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="49806-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="49806-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49806-128">-NoExpiryTime</span></span>
<span data-ttu-id="49806-129">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="49806-129">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="49806-130">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="49806-130">-NoStartTime</span></span>
<span data-ttu-id="49806-131">Legt fest, wie lange die Startzeit $Null werden soll.</span><span class="sxs-lookup"><span data-stu-id="49806-131">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="49806-132">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="49806-132">-Permission</span></span>
<span data-ttu-id="49806-133">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="49806-133">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="49806-134">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="49806-134">-Policy</span></span>
<span data-ttu-id="49806-135">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="49806-135">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="49806-136">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="49806-136">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="49806-137">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="49806-137">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="49806-138">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="49806-138">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="49806-139">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="49806-139">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="49806-140">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="49806-140">-StartTime</span></span>
<span data-ttu-id="49806-141">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="49806-141">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="49806-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49806-142">-Confirm</span></span>
<span data-ttu-id="49806-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49806-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49806-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49806-144">-WhatIf</span></span>
<span data-ttu-id="49806-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49806-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49806-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49806-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49806-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49806-147">CommonParameters</span></span>
<span data-ttu-id="49806-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49806-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49806-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49806-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49806-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49806-150">INPUTS</span></span>

## <span data-ttu-id="49806-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49806-151">OUTPUTS</span></span>

## <span data-ttu-id="49806-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="49806-152">NOTES</span></span>

## <span data-ttu-id="49806-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49806-153">RELATED LINKS</span></span>

[<span data-ttu-id="49806-154">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49806-154">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="49806-155">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="49806-155">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="49806-156">Neu – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49806-156">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="49806-157">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49806-157">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
