---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: cf9f4b3a6d58754c4b992163625887afcb3439b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849443"
---
# <span data-ttu-id="9877c-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9877c-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="9877c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9877c-102">SYNOPSIS</span></span>
<span data-ttu-id="9877c-103">Ruft CORS-Regeln für einen Speicher Diensttyp ab.</span><span class="sxs-lookup"><span data-stu-id="9877c-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9877c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9877c-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9877c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9877c-105">DESCRIPTION</span></span>
<span data-ttu-id="9877c-106">Das Cmdlet " **Get-AzureStorageCORSRule** " ruft CORS-Regeln (Cross-Origin Resource Sharing) für einen Azure-Speicher Diensttyp ab.</span><span class="sxs-lookup"><span data-stu-id="9877c-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="9877c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9877c-107">EXAMPLES</span></span>

### <span data-ttu-id="9877c-108">Beispiel 1: Abrufen von CORS-Regeln für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="9877c-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="9877c-109">Dieser Befehl ruft die CORS-Regeln für den BLOB-Diensttyp ab.</span><span class="sxs-lookup"><span data-stu-id="9877c-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="9877c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9877c-110">PARAMETERS</span></span>

### <span data-ttu-id="9877c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9877c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9877c-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="9877c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9877c-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="9877c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9877c-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9877c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9877c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9877c-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="9877c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9877c-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="9877c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9877c-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9877c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9877c-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="9877c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9877c-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9877c-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="9877c-121">-Context</span></span>
<span data-ttu-id="9877c-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9877c-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9877c-123">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9877c-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9877c-124">-DefaultProfile</span></span>
<span data-ttu-id="9877c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9877c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9877c-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9877c-127">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9877c-127">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9877c-128">-ServiceType</span></span>
<span data-ttu-id="9877c-129">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet CORS-Regeln erhält.</span><span class="sxs-lookup"><span data-stu-id="9877c-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="9877c-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9877c-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9877c-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="9877c-131">Blob</span></span> 
- <span data-ttu-id="9877c-132">Tabelle</span><span class="sxs-lookup"><span data-stu-id="9877c-132">Table</span></span> 
- <span data-ttu-id="9877c-133">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9877c-133">Queue</span></span> 
- <span data-ttu-id="9877c-134">Datei</span><span class="sxs-lookup"><span data-stu-id="9877c-134">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9877c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9877c-135">CommonParameters</span></span>
<span data-ttu-id="9877c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9877c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9877c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9877c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9877c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9877c-138">INPUTS</span></span>

### <span data-ttu-id="9877c-139">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9877c-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9877c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9877c-140">OUTPUTS</span></span>

### <span data-ttu-id="9877c-141">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="9877c-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="9877c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9877c-142">NOTES</span></span>

## <span data-ttu-id="9877c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9877c-143">RELATED LINKS</span></span>

[<span data-ttu-id="9877c-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9877c-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="9877c-145">Satz-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9877c-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


