---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 439000d73f2671b6f7c789e4f690a649b57f027b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658819"
---
# <span data-ttu-id="f858a-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f858a-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="f858a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f858a-102">SYNOPSIS</span></span>
<span data-ttu-id="f858a-103">Erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="f858a-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="f858a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f858a-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f858a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f858a-105">DESCRIPTION</span></span>
<span data-ttu-id="f858a-106">Das Cmdlet **New-AzStorageContainerStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="f858a-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="f858a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f858a-107">EXAMPLES</span></span>

### <span data-ttu-id="f858a-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="f858a-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="f858a-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 im Speichercontainer mit dem Namen MyContainer.</span><span class="sxs-lookup"><span data-stu-id="f858a-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="f858a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f858a-110">PARAMETERS</span></span>

### <span data-ttu-id="f858a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f858a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f858a-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f858a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f858a-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="f858a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f858a-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f858a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f858a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f858a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f858a-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="f858a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f858a-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="f858a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f858a-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f858a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f858a-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="f858a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f858a-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f858a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f858a-121">-Container</span><span class="sxs-lookup"><span data-stu-id="f858a-121">-Container</span></span>
<span data-ttu-id="f858a-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="f858a-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="f858a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f858a-123">-Context</span></span>
<span data-ttu-id="f858a-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f858a-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f858a-125">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f858a-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f858a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f858a-126">-DefaultProfile</span></span>
<span data-ttu-id="f858a-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f858a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f858a-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f858a-128">-ExpiryTime</span></span>
<span data-ttu-id="f858a-129">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="f858a-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f858a-130">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="f858a-130">-Permission</span></span>
<span data-ttu-id="f858a-131">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf den Container zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f858a-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="f858a-132">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="f858a-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f858a-133">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f858a-133">-Policy</span></span>
<span data-ttu-id="f858a-134">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="f858a-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="f858a-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f858a-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f858a-136">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f858a-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f858a-137">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="f858a-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f858a-138">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f858a-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f858a-139">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="f858a-139">-StartTime</span></span>
<span data-ttu-id="f858a-140">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="f858a-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f858a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f858a-141">CommonParameters</span></span>
<span data-ttu-id="f858a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f858a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f858a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f858a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f858a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f858a-144">INPUTS</span></span>

### <span data-ttu-id="f858a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f858a-145">System.String</span></span>

### <span data-ttu-id="f858a-146">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f858a-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f858a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f858a-147">OUTPUTS</span></span>

### <span data-ttu-id="f858a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f858a-148">System.String</span></span>

## <span data-ttu-id="f858a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="f858a-149">NOTES</span></span>

## <span data-ttu-id="f858a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f858a-150">RELATED LINKS</span></span>

[<span data-ttu-id="f858a-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f858a-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f858a-152">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f858a-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f858a-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f858a-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f858a-154">Satz-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f858a-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


