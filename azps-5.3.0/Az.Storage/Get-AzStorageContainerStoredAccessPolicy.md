---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374070"
---
# <span data-ttu-id="33d3b-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33d3b-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="33d3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="33d3b-103">Ruft die Richtlinie oder Richtlinien für den gespeicherten Zugriff für einen Azure -Speichercontainer ab.</span><span class="sxs-lookup"><span data-stu-id="33d3b-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="33d3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33d3b-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="33d3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="33d3b-106">Das **Cmdlet "Get-AzStorageContainerStoredAccessPolicy"** listet die gespeicherten Zugriffsrichtlinien für einen Azure -Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="33d3b-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="33d3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="33d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="33d3b-108">Beispiel 1: Erhalten einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="33d3b-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="33d3b-109">Dieser Befehl ruft die Zugriffsrichtlinie mit dem Namen "Policy22" im Speichercontainer namens "Container07" ab.</span><span class="sxs-lookup"><span data-stu-id="33d3b-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="33d3b-110">Beispiel 2: Alle Gespeicherten Zugriffsrichtlinien in einem Speichercontainer erhalten</span><span class="sxs-lookup"><span data-stu-id="33d3b-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="33d3b-111">Dieser Befehl ruft alle Zugriffsrichtlinien im Speichercontainer namens "Container07" ab.</span><span class="sxs-lookup"><span data-stu-id="33d3b-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="33d3b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33d3b-112">PARAMETERS</span></span>

### <span data-ttu-id="33d3b-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33d3b-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="33d3b-114">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="33d3b-115">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33d3b-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="33d3b-116">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="33d3b-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="33d3b-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="33d3b-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="33d3b-118">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="33d3b-119">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="33d3b-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="33d3b-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="33d3b-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="33d3b-121">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="33d3b-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="33d3b-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="33d3b-122">The default value is 10.</span></span>

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

### <span data-ttu-id="33d3b-123">-Container</span><span class="sxs-lookup"><span data-stu-id="33d3b-123">-Container</span></span>
<span data-ttu-id="33d3b-124">Gibt den Namen Ihres Azure -Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d3b-125">-Context</span><span class="sxs-lookup"><span data-stu-id="33d3b-125">-Context</span></span>
<span data-ttu-id="33d3b-126">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="33d3b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d3b-127">-DefaultProfile</span></span>
<span data-ttu-id="33d3b-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33d3b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d3b-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="33d3b-129">-Policy</span></span>
<span data-ttu-id="33d3b-130">Gibt die Azure-Richtlinie für gespeicherten Zugriff an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d3b-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="33d3b-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="33d3b-132">Gibt das intervallseitige Dienstzeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="33d3b-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="33d3b-133">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="33d3b-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="33d3b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d3b-134">CommonParameters</span></span>
<span data-ttu-id="33d3b-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d3b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d3b-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d3b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d3b-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="33d3b-137">INPUTS</span></span>

### <span data-ttu-id="33d3b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="33d3b-138">System.String</span></span>

### <span data-ttu-id="33d3b-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="33d3b-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="33d3b-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="33d3b-140">OUTPUTS</span></span>

### <span data-ttu-id="33d3b-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="33d3b-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="33d3b-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="33d3b-142">NOTES</span></span>

## <span data-ttu-id="33d3b-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="33d3b-143">RELATED LINKS</span></span>

[<span data-ttu-id="33d3b-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33d3b-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="33d3b-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33d3b-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="33d3b-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33d3b-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


