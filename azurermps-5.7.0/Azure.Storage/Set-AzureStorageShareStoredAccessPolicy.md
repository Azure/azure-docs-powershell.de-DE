---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 0c77d2dedadd205a659bf296e02c09b98342dcc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665216"
---
# <span data-ttu-id="5f34c-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f34c-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="5f34c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f34c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f34c-103">Aktualisiert eine gespeicherte Zugriffsrichtlinie für eine Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="5f34c-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f34c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f34c-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f34c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f34c-105">DESCRIPTION</span></span>
<span data-ttu-id="5f34c-106">Das Cmdlet " **Satz-AzureStorageShareStoredAccessPolicy** " aktualisiert die gespeicherte Zugriffsrichtlinie für eine Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="5f34c-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="5f34c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f34c-107">EXAMPLES</span></span>

### <span data-ttu-id="5f34c-108">Beispiel 1: Aktualisieren einer gespeicherten Zugriffsrichtlinie in der Speicherfreigabe</span><span class="sxs-lookup"><span data-stu-id="5f34c-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="5f34c-109">Dieser Befehl aktualisiert eine gespeicherte Zugriffsrichtlinie, die über die Berechtigung "Vollzugriff" in einer Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="5f34c-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="5f34c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f34c-110">PARAMETERS</span></span>

### <span data-ttu-id="5f34c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f34c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f34c-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f34c-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="5f34c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f34c-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5f34c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f34c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f34c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f34c-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f34c-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="5f34c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f34c-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="5f34c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f34c-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="5f34c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f34c-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5f34c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5f34c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5f34c-121">-Context</span></span>
<span data-ttu-id="5f34c-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f34c-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="5f34c-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5f34c-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f34c-124">-ExpiryTime</span></span>
<span data-ttu-id="5f34c-125">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="5f34c-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="5f34c-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5f34c-126">-NoExpiryTime</span></span>
<span data-ttu-id="5f34c-127">Gibt an, dass dieses Cmdlet die **ExpiryTime** -Eigenschaft in der gespeicherten Zugriffsrichtlinie löscht.</span><span class="sxs-lookup"><span data-stu-id="5f34c-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="5f34c-128">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="5f34c-128">-NoStartTime</span></span>
<span data-ttu-id="5f34c-129">Gibt an, dass dieses Cmdlet die **Startwert-Eigenschaft** in der gespeicherten Zugriffsrichtlinie löscht.</span><span class="sxs-lookup"><span data-stu-id="5f34c-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="5f34c-130">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5f34c-130">-Permission</span></span>
<span data-ttu-id="5f34c-131">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf die freigegebenen Dateien oder Dateien an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="5f34c-132">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5f34c-132">-Policy</span></span>
<span data-ttu-id="5f34c-133">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="5f34c-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f34c-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f34c-135">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5f34c-136">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="5f34c-136">-ShareName</span></span>
<span data-ttu-id="5f34c-137">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="5f34c-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="5f34c-138">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="5f34c-138">-StartTime</span></span>
<span data-ttu-id="5f34c-139">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="5f34c-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="5f34c-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f34c-140">-Confirm</span></span>
<span data-ttu-id="5f34c-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f34c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f34c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f34c-142">-WhatIf</span></span>
<span data-ttu-id="5f34c-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f34c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f34c-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f34c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f34c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f34c-145">CommonParameters</span></span>
<span data-ttu-id="5f34c-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f34c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f34c-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f34c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f34c-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f34c-148">INPUTS</span></span>

### <span data-ttu-id="5f34c-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f34c-149">IStorageContext</span></span>

<span data-ttu-id="5f34c-150">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f34c-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5f34c-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f34c-151">String</span></span>

<span data-ttu-id="5f34c-152">Der Parameter "Freigabename" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f34c-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5f34c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f34c-153">OUTPUTS</span></span>

### <span data-ttu-id="5f34c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5f34c-154">System.String</span></span>

## <span data-ttu-id="5f34c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f34c-155">NOTES</span></span>

## <span data-ttu-id="5f34c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f34c-156">RELATED LINKS</span></span>

[<span data-ttu-id="5f34c-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f34c-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="5f34c-158">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f34c-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5f34c-159">Neu – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f34c-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="5f34c-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f34c-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
