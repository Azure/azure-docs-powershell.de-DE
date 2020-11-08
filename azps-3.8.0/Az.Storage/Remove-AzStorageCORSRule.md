---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004867"
---
# <span data-ttu-id="a9efc-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a9efc-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="a9efc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9efc-102">SYNOPSIS</span></span>
<span data-ttu-id="a9efc-103">Entfernt CORS für einen Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="a9efc-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="a9efc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9efc-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a9efc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9efc-105">DESCRIPTION</span></span>
<span data-ttu-id="a9efc-106">Das Cmdlet **Remove-AzStorageCORSRule** entfernt die Ursprungs übergreifende Ressourcenfreigabe (CORS) für einen Azure-Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="a9efc-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="a9efc-107">Dieses Cmdlet löscht alle CORS-Regeln in einem Speicher Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="a9efc-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="a9efc-108">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="a9efc-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="a9efc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9efc-109">EXAMPLES</span></span>

### <span data-ttu-id="a9efc-110">Beispiel 1: Entfernen von CORS-Regeln für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="a9efc-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="a9efc-111">Dieser Befehl entfernt CORS-Regeln für den BLOB-Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="a9efc-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="a9efc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9efc-112">PARAMETERS</span></span>

### <span data-ttu-id="a9efc-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9efc-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a9efc-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a9efc-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a9efc-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="a9efc-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a9efc-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a9efc-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9efc-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a9efc-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a9efc-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="a9efc-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a9efc-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="a9efc-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a9efc-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a9efc-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a9efc-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a9efc-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a9efc-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a9efc-122">The default value is 10.</span></span>

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

### <span data-ttu-id="a9efc-123">-Context</span><span class="sxs-lookup"><span data-stu-id="a9efc-123">-Context</span></span>
<span data-ttu-id="a9efc-124">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a9efc-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a9efc-125">Zum Abrufen des Speicher Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9efc-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9efc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9efc-126">-DefaultProfile</span></span>
<span data-ttu-id="a9efc-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9efc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9efc-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a9efc-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a9efc-129">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="a9efc-129">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9efc-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a9efc-130">-ServiceType</span></span>
<span data-ttu-id="a9efc-131">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9efc-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="a9efc-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a9efc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9efc-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="a9efc-133">Blob</span></span> 
- <span data-ttu-id="a9efc-134">Tabelle</span><span class="sxs-lookup"><span data-stu-id="a9efc-134">Table</span></span> 
- <span data-ttu-id="a9efc-135">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="a9efc-135">Queue</span></span> 
- <span data-ttu-id="a9efc-136">Datei</span><span class="sxs-lookup"><span data-stu-id="a9efc-136">File</span></span>

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

### <span data-ttu-id="a9efc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9efc-137">CommonParameters</span></span>
<span data-ttu-id="a9efc-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9efc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9efc-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9efc-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9efc-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9efc-140">INPUTS</span></span>

### <span data-ttu-id="a9efc-141">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9efc-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9efc-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9efc-142">OUTPUTS</span></span>

### <span data-ttu-id="a9efc-143">System. void</span><span class="sxs-lookup"><span data-stu-id="a9efc-143">System.Void</span></span>

## <span data-ttu-id="a9efc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9efc-144">NOTES</span></span>

## <span data-ttu-id="a9efc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9efc-145">RELATED LINKS</span></span>

[<span data-ttu-id="a9efc-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a9efc-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="a9efc-147">Satz-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="a9efc-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


