---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: cc57638e1620e8c9177f3635074f6964ef38afb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658774"
---
# <span data-ttu-id="624af-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="624af-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="624af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="624af-102">SYNOPSIS</span></span>
<span data-ttu-id="624af-103">Löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="624af-103">Deletes a directory.</span></span>

## <span data-ttu-id="624af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="624af-104">SYNTAX</span></span>

### <span data-ttu-id="624af-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="624af-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="624af-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="624af-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="624af-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="624af-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="624af-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="624af-108">DESCRIPTION</span></span>
<span data-ttu-id="624af-109">Das Cmdlet **Remove-AzStorageDirectory** löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="624af-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="624af-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="624af-110">EXAMPLES</span></span>

### <span data-ttu-id="624af-111">Beispiel 1: Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="624af-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="624af-112">Dieser Befehl löscht den Ordner "ContosoWorkingFolder" aus der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="624af-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="624af-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="624af-113">PARAMETERS</span></span>

### <span data-ttu-id="624af-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="624af-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="624af-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="624af-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="624af-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="624af-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="624af-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="624af-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="624af-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="624af-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="624af-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="624af-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="624af-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="624af-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="624af-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="624af-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="624af-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="624af-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="624af-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="624af-123">The default value is 10.</span></span>

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

### <span data-ttu-id="624af-124">-Context</span><span class="sxs-lookup"><span data-stu-id="624af-124">-Context</span></span>
<span data-ttu-id="624af-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="624af-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="624af-126">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="624af-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="624af-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624af-127">-DefaultProfile</span></span>
<span data-ttu-id="624af-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="624af-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="624af-129">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="624af-129">-Directory</span></span>
<span data-ttu-id="624af-130">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="624af-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="624af-131">Mit diesem Cmdlet wird der Ordner entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="624af-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="624af-132">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="624af-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="624af-133">Sie können auch das Cmdlet **Get-AzStorageFile** verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="624af-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="624af-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="624af-134">-PassThru</span></span>
<span data-ttu-id="624af-135">Gibt an, dass, wenn dieses Cmdlet erfolgreich ist, der Wert $true zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="624af-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="624af-136">Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines unangemessenen Werts für den _path_ -Parameter nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="624af-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="624af-137">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="624af-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="624af-138">-Path</span><span class="sxs-lookup"><span data-stu-id="624af-138">-Path</span></span>
<span data-ttu-id="624af-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="624af-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="624af-140">Wenn der Ordner, den dieser Parameter angibt, leer ist, löscht dieses Cmdlet diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="624af-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="624af-141">Wenn der Ordner nicht leer ist, nimmt das Cmdlet keine Änderungen vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="624af-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="624af-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="624af-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="624af-143">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="624af-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="624af-144">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="624af-144">-Share</span></span>
<span data-ttu-id="624af-145">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="624af-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="624af-146">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="624af-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="624af-147">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="624af-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="624af-148">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="624af-148">This object contains the storage context.</span></span>
<span data-ttu-id="624af-149">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="624af-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="624af-150">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="624af-150">-ShareName</span></span>
<span data-ttu-id="624af-151">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="624af-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="624af-152">Mit diesem Cmdlet wird ein Ordner unter der Dateifreigabe entfernt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="624af-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="624af-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="624af-153">-Confirm</span></span>
<span data-ttu-id="624af-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="624af-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="624af-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="624af-155">-WhatIf</span></span>
<span data-ttu-id="624af-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="624af-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="624af-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="624af-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="624af-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624af-158">CommonParameters</span></span>
<span data-ttu-id="624af-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="624af-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624af-160">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="624af-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624af-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="624af-161">INPUTS</span></span>

### <span data-ttu-id="624af-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="624af-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="624af-163">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="624af-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="624af-164">System. String</span><span class="sxs-lookup"><span data-stu-id="624af-164">System.String</span></span>

### <span data-ttu-id="624af-165">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="624af-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="624af-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="624af-166">OUTPUTS</span></span>

### <span data-ttu-id="624af-167">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="624af-167">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="624af-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="624af-168">NOTES</span></span>

## <span data-ttu-id="624af-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="624af-169">RELATED LINKS</span></span>

[<span data-ttu-id="624af-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="624af-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="624af-171">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="624af-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="624af-172">Neu – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="624af-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
