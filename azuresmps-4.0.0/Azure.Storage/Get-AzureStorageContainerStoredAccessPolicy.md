---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e9ea56c53d73b9c71d2eade4fec7025466ed82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475686"
---
# <span data-ttu-id="563d9-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="563d9-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="563d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="563d9-102">SYNOPSIS</span></span>
<span data-ttu-id="563d9-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für einen Azure-Speichercontainer ab.</span><span class="sxs-lookup"><span data-stu-id="563d9-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="563d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="563d9-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="563d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="563d9-105">DESCRIPTION</span></span>
<span data-ttu-id="563d9-106">Das Cmdlet " **Get-AzureStorageContainerStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für einen Azure-Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="563d9-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="563d9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="563d9-107">EXAMPLES</span></span>

### <span data-ttu-id="563d9-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="563d9-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="563d9-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy22 im Speichercontainer mit dem Namen Container07 ab.</span><span class="sxs-lookup"><span data-stu-id="563d9-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="563d9-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="563d9-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="563d9-111">Dieser Befehl ruft alle Zugriffsrichtlinien im Speichercontainer mit dem Namen Container07 ab.</span><span class="sxs-lookup"><span data-stu-id="563d9-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="563d9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="563d9-112">PARAMETERS</span></span>

### <span data-ttu-id="563d9-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="563d9-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="563d9-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="563d9-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="563d9-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="563d9-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="563d9-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="563d9-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="563d9-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="563d9-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="563d9-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="563d9-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="563d9-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="563d9-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="563d9-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="563d9-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="563d9-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="563d9-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="563d9-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="563d9-122">The default value is 10.</span></span>

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

### <span data-ttu-id="563d9-123">-Container</span><span class="sxs-lookup"><span data-stu-id="563d9-123">-Container</span></span>
<span data-ttu-id="563d9-124">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="563d9-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="563d9-125">-Context</span><span class="sxs-lookup"><span data-stu-id="563d9-125">-Context</span></span>
<span data-ttu-id="563d9-126">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="563d9-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="563d9-127">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="563d9-127">-Policy</span></span>
<span data-ttu-id="563d9-128">Gibt die Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="563d9-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563d9-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="563d9-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="563d9-130">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="563d9-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="563d9-131">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="563d9-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="563d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563d9-132">CommonParameters</span></span>
<span data-ttu-id="563d9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="563d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563d9-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563d9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563d9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="563d9-135">INPUTS</span></span>

## <span data-ttu-id="563d9-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="563d9-136">OUTPUTS</span></span>

## <span data-ttu-id="563d9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="563d9-137">NOTES</span></span>

## <span data-ttu-id="563d9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="563d9-138">RELATED LINKS</span></span>

[<span data-ttu-id="563d9-139">Neu – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="563d9-139">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="563d9-140">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="563d9-140">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="563d9-141">Satz-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="563d9-141">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


