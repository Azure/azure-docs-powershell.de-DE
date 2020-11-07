---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: a4013543cfd96a1aaae591a9f1b1ed4b6da46155
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823879"
---
# <span data-ttu-id="96cbc-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cbc-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="96cbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="96cbc-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="96cbc-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="96cbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96cbc-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="96cbc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="96cbc-106">Das Cmdlet **New-AzStorageShareStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="96cbc-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="96cbc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96cbc-107">EXAMPLES</span></span>

### <span data-ttu-id="96cbc-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="96cbc-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="96cbc-109">Mit diesem Befehl wird eine gespeicherte Zugriffsrichtlinie erstellt, die über die Berechtigung "Vollzugriff" in einer Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="96cbc-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="96cbc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96cbc-110">PARAMETERS</span></span>

### <span data-ttu-id="96cbc-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96cbc-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="96cbc-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96cbc-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="96cbc-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96cbc-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="96cbc-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96cbc-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="96cbc-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="96cbc-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="96cbc-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="96cbc-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="96cbc-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="96cbc-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="96cbc-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="96cbc-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="96cbc-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="96cbc-120">The default value is 10.</span></span>

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

### <span data-ttu-id="96cbc-121">-Context</span><span class="sxs-lookup"><span data-stu-id="96cbc-121">-Context</span></span>
<span data-ttu-id="96cbc-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96cbc-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="96cbc-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="96cbc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cbc-124">-DefaultProfile</span></span>
<span data-ttu-id="96cbc-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96cbc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96cbc-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96cbc-126">-ExpiryTime</span></span>
<span data-ttu-id="96cbc-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="96cbc-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cbc-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="96cbc-128">-Permission</span></span>
<span data-ttu-id="96cbc-129">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf die Speicherfreigabe oder Dateien unter dieser an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="96cbc-130">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="96cbc-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cbc-131">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="96cbc-131">-Policy</span></span>
<span data-ttu-id="96cbc-132">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cbc-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96cbc-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="96cbc-134">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="96cbc-135">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="96cbc-135">-ShareName</span></span>
<span data-ttu-id="96cbc-136">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="96cbc-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="96cbc-137">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="96cbc-137">-StartTime</span></span>
<span data-ttu-id="96cbc-138">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="96cbc-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96cbc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cbc-139">CommonParameters</span></span>
<span data-ttu-id="96cbc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96cbc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cbc-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cbc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cbc-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96cbc-142">INPUTS</span></span>

### <span data-ttu-id="96cbc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="96cbc-143">System.String</span></span>

### <span data-ttu-id="96cbc-144">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cbc-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96cbc-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96cbc-145">OUTPUTS</span></span>

### <span data-ttu-id="96cbc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="96cbc-146">System.String</span></span>

## <span data-ttu-id="96cbc-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="96cbc-147">NOTES</span></span>

## <span data-ttu-id="96cbc-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96cbc-148">RELATED LINKS</span></span>

[<span data-ttu-id="96cbc-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cbc-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="96cbc-150">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cbc-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="96cbc-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cbc-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="96cbc-152">Satz-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cbc-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
