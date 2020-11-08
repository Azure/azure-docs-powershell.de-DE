---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176537"
---
# <span data-ttu-id="e22b1-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e22b1-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e22b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e22b1-102">SYNOPSIS</span></span>
<span data-ttu-id="e22b1-103">Entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="e22b1-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e22b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e22b1-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e22b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e22b1-105">DESCRIPTION</span></span>
<span data-ttu-id="e22b1-106">Das Cmdlet " **Remove-AzStorageContainerStoredAccessPolicy** " entfernt eine gespeicherte Zugriffsrichtlinie aus einem Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="e22b1-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e22b1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e22b1-107">EXAMPLES</span></span>

### <span data-ttu-id="e22b1-108">Beispiel 1: Entfernen einer gespeicherten Zugriffsrichtlinie aus einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="e22b1-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="e22b1-109">Dieser Befehl entfernt eine Access-Richtlinie mit dem Namen Policy03 aus dem gespeicherten Container mit dem Namen MyContainer.</span><span class="sxs-lookup"><span data-stu-id="e22b1-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="e22b1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e22b1-110">PARAMETERS</span></span>

### <span data-ttu-id="e22b1-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e22b1-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e22b1-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e22b1-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e22b1-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="e22b1-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e22b1-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e22b1-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e22b1-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e22b1-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e22b1-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="e22b1-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e22b1-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="e22b1-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e22b1-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e22b1-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e22b1-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e22b1-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e22b1-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="e22b1-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e22b1-121">-Container</span><span class="sxs-lookup"><span data-stu-id="e22b1-121">-Container</span></span>
<span data-ttu-id="e22b1-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="e22b1-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="e22b1-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e22b1-123">-Context</span></span>
<span data-ttu-id="e22b1-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e22b1-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e22b1-125">Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e22b1-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e22b1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22b1-126">-DefaultProfile</span></span>
<span data-ttu-id="e22b1-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e22b1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22b1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e22b1-128">-PassThru</span></span>
<span data-ttu-id="e22b1-129">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="e22b1-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e22b1-130">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e22b1-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e22b1-131">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e22b1-131">-Policy</span></span>
<span data-ttu-id="e22b1-132">Gibt den Namen der gespeicherten Zugriffsrichtlinie an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e22b1-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e22b1-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e22b1-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e22b1-134">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e22b1-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e22b1-135">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="e22b1-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e22b1-136">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e22b1-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e22b1-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e22b1-137">-Confirm</span></span>
<span data-ttu-id="e22b1-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e22b1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22b1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22b1-139">-WhatIf</span></span>
<span data-ttu-id="e22b1-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e22b1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22b1-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e22b1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22b1-142">CommonParameters</span></span>
<span data-ttu-id="e22b1-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22b1-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22b1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22b1-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e22b1-145">INPUTS</span></span>

### <span data-ttu-id="e22b1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e22b1-146">System.String</span></span>

### <span data-ttu-id="e22b1-147">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e22b1-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e22b1-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e22b1-148">OUTPUTS</span></span>

### <span data-ttu-id="e22b1-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e22b1-149">System.Boolean</span></span>

## <span data-ttu-id="e22b1-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e22b1-150">NOTES</span></span>

## <span data-ttu-id="e22b1-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e22b1-151">RELATED LINKS</span></span>

[<span data-ttu-id="e22b1-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e22b1-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e22b1-153">Neu – AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e22b1-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e22b1-154">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e22b1-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e22b1-155">Satz-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e22b1-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
