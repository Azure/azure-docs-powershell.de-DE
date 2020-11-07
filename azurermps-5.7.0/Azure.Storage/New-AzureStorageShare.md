---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
ms.openlocfilehash: d079c46294899377c958ba56b358394387966b78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662871"
---
# <span data-ttu-id="9dfb9-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9dfb9-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="9dfb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9dfb9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfb9-103">Erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dfb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dfb9-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9dfb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dfb9-105">DESCRIPTION</span></span>
<span data-ttu-id="9dfb9-106">Das Cmdlet **New-AzureStorageShare** erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="9dfb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dfb9-107">EXAMPLES</span></span>

### <span data-ttu-id="9dfb9-108">Beispiel 1: Erstellen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="9dfb9-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="9dfb9-109">Dieser Befehl erstellt eine Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="9dfb9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dfb9-110">PARAMETERS</span></span>

### <span data-ttu-id="9dfb9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9dfb9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9dfb9-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9dfb9-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9dfb9-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9dfb9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9dfb9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9dfb9-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9dfb9-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9dfb9-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9dfb9-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9dfb9-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9dfb9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="9dfb9-121">-Context</span></span>
<span data-ttu-id="9dfb9-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9dfb9-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfb9-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9dfb9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9dfb9-124">-Name</span></span>
<span data-ttu-id="9dfb9-125">Gibt den Namen einer Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="9dfb9-126">Dieses Cmdlet erstellt eine Dateifreigabe mit dem Namen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfb9-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9dfb9-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9dfb9-128">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9dfb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfb9-129">CommonParameters</span></span>
<span data-ttu-id="9dfb9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfb9-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dfb9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfb9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9dfb9-132">INPUTS</span></span>

### <span data-ttu-id="9dfb9-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9dfb9-133">IStorageContext</span></span>

<span data-ttu-id="9dfb9-134">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9dfb9-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9dfb9-135">String</span></span>

<span data-ttu-id="9dfb9-136">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9dfb9-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9dfb9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9dfb9-137">OUTPUTS</span></span>

## <span data-ttu-id="9dfb9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9dfb9-138">NOTES</span></span>

## <span data-ttu-id="9dfb9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9dfb9-139">RELATED LINKS</span></span>

[<span data-ttu-id="9dfb9-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9dfb9-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9dfb9-141">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9dfb9-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9dfb9-142">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9dfb9-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
