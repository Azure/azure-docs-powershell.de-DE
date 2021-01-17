---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303307"
---
# <span data-ttu-id="734d0-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="734d0-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="734d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="734d0-102">SYNOPSIS</span></span>
<span data-ttu-id="734d0-103">Legt eine Richtlinie für den gespeicherten Zugriff für einen Azure -Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="734d0-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="734d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="734d0-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="734d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="734d0-105">DESCRIPTION</span></span>
<span data-ttu-id="734d0-106">Das **Cmdlet "Set-AzStorageContainerStoredAccessPolicy"** legt eine gespeicherte Zugriffsrichtlinie für einen Azure -Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="734d0-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="734d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="734d0-107">EXAMPLES</span></span>

### <span data-ttu-id="734d0-108">Beispiel 1: Festlegen einer Gespeicherten Zugriffsrichtlinie in einem Speichercontainer mit der vollen Berechtigung</span><span class="sxs-lookup"><span data-stu-id="734d0-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="734d0-109">Mit diesem Befehl wird eine Zugriffsrichtlinie namens "Policy06" für den Speichercontainer namens "MyContainer" definiert.</span><span class="sxs-lookup"><span data-stu-id="734d0-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="734d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="734d0-110">PARAMETERS</span></span>

### <span data-ttu-id="734d0-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="734d0-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="734d0-112">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="734d0-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="734d0-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="734d0-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="734d0-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="734d0-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="734d0-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="734d0-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="734d0-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="734d0-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="734d0-117">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="734d0-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="734d0-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="734d0-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="734d0-119">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="734d0-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="734d0-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="734d0-120">The default value is 10.</span></span>

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

### <span data-ttu-id="734d0-121">-Container</span><span class="sxs-lookup"><span data-stu-id="734d0-121">-Container</span></span>
<span data-ttu-id="734d0-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="734d0-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="734d0-123">-Context</span><span class="sxs-lookup"><span data-stu-id="734d0-123">-Context</span></span>
<span data-ttu-id="734d0-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="734d0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="734d0-125">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734d0-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="734d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734d0-126">-DefaultProfile</span></span>
<span data-ttu-id="734d0-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="734d0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734d0-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="734d0-128">-ExpiryTime</span></span>
<span data-ttu-id="734d0-129">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="734d0-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="734d0-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="734d0-130">-NoExpiryTime</span></span>
<span data-ttu-id="734d0-131">Gibt an, dass die Zugriffsrichtlinie kein Ablaufdatum hat.</span><span class="sxs-lookup"><span data-stu-id="734d0-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="734d0-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="734d0-132">-NoStartTime</span></span>
<span data-ttu-id="734d0-133">Legt fest, dass die Startzeit $Null.</span><span class="sxs-lookup"><span data-stu-id="734d0-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="734d0-134">-Permission</span><span class="sxs-lookup"><span data-stu-id="734d0-134">-Permission</span></span>
<span data-ttu-id="734d0-135">Gibt Berechtigungen in der Richtlinie für den gespeicherten Zugriff für den Zugriff auf den Speichercontainer an.</span><span class="sxs-lookup"><span data-stu-id="734d0-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="734d0-136">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="734d0-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="734d0-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="734d0-137">-Policy</span></span>
<span data-ttu-id="734d0-138">Gibt den Namen der gespeicherten Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="734d0-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="734d0-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="734d0-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="734d0-140">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="734d0-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="734d0-141">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="734d0-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="734d0-142">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="734d0-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="734d0-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="734d0-143">-StartTime</span></span>
<span data-ttu-id="734d0-144">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="734d0-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="734d0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="734d0-145">-Confirm</span></span>
<span data-ttu-id="734d0-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="734d0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734d0-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="734d0-147">-WhatIf</span></span>
<span data-ttu-id="734d0-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="734d0-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="734d0-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="734d0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734d0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734d0-150">CommonParameters</span></span>
<span data-ttu-id="734d0-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734d0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734d0-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="734d0-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734d0-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="734d0-153">INPUTS</span></span>

### <span data-ttu-id="734d0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="734d0-154">System.String</span></span>

### <span data-ttu-id="734d0-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="734d0-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="734d0-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="734d0-156">OUTPUTS</span></span>

### <span data-ttu-id="734d0-157">System.String</span><span class="sxs-lookup"><span data-stu-id="734d0-157">System.String</span></span>

## <span data-ttu-id="734d0-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="734d0-158">NOTES</span></span>

## <span data-ttu-id="734d0-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="734d0-159">RELATED LINKS</span></span>

[<span data-ttu-id="734d0-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="734d0-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="734d0-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="734d0-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="734d0-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="734d0-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="734d0-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="734d0-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
