---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
ms.openlocfilehash: b332ed4ec47e5baaa07f579e6ccdbc867b64608e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498614"
---
# <span data-ttu-id="2d543-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d543-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="2d543-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d543-102">SYNOPSIS</span></span>
<span data-ttu-id="2d543-103">Erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="2d543-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d543-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d543-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d543-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d543-105">DESCRIPTION</span></span>
<span data-ttu-id="2d543-106">Das Cmdlet **New-AzureStorageShare** erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="2d543-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="2d543-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d543-107">EXAMPLES</span></span>

### <span data-ttu-id="2d543-108">Beispiel 1: Erstellen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="2d543-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="2d543-109">Dieser Befehl erstellt eine Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="2d543-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="2d543-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d543-110">PARAMETERS</span></span>

### <span data-ttu-id="2d543-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2d543-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2d543-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2d543-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2d543-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="2d543-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2d543-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2d543-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2d543-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2d543-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2d543-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="2d543-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2d543-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="2d543-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2d543-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2d543-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2d543-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="2d543-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2d543-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2d543-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2d543-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2d543-121">-Context</span></span>
<span data-ttu-id="2d543-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="2d543-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2d543-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="2d543-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="2d543-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d543-124">-DefaultProfile</span></span>
<span data-ttu-id="2d543-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d543-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d543-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2d543-126">-Name</span></span>
<span data-ttu-id="2d543-127">Gibt den Namen einer Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="2d543-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="2d543-128">Dieses Cmdlet erstellt eine Dateifreigabe mit dem Namen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2d543-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d543-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2d543-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2d543-130">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="2d543-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="2d543-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d543-131">CommonParameters</span></span>
<span data-ttu-id="2d543-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d543-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d543-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d543-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d543-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d543-134">INPUTS</span></span>

### <span data-ttu-id="2d543-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2d543-135">System.String</span></span>

### <span data-ttu-id="2d543-136">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d543-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d543-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d543-137">OUTPUTS</span></span>

### <span data-ttu-id="2d543-138">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="2d543-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="2d543-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d543-139">NOTES</span></span>

## <span data-ttu-id="2d543-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d543-140">RELATED LINKS</span></span>

[<span data-ttu-id="2d543-141">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d543-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="2d543-142">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d543-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2d543-143">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d543-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
