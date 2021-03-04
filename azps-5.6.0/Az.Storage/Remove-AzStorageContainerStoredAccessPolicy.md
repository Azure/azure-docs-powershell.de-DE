---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 4d2828351c4007e57fd8c7534e88aa3be5543199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938443"
---
# <span data-ttu-id="63a59-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="63a59-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="63a59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a59-102">SYNOPSIS</span></span>
<span data-ttu-id="63a59-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="63a59-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="63a59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63a59-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63a59-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63a59-105">DESCRIPTION</span></span>
<span data-ttu-id="63a59-106">Das **Cmdlet Remove-AzStorageContainerStoredAccessPolicy** entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="63a59-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="63a59-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="63a59-107">EXAMPLES</span></span>

### <span data-ttu-id="63a59-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="63a59-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="63a59-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy03" aus dem gespeicherten Container "MyContainer" entfernt.</span><span class="sxs-lookup"><span data-stu-id="63a59-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="63a59-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="63a59-110">PARAMETERS</span></span>

### <span data-ttu-id="63a59-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63a59-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="63a59-112">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="63a59-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="63a59-113">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63a59-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="63a59-114">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="63a59-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="63a59-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="63a59-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="63a59-116">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="63a59-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="63a59-117">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="63a59-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="63a59-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="63a59-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="63a59-119">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="63a59-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="63a59-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="63a59-120">The default value is 10.</span></span>

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

### <span data-ttu-id="63a59-121">-Container</span><span class="sxs-lookup"><span data-stu-id="63a59-121">-Container</span></span>
<span data-ttu-id="63a59-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="63a59-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="63a59-123">-Context</span><span class="sxs-lookup"><span data-stu-id="63a59-123">-Context</span></span>
<span data-ttu-id="63a59-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="63a59-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="63a59-125">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63a59-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="63a59-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a59-126">-DefaultProfile</span></span>
<span data-ttu-id="63a59-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63a59-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a59-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63a59-128">-PassThru</span></span>
<span data-ttu-id="63a59-129">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="63a59-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="63a59-130">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="63a59-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="63a59-131">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="63a59-131">-Policy</span></span>
<span data-ttu-id="63a59-132">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="63a59-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="63a59-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63a59-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="63a59-134">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="63a59-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="63a59-135">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63a59-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="63a59-136">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="63a59-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="63a59-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63a59-137">-Confirm</span></span>
<span data-ttu-id="63a59-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63a59-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63a59-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a59-139">-WhatIf</span></span>
<span data-ttu-id="63a59-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63a59-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63a59-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63a59-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63a59-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a59-142">CommonParameters</span></span>
<span data-ttu-id="63a59-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a59-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a59-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a59-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a59-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="63a59-145">INPUTS</span></span>

### <span data-ttu-id="63a59-146">System.String</span><span class="sxs-lookup"><span data-stu-id="63a59-146">System.String</span></span>

### <span data-ttu-id="63a59-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="63a59-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="63a59-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="63a59-148">OUTPUTS</span></span>

### <span data-ttu-id="63a59-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="63a59-149">System.Boolean</span></span>

## <span data-ttu-id="63a59-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="63a59-150">NOTES</span></span>

## <span data-ttu-id="63a59-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="63a59-151">RELATED LINKS</span></span>

[<span data-ttu-id="63a59-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="63a59-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="63a59-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="63a59-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="63a59-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="63a59-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="63a59-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="63a59-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
