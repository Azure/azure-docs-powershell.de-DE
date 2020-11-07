---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 58fc0ef20300f57407d7df35f1732830dbc4c5d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658733"
---
# <span data-ttu-id="538e4-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="538e4-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="538e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="538e4-102">SYNOPSIS</span></span>
<span data-ttu-id="538e4-103">Aktualisiert eine gespeicherte Zugriffsrichtlinie für eine Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="538e4-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="538e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="538e4-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="538e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538e4-105">DESCRIPTION</span></span>
<span data-ttu-id="538e4-106">Das Cmdlet " **Satz-AzStorageShareStoredAccessPolicy** " aktualisiert die gespeicherte Zugriffsrichtlinie für eine Azure-Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="538e4-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="538e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="538e4-107">EXAMPLES</span></span>

### <span data-ttu-id="538e4-108">Beispiel 1: Aktualisieren einer gespeicherten Zugriffsrichtlinie in der Speicherfreigabe</span><span class="sxs-lookup"><span data-stu-id="538e4-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="538e4-109">Dieser Befehl aktualisiert eine gespeicherte Zugriffsrichtlinie, die über die Berechtigung "Vollzugriff" in einer Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="538e4-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="538e4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="538e4-110">PARAMETERS</span></span>

### <span data-ttu-id="538e4-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="538e4-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="538e4-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="538e4-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="538e4-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="538e4-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="538e4-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="538e4-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="538e4-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="538e4-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="538e4-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="538e4-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="538e4-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="538e4-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="538e4-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="538e4-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="538e4-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="538e4-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="538e4-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="538e4-120">The default value is 10.</span></span>

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

### <span data-ttu-id="538e4-121">-Context</span><span class="sxs-lookup"><span data-stu-id="538e4-121">-Context</span></span>
<span data-ttu-id="538e4-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="538e4-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="538e4-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="538e4-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="538e4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538e4-124">-DefaultProfile</span></span>
<span data-ttu-id="538e4-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="538e4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="538e4-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="538e4-126">-ExpiryTime</span></span>
<span data-ttu-id="538e4-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="538e4-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="538e4-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="538e4-128">-NoExpiryTime</span></span>
<span data-ttu-id="538e4-129">Gibt an, dass dieses Cmdlet die **ExpiryTime** -Eigenschaft in der gespeicherten Zugriffsrichtlinie löscht.</span><span class="sxs-lookup"><span data-stu-id="538e4-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="538e4-130">-Nostartzeit</span><span class="sxs-lookup"><span data-stu-id="538e4-130">-NoStartTime</span></span>
<span data-ttu-id="538e4-131">Gibt an, dass dieses Cmdlet die **Startwert-Eigenschaft** in der gespeicherten Zugriffsrichtlinie löscht.</span><span class="sxs-lookup"><span data-stu-id="538e4-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="538e4-132">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="538e4-132">-Permission</span></span>
<span data-ttu-id="538e4-133">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie für den Zugriff auf die freigegebenen Dateien oder Dateien an.</span><span class="sxs-lookup"><span data-stu-id="538e4-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="538e4-134">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="538e4-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="538e4-135">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="538e4-135">-Policy</span></span>
<span data-ttu-id="538e4-136">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="538e4-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="538e4-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="538e4-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="538e4-138">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="538e4-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="538e4-139">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="538e4-139">-ShareName</span></span>
<span data-ttu-id="538e4-140">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="538e4-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="538e4-141">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="538e4-141">-StartTime</span></span>
<span data-ttu-id="538e4-142">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="538e4-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="538e4-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="538e4-143">-Confirm</span></span>
<span data-ttu-id="538e4-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="538e4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="538e4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="538e4-145">-WhatIf</span></span>
<span data-ttu-id="538e4-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="538e4-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="538e4-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="538e4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="538e4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538e4-148">CommonParameters</span></span>
<span data-ttu-id="538e4-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="538e4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538e4-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="538e4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538e4-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="538e4-151">INPUTS</span></span>

### <span data-ttu-id="538e4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="538e4-152">System.String</span></span>

### <span data-ttu-id="538e4-153">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="538e4-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="538e4-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="538e4-154">OUTPUTS</span></span>

### <span data-ttu-id="538e4-155">System. String</span><span class="sxs-lookup"><span data-stu-id="538e4-155">System.String</span></span>

## <span data-ttu-id="538e4-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="538e4-156">NOTES</span></span>

## <span data-ttu-id="538e4-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="538e4-157">RELATED LINKS</span></span>

[<span data-ttu-id="538e4-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="538e4-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="538e4-159">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="538e4-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="538e4-160">Neu – AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="538e4-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="538e4-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="538e4-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
