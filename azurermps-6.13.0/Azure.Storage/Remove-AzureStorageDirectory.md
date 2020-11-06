---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
ms.openlocfilehash: 6df60027ff2c25a8f2c1c948d04213cfc6d6158e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478086"
---
# <span data-ttu-id="7e432-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7e432-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="7e432-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e432-102">SYNOPSIS</span></span>
<span data-ttu-id="7e432-103">Löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7e432-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e432-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e432-104">SYNTAX</span></span>

### <span data-ttu-id="7e432-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e432-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e432-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="7e432-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e432-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="7e432-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e432-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e432-108">DESCRIPTION</span></span>
<span data-ttu-id="7e432-109">Das Cmdlet **Remove-AzureStorageDirectory** löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7e432-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="7e432-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e432-110">EXAMPLES</span></span>

### <span data-ttu-id="7e432-111">Beispiel 1: Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="7e432-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="7e432-112">Dieser Befehl löscht den Ordner "ContosoWorkingFolder" aus der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="7e432-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="7e432-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e432-113">PARAMETERS</span></span>

### <span data-ttu-id="7e432-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e432-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7e432-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7e432-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7e432-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="7e432-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7e432-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7e432-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7e432-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7e432-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7e432-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="7e432-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7e432-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="7e432-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7e432-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="7e432-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7e432-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="7e432-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7e432-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="7e432-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7e432-124">-Context</span><span class="sxs-lookup"><span data-stu-id="7e432-124">-Context</span></span>
<span data-ttu-id="7e432-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7e432-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7e432-126">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="7e432-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="7e432-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e432-127">-DefaultProfile</span></span>
<span data-ttu-id="7e432-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e432-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e432-129">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="7e432-129">-Directory</span></span>
<span data-ttu-id="7e432-130">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7e432-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7e432-131">Mit diesem Cmdlet wird der Ordner entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7e432-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="7e432-132">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e432-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7e432-133">Sie können auch das Cmdlet **Get-AzureStorageFile** verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e432-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e432-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e432-134">-PassThru</span></span>
<span data-ttu-id="7e432-135">Gibt an, dass, wenn dieses Cmdlet erfolgreich ist, der Wert $true zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e432-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="7e432-136">Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines unangemessenen Werts für den _path_ -Parameter nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7e432-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="7e432-137">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7e432-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7e432-138">-Path</span><span class="sxs-lookup"><span data-stu-id="7e432-138">-Path</span></span>
<span data-ttu-id="7e432-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="7e432-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="7e432-140">Wenn der Ordner, den dieser Parameter angibt, leer ist, löscht dieses Cmdlet diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e432-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="7e432-141">Wenn der Ordner nicht leer ist, nimmt das Cmdlet keine Änderungen vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7e432-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e432-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7e432-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7e432-143">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="7e432-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7e432-144">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="7e432-144">-Share</span></span>
<span data-ttu-id="7e432-145">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7e432-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7e432-146">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7e432-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="7e432-147">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7e432-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="7e432-148">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="7e432-148">This object contains the storage context.</span></span>
<span data-ttu-id="7e432-149">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="7e432-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="7e432-150">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="7e432-150">-ShareName</span></span>
<span data-ttu-id="7e432-151">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="7e432-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="7e432-152">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7e432-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e432-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e432-153">-Confirm</span></span>
<span data-ttu-id="7e432-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e432-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e432-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e432-155">-WhatIf</span></span>
<span data-ttu-id="7e432-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e432-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e432-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e432-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e432-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e432-158">CommonParameters</span></span>
<span data-ttu-id="7e432-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e432-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e432-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e432-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e432-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e432-161">INPUTS</span></span>

### <span data-ttu-id="7e432-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7e432-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="7e432-163">Parameter: freigeben (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e432-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="7e432-164">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7e432-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="7e432-165">Parameter: Verzeichnis (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e432-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="7e432-166">System. String</span><span class="sxs-lookup"><span data-stu-id="7e432-166">System.String</span></span>

### <span data-ttu-id="7e432-167">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e432-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7e432-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e432-168">OUTPUTS</span></span>

### <span data-ttu-id="7e432-169">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7e432-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="7e432-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e432-170">NOTES</span></span>

## <span data-ttu-id="7e432-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e432-171">RELATED LINKS</span></span>

[<span data-ttu-id="7e432-172">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="7e432-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="7e432-173">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7e432-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7e432-174">Neu – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="7e432-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
