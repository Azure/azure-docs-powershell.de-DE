---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471702"
---
# <span data-ttu-id="8b807-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b807-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="8b807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b807-102">SYNOPSIS</span></span>
<span data-ttu-id="8b807-103">Entfernt KORS für einen Speicherdienst.</span><span class="sxs-lookup"><span data-stu-id="8b807-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="8b807-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b807-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8b807-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b807-105">DESCRIPTION</span></span>
<span data-ttu-id="8b807-106">Das **Cmdlet "Remove-AzStorageCORSRule"** entfernt die cross origin-Resource Sharing (CORS) für einen Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8b807-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="8b807-107">Mit diesem Cmdlet werden alle KORS-Regeln eines Speicherdiensttyps gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b807-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="8b807-108">Die Speicherdienste für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="8b807-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="8b807-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b807-109">EXAMPLES</span></span>

### <span data-ttu-id="8b807-110">Beispiel 1: Entfernen von KORS-Regeln für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="8b807-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="8b807-111">Mit diesem Befehl werden DIE KORS-Regeln für den Blob-Diensttyp entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b807-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="8b807-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b807-112">PARAMETERS</span></span>

### <span data-ttu-id="8b807-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b807-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8b807-114">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="8b807-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8b807-115">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b807-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8b807-116">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8b807-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8b807-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8b807-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8b807-118">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="8b807-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8b807-119">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="8b807-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8b807-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8b807-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8b807-121">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8b807-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8b807-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8b807-122">The default value is 10.</span></span>

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

### <span data-ttu-id="8b807-123">-Context</span><span class="sxs-lookup"><span data-stu-id="8b807-123">-Context</span></span>
<span data-ttu-id="8b807-124">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8b807-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8b807-125">Zum Abrufen des Speicherkontexts wird das New-AzStorageContext cmdlet verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b807-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8b807-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b807-126">-DefaultProfile</span></span>
<span data-ttu-id="8b807-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b807-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b807-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8b807-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8b807-129">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8b807-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8b807-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8b807-130">-ServiceType</span></span>
<span data-ttu-id="8b807-131">Gibt den Azure Storage-Diensttyp an, für den dieses Cmdlet Regeln entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b807-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="8b807-132">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8b807-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b807-133">BLOB</span><span class="sxs-lookup"><span data-stu-id="8b807-133">Blob</span></span> 
- <span data-ttu-id="8b807-134">Tabelle</span><span class="sxs-lookup"><span data-stu-id="8b807-134">Table</span></span> 
- <span data-ttu-id="8b807-135">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="8b807-135">Queue</span></span> 
- <span data-ttu-id="8b807-136">Datei</span><span class="sxs-lookup"><span data-stu-id="8b807-136">File</span></span>

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

### <span data-ttu-id="8b807-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b807-137">CommonParameters</span></span>
<span data-ttu-id="8b807-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b807-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b807-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b807-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b807-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b807-140">INPUTS</span></span>

### <span data-ttu-id="8b807-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8b807-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8b807-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b807-142">OUTPUTS</span></span>

### <span data-ttu-id="8b807-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="8b807-143">System.Void</span></span>

## <span data-ttu-id="8b807-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8b807-144">NOTES</span></span>

## <span data-ttu-id="8b807-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8b807-145">RELATED LINKS</span></span>

[<span data-ttu-id="8b807-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b807-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="8b807-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="8b807-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


