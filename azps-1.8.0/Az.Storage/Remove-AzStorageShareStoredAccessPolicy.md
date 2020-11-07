---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: db37ead04710a422983f00b461a69b1cb12f328f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658767"
---
# <span data-ttu-id="96f49-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96f49-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="96f49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96f49-102">SYNOPSIS</span></span>
<span data-ttu-id="96f49-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einer Speicherfreigabe.</span><span class="sxs-lookup"><span data-stu-id="96f49-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="96f49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96f49-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96f49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96f49-105">DESCRIPTION</span></span>
<span data-ttu-id="96f49-106">Das Cmdlet " **Remove-AzStorageShareStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einer Azure Storage-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="96f49-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="96f49-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96f49-107">EXAMPLES</span></span>

### <span data-ttu-id="96f49-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einer Azure Storage-Freigabe</span><span class="sxs-lookup"><span data-stu-id="96f49-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="96f49-109">Dieser Befehl entfernt eine gespeicherte Zugriffsrichtlinie mit dem Namen GeneralPolicy aus ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="96f49-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="96f49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96f49-110">PARAMETERS</span></span>

### <span data-ttu-id="96f49-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96f49-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="96f49-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="96f49-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="96f49-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="96f49-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="96f49-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="96f49-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="96f49-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="96f49-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="96f49-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="96f49-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="96f49-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="96f49-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="96f49-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="96f49-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="96f49-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="96f49-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="96f49-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="96f49-120">The default value is 10.</span></span>

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

### <span data-ttu-id="96f49-121">-Context</span><span class="sxs-lookup"><span data-stu-id="96f49-121">-Context</span></span>
<span data-ttu-id="96f49-122">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="96f49-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96f49-123">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="96f49-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="96f49-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f49-124">-DefaultProfile</span></span>
<span data-ttu-id="96f49-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96f49-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f49-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96f49-126">-PassThru</span></span>
<span data-ttu-id="96f49-127">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="96f49-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="96f49-128">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="96f49-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="96f49-129">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="96f49-129">-Policy</span></span>
<span data-ttu-id="96f49-130">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="96f49-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96f49-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="96f49-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="96f49-132">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="96f49-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="96f49-133">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="96f49-133">-ShareName</span></span>
<span data-ttu-id="96f49-134">Gibt den Speicherfreigabe Namen an, für den dieses Cmdlet eine Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="96f49-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="96f49-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96f49-135">-Confirm</span></span>
<span data-ttu-id="96f49-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96f49-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f49-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f49-137">-WhatIf</span></span>
<span data-ttu-id="96f49-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96f49-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f49-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96f49-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f49-140">CommonParameters</span></span>
<span data-ttu-id="96f49-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f49-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f49-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f49-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96f49-143">INPUTS</span></span>

### <span data-ttu-id="96f49-144">System. String</span><span class="sxs-lookup"><span data-stu-id="96f49-144">System.String</span></span>

### <span data-ttu-id="96f49-145">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96f49-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96f49-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96f49-146">OUTPUTS</span></span>

### <span data-ttu-id="96f49-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96f49-147">System.Boolean</span></span>

## <span data-ttu-id="96f49-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="96f49-148">NOTES</span></span>

## <span data-ttu-id="96f49-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96f49-149">RELATED LINKS</span></span>

[<span data-ttu-id="96f49-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96f49-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="96f49-151">Neu – AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96f49-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="96f49-152">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96f49-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="96f49-153">Satz-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96f49-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
