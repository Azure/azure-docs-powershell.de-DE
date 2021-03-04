---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 492ad3713bafa692d0ddf969540b8cab89fc05a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944471"
---
# <span data-ttu-id="5f180-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f180-101">New-AzStorageShare</span></span>

## <span data-ttu-id="5f180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f180-102">SYNOPSIS</span></span>
<span data-ttu-id="5f180-103">Erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="5f180-103">Creates a file share.</span></span>

## <span data-ttu-id="5f180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f180-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f180-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f180-105">DESCRIPTION</span></span>
<span data-ttu-id="5f180-106">Das **Cmdlet New-AzStorageShare** erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="5f180-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="5f180-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f180-107">EXAMPLES</span></span>

### <span data-ttu-id="5f180-108">Beispiel 1: Erstellen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="5f180-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="5f180-109">Mit diesem Befehl wird eine Dateifreigabe namens ContosoShare06 erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f180-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="5f180-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f180-110">PARAMETERS</span></span>

### <span data-ttu-id="5f180-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f180-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f180-112">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="5f180-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f180-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f180-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f180-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5f180-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f180-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f180-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f180-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="5f180-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f180-117">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="5f180-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f180-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="5f180-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f180-119">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="5f180-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f180-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="5f180-120">The default value is 10.</span></span>

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

### <span data-ttu-id="5f180-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5f180-121">-Context</span></span>
<span data-ttu-id="5f180-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5f180-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5f180-123">Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="5f180-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5f180-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f180-124">-DefaultProfile</span></span>
<span data-ttu-id="5f180-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f180-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f180-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5f180-126">-Name</span></span>
<span data-ttu-id="5f180-127">Gibt den Namen einer Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="5f180-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="5f180-128">Dieses Cmdlet erstellt eine Dateifreigabe mit dem Namen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5f180-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f180-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f180-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f180-130">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="5f180-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5f180-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f180-131">CommonParameters</span></span>
<span data-ttu-id="5f180-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f180-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f180-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f180-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f180-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f180-134">INPUTS</span></span>

### <span data-ttu-id="5f180-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5f180-135">System.String</span></span>

### <span data-ttu-id="5f180-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f180-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5f180-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f180-137">OUTPUTS</span></span>

### <span data-ttu-id="5f180-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="5f180-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="5f180-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f180-139">NOTES</span></span>

## <span data-ttu-id="5f180-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f180-140">RELATED LINKS</span></span>

[<span data-ttu-id="5f180-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f180-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="5f180-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f180-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="5f180-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="5f180-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
