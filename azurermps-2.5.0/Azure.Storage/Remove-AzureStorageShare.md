---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 07ab4071d89e1ba97d4c824bd98012fae70a79de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850492"
---
# <span data-ttu-id="922ca-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="922ca-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="922ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="922ca-102">SYNOPSIS</span></span>
<span data-ttu-id="922ca-103">Löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="922ca-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="922ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="922ca-104">SYNTAX</span></span>

### <span data-ttu-id="922ca-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="922ca-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="922ca-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="922ca-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="922ca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="922ca-107">DESCRIPTION</span></span>
<span data-ttu-id="922ca-108">Das Cmdlet **Remove-AzureStorageShare** löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="922ca-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="922ca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="922ca-109">EXAMPLES</span></span>

### <span data-ttu-id="922ca-110">Beispiel 1: Entfernen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="922ca-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="922ca-111">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="922ca-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="922ca-112">Beispiel 2: Entfernen einer Dateifreigabe und aller zugehörigen Snapshots</span><span class="sxs-lookup"><span data-stu-id="922ca-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="922ca-113">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06 und alle zugehörigen Snapshots.</span><span class="sxs-lookup"><span data-stu-id="922ca-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="922ca-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="922ca-114">PARAMETERS</span></span>

### <span data-ttu-id="922ca-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="922ca-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="922ca-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="922ca-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="922ca-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="922ca-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="922ca-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="922ca-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="922ca-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="922ca-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="922ca-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="922ca-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="922ca-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="922ca-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="922ca-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="922ca-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="922ca-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="922ca-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="922ca-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="922ca-124">The default value is 10.</span></span>

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

### <span data-ttu-id="922ca-125">-Context</span><span class="sxs-lookup"><span data-stu-id="922ca-125">-Context</span></span>
<span data-ttu-id="922ca-126">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="922ca-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="922ca-127">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="922ca-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="922ca-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="922ca-128">-DefaultProfile</span></span>
<span data-ttu-id="922ca-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="922ca-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="922ca-130">-Force</span><span class="sxs-lookup"><span data-stu-id="922ca-130">-Force</span></span>
<span data-ttu-id="922ca-131">Erzwingen Sie die Freigabe für alle Snapshots und alle Inhalte.</span><span class="sxs-lookup"><span data-stu-id="922ca-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="922ca-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="922ca-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="922ca-133">Entfernen der Dateifreigabe für alle Snapshots</span><span class="sxs-lookup"><span data-stu-id="922ca-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="922ca-134">-Name</span><span class="sxs-lookup"><span data-stu-id="922ca-134">-Name</span></span>
<span data-ttu-id="922ca-135">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="922ca-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="922ca-136">Dieses Cmdlet löscht die Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="922ca-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="922ca-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="922ca-137">-PassThru</span></span>
<span data-ttu-id="922ca-138">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="922ca-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="922ca-139">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="922ca-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="922ca-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="922ca-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="922ca-141">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="922ca-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="922ca-142">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="922ca-142">-Share</span></span>
<span data-ttu-id="922ca-143">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="922ca-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="922ca-144">Dieses Cmdlet entfernt das Objekt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="922ca-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="922ca-145">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="922ca-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="922ca-146">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="922ca-146">This object contains the storage context.</span></span>
<span data-ttu-id="922ca-147">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="922ca-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="922ca-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="922ca-148">-Confirm</span></span>
<span data-ttu-id="922ca-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="922ca-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="922ca-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="922ca-150">-WhatIf</span></span>
<span data-ttu-id="922ca-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="922ca-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="922ca-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="922ca-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="922ca-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="922ca-153">CommonParameters</span></span>
<span data-ttu-id="922ca-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="922ca-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="922ca-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="922ca-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="922ca-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="922ca-156">INPUTS</span></span>

### <span data-ttu-id="922ca-157">System. String</span><span class="sxs-lookup"><span data-stu-id="922ca-157">System.String</span></span>

### <span data-ttu-id="922ca-158">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="922ca-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="922ca-159">Parameter: freigeben (ByValue)</span><span class="sxs-lookup"><span data-stu-id="922ca-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="922ca-160">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="922ca-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="922ca-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="922ca-161">OUTPUTS</span></span>

### <span data-ttu-id="922ca-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="922ca-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="922ca-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="922ca-163">NOTES</span></span>

## <span data-ttu-id="922ca-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="922ca-164">RELATED LINKS</span></span>

[<span data-ttu-id="922ca-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="922ca-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="922ca-166">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="922ca-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="922ca-167">Neu – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="922ca-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
