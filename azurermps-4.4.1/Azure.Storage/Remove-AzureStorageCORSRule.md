---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 5c3475a49c76a9a9617de02519a1f37c29059f31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505698"
---
# <span data-ttu-id="14372-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="14372-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="14372-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14372-102">SYNOPSIS</span></span>
<span data-ttu-id="14372-103">Entfernt CORS für einen Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="14372-103">Removes CORS for a Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14372-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14372-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="14372-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14372-105">DESCRIPTION</span></span>
<span data-ttu-id="14372-106">Das Cmdlet **Remove-AzureStorageCORSRule** entfernt die Ursprungs übergreifende Ressourcenfreigabe (CORS) für einen Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="14372-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="14372-107">Dieses Cmdlet löscht alle CORS-Regeln in einem Speicher Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="14372-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="14372-108">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="14372-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="14372-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14372-109">EXAMPLES</span></span>

### <span data-ttu-id="14372-110">Beispiel 1: Entfernen von CORS-Regeln für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="14372-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="14372-111">Dieser Befehl entfernt CORS-Regeln für den BLOB-Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="14372-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="14372-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="14372-112">PARAMETERS</span></span>

### <span data-ttu-id="14372-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14372-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="14372-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="14372-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="14372-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="14372-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="14372-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="14372-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="14372-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="14372-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="14372-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="14372-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="14372-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="14372-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="14372-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="14372-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="14372-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="14372-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="14372-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="14372-122">The default value is 10.</span></span>

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

### <span data-ttu-id="14372-123">-Context</span><span class="sxs-lookup"><span data-stu-id="14372-123">-Context</span></span>
<span data-ttu-id="14372-124">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="14372-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="14372-125">Zum Abrufen des Speicher Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14372-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="14372-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14372-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="14372-127">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="14372-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="14372-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="14372-128">-ServiceType</span></span>
<span data-ttu-id="14372-129">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln entfernt.</span><span class="sxs-lookup"><span data-stu-id="14372-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="14372-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="14372-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="14372-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="14372-131">Blob</span></span> 
- <span data-ttu-id="14372-132">Tabelle</span><span class="sxs-lookup"><span data-stu-id="14372-132">Table</span></span> 
- <span data-ttu-id="14372-133">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="14372-133">Queue</span></span> 
- <span data-ttu-id="14372-134">Datei</span><span class="sxs-lookup"><span data-stu-id="14372-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14372-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14372-135">CommonParameters</span></span>
<span data-ttu-id="14372-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14372-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14372-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14372-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14372-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14372-138">INPUTS</span></span>

### <span data-ttu-id="14372-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14372-139">IStorageContext</span></span>

<span data-ttu-id="14372-140">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="14372-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="14372-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14372-141">OUTPUTS</span></span>

## <span data-ttu-id="14372-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="14372-142">NOTES</span></span>

## <span data-ttu-id="14372-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14372-143">RELATED LINKS</span></span>

[<span data-ttu-id="14372-144">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="14372-144">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="14372-145">Satz-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="14372-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


