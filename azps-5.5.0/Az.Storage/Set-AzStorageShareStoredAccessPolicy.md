---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 5159e09d4e56b45e9b7ce61bae3e9d8e5fd115c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150385"
---
# <span data-ttu-id="0092b-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0092b-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="0092b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0092b-102">SYNOPSIS</span></span>
<span data-ttu-id="0092b-103">Aktualisiert eine Richtlinie für den gespeicherten Zugriff auf einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="0092b-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="0092b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0092b-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0092b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0092b-105">DESCRIPTION</span></span>
<span data-ttu-id="0092b-106">Das **Cmdlet "Set-AzStorageShareStoredAccessPolicy"** aktualisiert die gespeicherte Zugriffsrichtlinie auf einer Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="0092b-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="0092b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0092b-107">EXAMPLES</span></span>

### <span data-ttu-id="0092b-108">Beispiel 1: Aktualisieren einer Gespeicherten Zugriffsrichtlinie in der Speicherfreigabe</span><span class="sxs-lookup"><span data-stu-id="0092b-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="0092b-109">Mit diesem Befehl wird eine gespeicherte Zugriffsrichtlinie aktualisiert, die über die vollständigen Berechtigungen für eine Freigabe verfügt.</span><span class="sxs-lookup"><span data-stu-id="0092b-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="0092b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0092b-110">PARAMETERS</span></span>

### <span data-ttu-id="0092b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0092b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0092b-112">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="0092b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0092b-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0092b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0092b-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0092b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0092b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0092b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0092b-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="0092b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0092b-117">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="0092b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0092b-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="0092b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0092b-119">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="0092b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0092b-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="0092b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0092b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0092b-121">-Context</span></span>
<span data-ttu-id="0092b-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="0092b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0092b-123">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="0092b-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0092b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0092b-124">-DefaultProfile</span></span>
<span data-ttu-id="0092b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0092b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0092b-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0092b-126">-ExpiryTime</span></span>
<span data-ttu-id="0092b-127">Gibt den Zeitpunkt an, zu dem die Richtlinie für den gespeicherten Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="0092b-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="0092b-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0092b-128">-NoExpiryTime</span></span>
<span data-ttu-id="0092b-129">Gibt an, dass mit diesem Cmdlet die **Eigenschaft "ExpiryTime"** in der gespeicherten Zugriffsrichtlinie entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0092b-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="0092b-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="0092b-130">-NoStartTime</span></span>
<span data-ttu-id="0092b-131">Gibt an, dass mit diesem Cmdlet die **"StartTime"-Eigenschaft** in der gespeicherten Zugriffsrichtlinie entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0092b-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="0092b-132">-Permission</span><span class="sxs-lookup"><span data-stu-id="0092b-132">-Permission</span></span>
<span data-ttu-id="0092b-133">Gibt Berechtigungen in der Richtlinie für den gespeicherten Zugriff für den Zugriff auf die Freigabe oder die Dateien unter der Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="0092b-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="0092b-134">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="0092b-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0092b-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="0092b-135">-Policy</span></span>
<span data-ttu-id="0092b-136">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="0092b-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="0092b-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0092b-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0092b-138">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="0092b-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0092b-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0092b-139">-ShareName</span></span>
<span data-ttu-id="0092b-140">Gibt den Namen der Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="0092b-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="0092b-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0092b-141">-StartTime</span></span>
<span data-ttu-id="0092b-142">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="0092b-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="0092b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0092b-143">-Confirm</span></span>
<span data-ttu-id="0092b-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0092b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0092b-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0092b-145">-WhatIf</span></span>
<span data-ttu-id="0092b-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0092b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0092b-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0092b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0092b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0092b-148">CommonParameters</span></span>
<span data-ttu-id="0092b-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0092b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0092b-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0092b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0092b-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0092b-151">INPUTS</span></span>

### <span data-ttu-id="0092b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="0092b-152">System.String</span></span>

### <span data-ttu-id="0092b-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0092b-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0092b-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0092b-154">OUTPUTS</span></span>

### <span data-ttu-id="0092b-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0092b-155">System.String</span></span>

## <span data-ttu-id="0092b-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0092b-156">NOTES</span></span>

## <span data-ttu-id="0092b-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0092b-157">RELATED LINKS</span></span>

[<span data-ttu-id="0092b-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0092b-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0092b-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0092b-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0092b-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0092b-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="0092b-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0092b-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
