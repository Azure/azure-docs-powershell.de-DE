---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 8780b5e356192db65b31876cc528f9105b251080
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843039"
---
# <span data-ttu-id="b7890-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7890-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b7890-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7890-102">SYNOPSIS</span></span>
<span data-ttu-id="b7890-103">Ruft gespeicherte Zugriffsrichtlinien für eine Speicherfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="b7890-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="b7890-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7890-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b7890-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7890-105">DESCRIPTION</span></span>
<span data-ttu-id="b7890-106">Das Cmdlet " **Get-AzStorageShareStoredAccessPolicy** " ruft gespeicherte Zugriffsrichtlinien für eine Azure-Speicherfreigabe ab.</span><span class="sxs-lookup"><span data-stu-id="b7890-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="b7890-107">Wenn Sie eine bestimmte Richtlinie abrufen möchten, geben Sie Sie über den Namen an.</span><span class="sxs-lookup"><span data-stu-id="b7890-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="b7890-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7890-108">EXAMPLES</span></span>

### <span data-ttu-id="b7890-109">Beispiel 1: Abrufen einer gespeicherten Zugriffsrichtlinie in einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="b7890-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="b7890-110">Dieser Befehl ruft eine gespeicherte Zugriffsrichtlinie mit dem Namen GeneralPolicy in ContosoShare ab.</span><span class="sxs-lookup"><span data-stu-id="b7890-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="b7890-111">Beispiel 2: Abrufen aller gespeicherten Zugriffsrichtlinien in share</span><span class="sxs-lookup"><span data-stu-id="b7890-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="b7890-112">Dieser Befehl ruft alle gespeicherten Zugriffsrichtlinien in ContosoShare ab.</span><span class="sxs-lookup"><span data-stu-id="b7890-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="b7890-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7890-113">PARAMETERS</span></span>

### <span data-ttu-id="b7890-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7890-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b7890-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="b7890-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b7890-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="b7890-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b7890-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b7890-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b7890-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b7890-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b7890-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="b7890-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b7890-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="b7890-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b7890-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b7890-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b7890-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="b7890-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b7890-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b7890-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b7890-124">-Context</span><span class="sxs-lookup"><span data-stu-id="b7890-124">-Context</span></span>
<span data-ttu-id="b7890-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b7890-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b7890-126">Verwenden Sie zum Abrufen eines Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="b7890-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b7890-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7890-127">-DefaultProfile</span></span>
<span data-ttu-id="b7890-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7890-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7890-129">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="b7890-129">-Policy</span></span>
<span data-ttu-id="b7890-130">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b7890-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7890-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b7890-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b7890-132">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b7890-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b7890-133">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="b7890-133">-ShareName</span></span>
<span data-ttu-id="b7890-134">Gibt den Speicherfreigabe Namen an, für den dieses Cmdlet Richtlinien erhält.</span><span class="sxs-lookup"><span data-stu-id="b7890-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="b7890-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7890-135">CommonParameters</span></span>
<span data-ttu-id="b7890-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7890-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7890-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7890-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7890-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7890-138">INPUTS</span></span>

### <span data-ttu-id="b7890-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b7890-139">System.String</span></span>

### <span data-ttu-id="b7890-140">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7890-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b7890-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7890-141">OUTPUTS</span></span>

### <span data-ttu-id="b7890-142">Microsoft. WindowsAz. Storage. File. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="b7890-142">Microsoft.WindowsAz.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="b7890-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7890-143">NOTES</span></span>

## <span data-ttu-id="b7890-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7890-144">RELATED LINKS</span></span>

[<span data-ttu-id="b7890-145">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b7890-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b7890-146">Neu – AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7890-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b7890-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7890-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b7890-148">Satz-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b7890-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
