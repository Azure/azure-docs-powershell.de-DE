---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505726"
---
# <span data-ttu-id="2127a-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2127a-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="2127a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2127a-102">SYNOPSIS</span></span>
<span data-ttu-id="2127a-103">Ruft die gespeicherte Zugriffsrichtlinie oder Richtlinien für einen Azure-Speichercontainer ab.</span><span class="sxs-lookup"><span data-stu-id="2127a-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2127a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2127a-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2127a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2127a-105">DESCRIPTION</span></span>
<span data-ttu-id="2127a-106">Das Cmdlet " **Get-AzureStorageContainerStoredAccessPolicy** " listet die gespeicherten Zugriffsrichtlinien oder Richtlinien für einen Azure-Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="2127a-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="2127a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2127a-107">EXAMPLES</span></span>

### <span data-ttu-id="2127a-108">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="2127a-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="2127a-109">Dieser Befehl ruft die Access-Richtlinie mit dem Namen Policy22 im Speichercontainer mit dem Namen Container07 ab.</span><span class="sxs-lookup"><span data-stu-id="2127a-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="2127a-110">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="2127a-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="2127a-111">Dieser Befehl ruft alle Zugriffsrichtlinien im Speichercontainer mit dem Namen Container07 ab.</span><span class="sxs-lookup"><span data-stu-id="2127a-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="2127a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2127a-112">PARAMETERS</span></span>

### <span data-ttu-id="2127a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2127a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2127a-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2127a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2127a-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="2127a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2127a-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2127a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2127a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2127a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2127a-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="2127a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2127a-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="2127a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2127a-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2127a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2127a-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="2127a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2127a-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2127a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="2127a-123">-Container</span><span class="sxs-lookup"><span data-stu-id="2127a-123">-Container</span></span>
<span data-ttu-id="2127a-124">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="2127a-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="2127a-125">-Context</span><span class="sxs-lookup"><span data-stu-id="2127a-125">-Context</span></span>
<span data-ttu-id="2127a-126">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="2127a-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="2127a-127">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="2127a-127">-Policy</span></span>
<span data-ttu-id="2127a-128">Gibt die Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="2127a-128">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="2127a-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2127a-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2127a-130">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2127a-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2127a-131">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2127a-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2127a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2127a-132">CommonParameters</span></span>
<span data-ttu-id="2127a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2127a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2127a-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2127a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2127a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2127a-135">INPUTS</span></span>

### <span data-ttu-id="2127a-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2127a-136">String</span></span>

<span data-ttu-id="2127a-137">Der Parameter "Container" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127a-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="2127a-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2127a-138">IStorageContext</span></span>

<span data-ttu-id="2127a-139">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2127a-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2127a-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2127a-140">OUTPUTS</span></span>

### <span data-ttu-id="2127a-141">Microsoft. WindowsAzure. Storage. BLOB. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="2127a-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="2127a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2127a-142">NOTES</span></span>

## <span data-ttu-id="2127a-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2127a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2127a-144">Neu – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2127a-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2127a-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2127a-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2127a-146">Satz-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2127a-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


