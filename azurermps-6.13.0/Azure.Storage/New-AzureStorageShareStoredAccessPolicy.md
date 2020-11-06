---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 823ae6183021e368933af8d2e01a61f0b582323e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480690"
---
# <span data-ttu-id="dcd00-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd00-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="dcd00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dcd00-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd00-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="dcd00-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcd00-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dcd00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcd00-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd00-106">Das Cmdlet **New-AzureStorageShareStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="dcd00-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="dcd00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dcd00-107">EXAMPLES</span></span>

### <span data-ttu-id="dcd00-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="dcd00-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="dcd00-109">Mit diesem Befehl wird eine gespeicherte Zugriffsrichtlinie erstellt, die über die Berechtigung "Vollzugriff" in einer Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="dcd00-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="dcd00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcd00-110">PARAMETERS</span></span>

### <span data-ttu-id="dcd00-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd00-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dcd00-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dcd00-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="dcd00-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dcd00-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="dcd00-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dcd00-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dcd00-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dcd00-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dcd00-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="dcd00-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dcd00-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="dcd00-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dcd00-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="dcd00-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dcd00-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="dcd00-120">The default value is 10.</span></span>

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

### <span data-ttu-id="dcd00-121">-Context</span><span class="sxs-lookup"><span data-stu-id="dcd00-121">-Context</span></span>
<span data-ttu-id="dcd00-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dcd00-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="dcd00-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dcd00-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd00-124">-DefaultProfile</span></span>
<span data-ttu-id="dcd00-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dcd00-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd00-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dcd00-126">-ExpiryTime</span></span>
<span data-ttu-id="dcd00-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="dcd00-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="dcd00-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="dcd00-128">-Permission</span></span>
<span data-ttu-id="dcd00-129">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf die Speicherfreigabe oder Dateien unter dieser an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="dcd00-130">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="dcd00-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="dcd00-131">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="dcd00-131">-Policy</span></span>
<span data-ttu-id="dcd00-132">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-132">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="dcd00-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd00-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dcd00-134">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dcd00-135">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="dcd00-135">-ShareName</span></span>
<span data-ttu-id="dcd00-136">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="dcd00-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="dcd00-137">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="dcd00-137">-StartTime</span></span>
<span data-ttu-id="dcd00-138">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="dcd00-138">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="dcd00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd00-139">CommonParameters</span></span>
<span data-ttu-id="dcd00-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd00-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd00-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd00-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dcd00-142">INPUTS</span></span>

### <span data-ttu-id="dcd00-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dcd00-143">System.String</span></span>

### <span data-ttu-id="dcd00-144">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd00-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dcd00-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dcd00-145">OUTPUTS</span></span>

### <span data-ttu-id="dcd00-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dcd00-146">System.String</span></span>

## <span data-ttu-id="dcd00-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="dcd00-147">NOTES</span></span>

## <span data-ttu-id="dcd00-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dcd00-148">RELATED LINKS</span></span>

[<span data-ttu-id="dcd00-149">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd00-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="dcd00-150">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd00-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dcd00-151">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd00-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="dcd00-152">Satz-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd00-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
