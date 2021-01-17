---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460560"
---
# <span data-ttu-id="32684-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="32684-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="32684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32684-102">SYNOPSIS</span></span>
<span data-ttu-id="32684-103">Ruft DIES -Regeln für einen Speicherdiensttyp ab.</span><span class="sxs-lookup"><span data-stu-id="32684-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="32684-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32684-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="32684-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32684-105">DESCRIPTION</span></span>
<span data-ttu-id="32684-106">Das **Cmdlet "Get-AzStorageCORSRule"** ruft für einen Diensttyp von Azure Storage Regeln für die cross origin-Resource Sharing (CORS) ab.</span><span class="sxs-lookup"><span data-stu-id="32684-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="32684-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32684-107">EXAMPLES</span></span>

### <span data-ttu-id="32684-108">Beispiel 1: Erhalten von KORS-Regeln für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="32684-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="32684-109">Dieser Befehl ruft die CORS-Regeln für den Blob-Diensttyp ab.</span><span class="sxs-lookup"><span data-stu-id="32684-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="32684-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32684-110">PARAMETERS</span></span>

### <span data-ttu-id="32684-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="32684-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="32684-112">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="32684-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="32684-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32684-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="32684-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="32684-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="32684-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="32684-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="32684-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="32684-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="32684-117">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="32684-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="32684-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="32684-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="32684-119">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="32684-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="32684-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="32684-120">The default value is 10.</span></span>

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

### <span data-ttu-id="32684-121">-Context</span><span class="sxs-lookup"><span data-stu-id="32684-121">-Context</span></span>
<span data-ttu-id="32684-122">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="32684-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="32684-123">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32684-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="32684-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32684-124">-DefaultProfile</span></span>
<span data-ttu-id="32684-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32684-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32684-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="32684-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="32684-127">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="32684-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="32684-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="32684-128">-ServiceType</span></span>
<span data-ttu-id="32684-129">Gibt den Azure Storage-Diensttyp an, für den dieses Cmdlet -REGELN erhält.</span><span class="sxs-lookup"><span data-stu-id="32684-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="32684-130">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="32684-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="32684-131">BLOB</span><span class="sxs-lookup"><span data-stu-id="32684-131">Blob</span></span> 
- <span data-ttu-id="32684-132">Tabelle</span><span class="sxs-lookup"><span data-stu-id="32684-132">Table</span></span> 
- <span data-ttu-id="32684-133">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="32684-133">Queue</span></span> 
- <span data-ttu-id="32684-134">Datei</span><span class="sxs-lookup"><span data-stu-id="32684-134">File</span></span>

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

### <span data-ttu-id="32684-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32684-135">CommonParameters</span></span>
<span data-ttu-id="32684-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32684-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32684-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32684-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32684-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32684-138">INPUTS</span></span>

### <span data-ttu-id="32684-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="32684-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="32684-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32684-140">OUTPUTS</span></span>

### <span data-ttu-id="32684-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="32684-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="32684-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32684-142">NOTES</span></span>

## <span data-ttu-id="32684-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32684-143">RELATED LINKS</span></span>

[<span data-ttu-id="32684-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="32684-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="32684-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="32684-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


