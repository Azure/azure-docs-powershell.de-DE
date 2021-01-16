---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376240"
---
# <span data-ttu-id="38d84-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38d84-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="38d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d84-102">SYNOPSIS</span></span>
<span data-ttu-id="38d84-103">Ruft gespeicherte Zugriffsrichtlinien für eine Speicherfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="38d84-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="38d84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38d84-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="38d84-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38d84-105">DESCRIPTION</span></span>
<span data-ttu-id="38d84-106">Das **Cmdlet "Get-AzStorageShareStoredAccessPolicy"** ruft gespeicherte Zugriffsrichtlinien für eine Azure Storage Share ab.</span><span class="sxs-lookup"><span data-stu-id="38d84-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="38d84-107">Um eine bestimmte Richtlinie zu erhalten, geben Sie sie nach Name an.</span><span class="sxs-lookup"><span data-stu-id="38d84-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="38d84-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38d84-108">EXAMPLES</span></span>

### <span data-ttu-id="38d84-109">Beispiel 1: Erhalten einer gespeicherten Zugriffsrichtlinie in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="38d84-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="38d84-110">Dieser Befehl ruft eine gespeicherte Zugriffsrichtlinie namens "GeneralPolicy" in ContosoShare ab.</span><span class="sxs-lookup"><span data-stu-id="38d84-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="38d84-111">Beispiel 2: Freigeben aller Gespeicherten Zugriffsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="38d84-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="38d84-112">Dieser Befehl ruft alle Richtlinien für gespeicherten Zugriff in ContosoShare ab.</span><span class="sxs-lookup"><span data-stu-id="38d84-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="38d84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d84-113">PARAMETERS</span></span>

### <span data-ttu-id="38d84-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38d84-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="38d84-115">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="38d84-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="38d84-116">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d84-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="38d84-117">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="38d84-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="38d84-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="38d84-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="38d84-119">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="38d84-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="38d84-120">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="38d84-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="38d84-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="38d84-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="38d84-122">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="38d84-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="38d84-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="38d84-123">The default value is 10.</span></span>

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

### <span data-ttu-id="38d84-124">-Context</span><span class="sxs-lookup"><span data-stu-id="38d84-124">-Context</span></span>
<span data-ttu-id="38d84-125">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="38d84-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="38d84-126">Verwenden Sie zum Abrufen eines Kontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="38d84-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="38d84-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d84-127">-DefaultProfile</span></span>
<span data-ttu-id="38d84-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38d84-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d84-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="38d84-129">-Policy</span></span>
<span data-ttu-id="38d84-130">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="38d84-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38d84-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="38d84-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="38d84-132">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="38d84-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="38d84-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="38d84-133">-ShareName</span></span>
<span data-ttu-id="38d84-134">Gibt den Speicherfreigabenamen an, für den dieses Cmdlet Richtlinien erhält.</span><span class="sxs-lookup"><span data-stu-id="38d84-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="38d84-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d84-135">CommonParameters</span></span>
<span data-ttu-id="38d84-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d84-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d84-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d84-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d84-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38d84-138">INPUTS</span></span>

### <span data-ttu-id="38d84-139">System.String</span><span class="sxs-lookup"><span data-stu-id="38d84-139">System.String</span></span>

### <span data-ttu-id="38d84-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="38d84-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38d84-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38d84-141">OUTPUTS</span></span>

### <span data-ttu-id="38d84-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="38d84-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="38d84-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38d84-143">NOTES</span></span>

## <span data-ttu-id="38d84-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38d84-144">RELATED LINKS</span></span>

[<span data-ttu-id="38d84-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="38d84-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="38d84-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38d84-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="38d84-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38d84-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="38d84-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="38d84-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
