---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662014"
---
# <span data-ttu-id="5223c-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5223c-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="5223c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5223c-102">SYNOPSIS</span></span>
<span data-ttu-id="5223c-103">Erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="5223c-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="5223c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5223c-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5223c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5223c-105">DESCRIPTION</span></span>
<span data-ttu-id="5223c-106">Das Cmdlet **New-AzureStorageContainerStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="5223c-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="5223c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5223c-107">EXAMPLES</span></span>

### <span data-ttu-id="5223c-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="5223c-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="5223c-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 im Speichercontainer mit dem Namen MyContainer.</span><span class="sxs-lookup"><span data-stu-id="5223c-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="5223c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5223c-110">PARAMETERS</span></span>

### <span data-ttu-id="5223c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5223c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5223c-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5223c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5223c-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="5223c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5223c-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5223c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5223c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5223c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5223c-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="5223c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5223c-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="5223c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5223c-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="5223c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5223c-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="5223c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5223c-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5223c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5223c-121">-Container</span><span class="sxs-lookup"><span data-stu-id="5223c-121">-Container</span></span>
<span data-ttu-id="5223c-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="5223c-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="5223c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5223c-123">-Context</span></span>
<span data-ttu-id="5223c-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5223c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5223c-125">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5223c-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5223c-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5223c-126">-ExpiryTime</span></span>
<span data-ttu-id="5223c-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="5223c-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="5223c-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="5223c-128">-Permission</span></span>
<span data-ttu-id="5223c-129">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="5223c-129">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="5223c-130">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="5223c-130">-Policy</span></span>
<span data-ttu-id="5223c-131">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="5223c-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="5223c-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5223c-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5223c-133">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="5223c-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5223c-134">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="5223c-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5223c-135">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5223c-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5223c-136">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="5223c-136">-StartTime</span></span>
<span data-ttu-id="5223c-137">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="5223c-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="5223c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5223c-138">CommonParameters</span></span>
<span data-ttu-id="5223c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5223c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5223c-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5223c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5223c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5223c-141">INPUTS</span></span>

## <span data-ttu-id="5223c-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5223c-142">OUTPUTS</span></span>

## <span data-ttu-id="5223c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5223c-143">NOTES</span></span>

## <span data-ttu-id="5223c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5223c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5223c-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5223c-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5223c-146">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5223c-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5223c-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5223c-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="5223c-148">Satz-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5223c-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


