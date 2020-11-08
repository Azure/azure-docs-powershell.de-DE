---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176006"
---
# <span data-ttu-id="4fefb-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fefb-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="4fefb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fefb-102">SYNOPSIS</span></span>
<span data-ttu-id="4fefb-103">Löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="4fefb-103">Deletes a file share.</span></span>

## <span data-ttu-id="4fefb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fefb-104">SYNTAX</span></span>

### <span data-ttu-id="4fefb-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="4fefb-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fefb-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="4fefb-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fefb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fefb-107">DESCRIPTION</span></span>
<span data-ttu-id="4fefb-108">Das Cmdlet **Remove-AzStorageShare** löscht eine Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="4fefb-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="4fefb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fefb-109">EXAMPLES</span></span>

### <span data-ttu-id="4fefb-110">Beispiel 1: Entfernen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="4fefb-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4fefb-111">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="4fefb-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="4fefb-112">Beispiel 2: Entfernen einer Dateifreigabe und aller zugehörigen Snapshots</span><span class="sxs-lookup"><span data-stu-id="4fefb-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="4fefb-113">Dieser Befehl entfernt die Dateifreigabe mit dem Namen ContosoShare06 und alle zugehörigen Snapshots.</span><span class="sxs-lookup"><span data-stu-id="4fefb-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="4fefb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fefb-114">PARAMETERS</span></span>

### <span data-ttu-id="4fefb-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fefb-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4fefb-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4fefb-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="4fefb-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4fefb-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4fefb-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4fefb-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4fefb-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4fefb-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4fefb-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4fefb-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4fefb-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4fefb-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4fefb-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4fefb-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4fefb-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4fefb-124">The default value is 10.</span></span>

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

### <span data-ttu-id="4fefb-125">-Context</span><span class="sxs-lookup"><span data-stu-id="4fefb-125">-Context</span></span>
<span data-ttu-id="4fefb-126">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fefb-127">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="4fefb-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fefb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fefb-128">-DefaultProfile</span></span>
<span data-ttu-id="4fefb-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fefb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fefb-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4fefb-130">-Force</span></span>
<span data-ttu-id="4fefb-131">Erzwingen Sie die Freigabe für alle Snapshots und alle Inhalte.</span><span class="sxs-lookup"><span data-stu-id="4fefb-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="4fefb-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="4fefb-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="4fefb-133">Entfernen der Dateifreigabe für alle Snapshots</span><span class="sxs-lookup"><span data-stu-id="4fefb-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="4fefb-134">-Name</span><span class="sxs-lookup"><span data-stu-id="4fefb-134">-Name</span></span>
<span data-ttu-id="4fefb-135">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="4fefb-136">Dieses Cmdlet löscht die Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4fefb-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="4fefb-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fefb-137">-PassThru</span></span>
<span data-ttu-id="4fefb-138">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="4fefb-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4fefb-139">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4fefb-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4fefb-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fefb-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4fefb-141">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4fefb-142">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="4fefb-142">-Share</span></span>
<span data-ttu-id="4fefb-143">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="4fefb-144">Dieses Cmdlet entfernt das Objekt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4fefb-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="4fefb-145">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4fefb-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="4fefb-146">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="4fefb-146">This object contains the storage context.</span></span>
<span data-ttu-id="4fefb-147">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="4fefb-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fefb-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4fefb-148">-Confirm</span></span>
<span data-ttu-id="4fefb-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4fefb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fefb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fefb-150">-WhatIf</span></span>
<span data-ttu-id="4fefb-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fefb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fefb-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fefb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fefb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fefb-153">CommonParameters</span></span>
<span data-ttu-id="4fefb-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fefb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fefb-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fefb-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fefb-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fefb-156">INPUTS</span></span>

### <span data-ttu-id="4fefb-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4fefb-157">System.String</span></span>

### <span data-ttu-id="4fefb-158">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4fefb-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4fefb-159">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fefb-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4fefb-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fefb-160">OUTPUTS</span></span>

### <span data-ttu-id="4fefb-161">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="4fefb-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="4fefb-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fefb-162">NOTES</span></span>

## <span data-ttu-id="4fefb-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fefb-163">RELATED LINKS</span></span>

[<span data-ttu-id="4fefb-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fefb-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4fefb-165">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fefb-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4fefb-166">Neu – AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4fefb-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
