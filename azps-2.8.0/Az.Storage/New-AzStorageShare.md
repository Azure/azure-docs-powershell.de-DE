---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 82d4c773c32ae8069218ab1b07bedefd6a549f59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823883"
---
# <span data-ttu-id="a3a95-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a3a95-101">New-AzStorageShare</span></span>

## <span data-ttu-id="a3a95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3a95-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a95-103">Erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="a3a95-103">Creates a file share.</span></span>

## <span data-ttu-id="a3a95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3a95-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3a95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3a95-105">DESCRIPTION</span></span>
<span data-ttu-id="a3a95-106">Das Cmdlet **New-AzStorageShare** erstellt eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="a3a95-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="a3a95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3a95-107">EXAMPLES</span></span>

### <span data-ttu-id="a3a95-108">Beispiel 1: Erstellen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="a3a95-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="a3a95-109">Dieser Befehl erstellt eine Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a3a95-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="a3a95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a95-110">PARAMETERS</span></span>

### <span data-ttu-id="a3a95-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a3a95-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a3a95-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="a3a95-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a3a95-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="a3a95-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a3a95-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a3a95-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a3a95-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a3a95-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a3a95-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="a3a95-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a3a95-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="a3a95-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a3a95-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a3a95-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a3a95-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="a3a95-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a3a95-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="a3a95-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a3a95-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a3a95-121">-Context</span></span>
<span data-ttu-id="a3a95-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="a3a95-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a3a95-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a95-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a3a95-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a95-124">-DefaultProfile</span></span>
<span data-ttu-id="a3a95-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3a95-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a95-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a3a95-126">-Name</span></span>
<span data-ttu-id="a3a95-127">Gibt den Namen einer Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="a3a95-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="a3a95-128">Dieses Cmdlet erstellt eine Dateifreigabe mit dem Namen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a3a95-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3a95-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a3a95-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a3a95-130">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="a3a95-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a3a95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a95-131">CommonParameters</span></span>
<span data-ttu-id="a3a95-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a95-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a95-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a95-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3a95-134">INPUTS</span></span>

### <span data-ttu-id="a3a95-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a3a95-135">System.String</span></span>

### <span data-ttu-id="a3a95-136">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a3a95-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a3a95-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3a95-137">OUTPUTS</span></span>

### <span data-ttu-id="a3a95-138">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a3a95-138">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="a3a95-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3a95-139">NOTES</span></span>

## <span data-ttu-id="a3a95-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3a95-140">RELATED LINKS</span></span>

[<span data-ttu-id="a3a95-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a3a95-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="a3a95-142">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a3a95-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a3a95-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="a3a95-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
