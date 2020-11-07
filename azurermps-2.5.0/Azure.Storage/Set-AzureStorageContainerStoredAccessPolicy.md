---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 490b415d047269b4c725867a702ee172ce51c7ec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849795"
---
# <span data-ttu-id="34a42-101">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34a42-101">Set-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="34a42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34a42-102">SYNOPSIS</span></span>
<span data-ttu-id="34a42-103">Legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="34a42-103">Sets a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34a42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34a42-104">SYNTAX</span></span>

```
Set-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34a42-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34a42-105">DESCRIPTION</span></span>
<span data-ttu-id="34a42-106">Das Cmdlet " **Set-AzureStorageContainerStoredAccessPolicy** " legt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="34a42-106">The **Set-AzureStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="34a42-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34a42-107">EXAMPLES</span></span>

### <span data-ttu-id="34a42-108">Beispiel 1: Festlegen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer mit der vollständigen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="34a42-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="34a42-109">Dieser Befehl legt eine Zugriffsrichtlinie mit dem Namen Policy06 für den Speichercontainer mit dem Namen MyContainer fest.</span><span class="sxs-lookup"><span data-stu-id="34a42-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="34a42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34a42-110">PARAMETERS</span></span>

### <span data-ttu-id="34a42-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34a42-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="34a42-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="34a42-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34a42-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="34a42-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34a42-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="34a42-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34a42-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="34a42-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="34a42-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="34a42-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="34a42-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="34a42-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="34a42-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="34a42-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="34a42-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="34a42-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="34a42-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="34a42-120">The default value is 10.</span></span>

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

### <span data-ttu-id="34a42-121">-Container</span><span class="sxs-lookup"><span data-stu-id="34a42-121">-Container</span></span>
<span data-ttu-id="34a42-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="34a42-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="34a42-123">-Context</span><span class="sxs-lookup"><span data-stu-id="34a42-123">-Context</span></span>
<span data-ttu-id="34a42-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="34a42-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="34a42-125">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34a42-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="34a42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a42-126">-DefaultProfile</span></span>
<span data-ttu-id="34a42-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34a42-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a42-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="34a42-128">-ExpiryTime</span></span>
<span data-ttu-id="34a42-129">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="34a42-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="34a42-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="34a42-130">-NoExpiryTime</span></span>
<span data-ttu-id="34a42-131">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum aufweist.</span><span class="sxs-lookup"><span data-stu-id="34a42-131">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a42-132">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="34a42-132">-NoStartTime</span></span>
<span data-ttu-id="34a42-133">Legt fest, wie lange die Startzeit $Null werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a42-133">Sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a42-134">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="34a42-134">-Permission</span></span>
<span data-ttu-id="34a42-135">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf den Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="34a42-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="34a42-136">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="34a42-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="34a42-137">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="34a42-137">-Policy</span></span>
<span data-ttu-id="34a42-138">Gibt den Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="34a42-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="34a42-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="34a42-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="34a42-140">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="34a42-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="34a42-141">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="34a42-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="34a42-142">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="34a42-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="34a42-143">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="34a42-143">-StartTime</span></span>
<span data-ttu-id="34a42-144">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="34a42-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="34a42-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34a42-145">-Confirm</span></span>
<span data-ttu-id="34a42-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34a42-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a42-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a42-147">-WhatIf</span></span>
<span data-ttu-id="34a42-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34a42-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34a42-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34a42-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34a42-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a42-150">CommonParameters</span></span>
<span data-ttu-id="34a42-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a42-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a42-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a42-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a42-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34a42-153">INPUTS</span></span>

### <span data-ttu-id="34a42-154">System. String</span><span class="sxs-lookup"><span data-stu-id="34a42-154">System.String</span></span>

### <span data-ttu-id="34a42-155">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34a42-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34a42-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34a42-156">OUTPUTS</span></span>

### <span data-ttu-id="34a42-157">System. String</span><span class="sxs-lookup"><span data-stu-id="34a42-157">System.String</span></span>

## <span data-ttu-id="34a42-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="34a42-158">NOTES</span></span>

## <span data-ttu-id="34a42-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34a42-159">RELATED LINKS</span></span>

[<span data-ttu-id="34a42-160">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34a42-160">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="34a42-161">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="34a42-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="34a42-162">Neu – AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34a42-162">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="34a42-163">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="34a42-163">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)
