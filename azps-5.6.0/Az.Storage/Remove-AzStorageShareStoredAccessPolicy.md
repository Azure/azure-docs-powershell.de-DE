---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 9a6702b59bbe2e0305966cd9a1323edc120e86c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923235"
---
# <span data-ttu-id="9b555-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b555-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="9b555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b555-102">SYNOPSIS</span></span>
<span data-ttu-id="9b555-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="9b555-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="9b555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b555-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b555-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b555-105">DESCRIPTION</span></span>
<span data-ttu-id="9b555-106">Das **Cmdlet Remove-AzStorageShareStoredAccessPolicy** entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="9b555-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="9b555-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b555-107">EXAMPLES</span></span>

### <span data-ttu-id="9b555-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Azure Storage-Freigabe</span><span class="sxs-lookup"><span data-stu-id="9b555-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="9b555-109">Mit diesem Befehl wird eine gespeicherte Zugriffsrichtlinie namens "GeneralPolicy" aus ContosoShare entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b555-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="9b555-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b555-110">PARAMETERS</span></span>

### <span data-ttu-id="9b555-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b555-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9b555-112">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="9b555-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9b555-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b555-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9b555-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9b555-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9b555-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9b555-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9b555-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="9b555-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9b555-117">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="9b555-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9b555-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9b555-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9b555-119">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="9b555-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9b555-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9b555-120">The default value is 10.</span></span>

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

### <span data-ttu-id="9b555-121">-Context</span><span class="sxs-lookup"><span data-stu-id="9b555-121">-Context</span></span>
<span data-ttu-id="9b555-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9b555-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9b555-123">Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="9b555-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9b555-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b555-124">-DefaultProfile</span></span>
<span data-ttu-id="9b555-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b555-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b555-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b555-126">-PassThru</span></span>
<span data-ttu-id="9b555-127">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="9b555-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="9b555-128">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9b555-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9b555-129">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9b555-129">-Policy</span></span>
<span data-ttu-id="9b555-130">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9b555-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b555-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b555-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9b555-132">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9b555-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9b555-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9b555-133">-ShareName</span></span>
<span data-ttu-id="9b555-134">Gibt den Namen der Speicherfreigabe an, für den dieses Cmdlet eine Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b555-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b555-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b555-135">-Confirm</span></span>
<span data-ttu-id="9b555-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b555-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b555-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b555-137">-WhatIf</span></span>
<span data-ttu-id="9b555-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b555-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b555-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b555-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b555-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b555-140">CommonParameters</span></span>
<span data-ttu-id="9b555-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b555-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b555-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b555-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b555-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b555-143">INPUTS</span></span>

### <span data-ttu-id="9b555-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9b555-144">System.String</span></span>

### <span data-ttu-id="9b555-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b555-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9b555-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b555-146">OUTPUTS</span></span>

### <span data-ttu-id="9b555-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b555-147">System.Boolean</span></span>

## <span data-ttu-id="9b555-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9b555-148">NOTES</span></span>

## <span data-ttu-id="9b555-149">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9b555-149">RELATED LINKS</span></span>

[<span data-ttu-id="9b555-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b555-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="9b555-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b555-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="9b555-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b555-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9b555-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9b555-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
