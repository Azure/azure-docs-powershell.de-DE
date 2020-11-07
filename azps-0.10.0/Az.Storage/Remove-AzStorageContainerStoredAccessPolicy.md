---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 113e76a7bb9e1d6a88536980556ebe3222488b07
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842935"
---
# <span data-ttu-id="f67ee-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f67ee-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="f67ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f67ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f67ee-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="f67ee-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="f67ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f67ee-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f67ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f67ee-105">DESCRIPTION</span></span>
<span data-ttu-id="f67ee-106">Das Cmdlet " **Remove-AzStorageContainerStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="f67ee-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="f67ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f67ee-107">EXAMPLES</span></span>

### <span data-ttu-id="f67ee-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="f67ee-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="f67ee-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy03 aus dem gespeicherten Container mit dem Namen MyContainer.</span><span class="sxs-lookup"><span data-stu-id="f67ee-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="f67ee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f67ee-110">PARAMETERS</span></span>

### <span data-ttu-id="f67ee-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f67ee-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f67ee-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f67ee-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f67ee-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="f67ee-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f67ee-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ee-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f67ee-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f67ee-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f67ee-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="f67ee-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f67ee-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="f67ee-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f67ee-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f67ee-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f67ee-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="f67ee-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f67ee-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f67ee-120">The default value is 10.</span></span>

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

### <span data-ttu-id="f67ee-121">-Container</span><span class="sxs-lookup"><span data-stu-id="f67ee-121">-Container</span></span>
<span data-ttu-id="f67ee-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="f67ee-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="f67ee-123">-Context</span><span class="sxs-lookup"><span data-stu-id="f67ee-123">-Context</span></span>
<span data-ttu-id="f67ee-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f67ee-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f67ee-125">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f67ee-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f67ee-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67ee-126">-DefaultProfile</span></span>
<span data-ttu-id="f67ee-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f67ee-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f67ee-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f67ee-128">-PassThru</span></span>
<span data-ttu-id="f67ee-129">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="f67ee-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f67ee-130">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ee-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f67ee-131">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f67ee-131">-Policy</span></span>
<span data-ttu-id="f67ee-132">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ee-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f67ee-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f67ee-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f67ee-134">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f67ee-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f67ee-135">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="f67ee-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f67ee-136">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f67ee-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f67ee-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f67ee-137">-Confirm</span></span>
<span data-ttu-id="f67ee-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f67ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f67ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f67ee-139">-WhatIf</span></span>
<span data-ttu-id="f67ee-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f67ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f67ee-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f67ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f67ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67ee-142">CommonParameters</span></span>
<span data-ttu-id="f67ee-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f67ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67ee-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67ee-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67ee-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f67ee-145">INPUTS</span></span>

### <span data-ttu-id="f67ee-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f67ee-146">System.String</span></span>

### <span data-ttu-id="f67ee-147">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f67ee-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f67ee-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f67ee-148">OUTPUTS</span></span>

### <span data-ttu-id="f67ee-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f67ee-149">System.Boolean</span></span>

## <span data-ttu-id="f67ee-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="f67ee-150">NOTES</span></span>

## <span data-ttu-id="f67ee-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f67ee-151">RELATED LINKS</span></span>

[<span data-ttu-id="f67ee-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f67ee-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f67ee-153">Neu – AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f67ee-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="f67ee-154">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f67ee-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f67ee-155">Satz-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f67ee-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
