---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 0b8adb43c8ae83afe0d8053d8367c8bf8152b233
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826356"
---
# <span data-ttu-id="642b2-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="642b2-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="642b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="642b2-102">SYNOPSIS</span></span>
<span data-ttu-id="642b2-103">Löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="642b2-103">Deletes a file.</span></span>

## <span data-ttu-id="642b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="642b2-104">SYNTAX</span></span>

### <span data-ttu-id="642b2-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="642b2-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642b2-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="642b2-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642b2-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="642b2-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="642b2-108">Datei</span><span class="sxs-lookup"><span data-stu-id="642b2-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642b2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="642b2-109">DESCRIPTION</span></span>
<span data-ttu-id="642b2-110">Das Cmdlet **Remove-AzStorageFile** löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="642b2-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="642b2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="642b2-111">EXAMPLES</span></span>

### <span data-ttu-id="642b2-112">Beispiel 1: Löschen einer Datei aus einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="642b2-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="642b2-113">Dieser Befehl löscht die Datei mit dem Namen ContosoFile22 aus der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="642b2-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="642b2-114">Beispiel 2: Abrufen einer Datei aus einer Dateifreigabe mithilfe eines Dateifreigabe Objekts</span><span class="sxs-lookup"><span data-stu-id="642b2-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="642b2-115">Dieser Befehl verwendet das Cmdlet " **Get-AzStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="642b2-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="642b2-116">Der aktuelle Befehl löscht die Datei mit dem Namen ContosoFile22 aus ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="642b2-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="642b2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="642b2-117">PARAMETERS</span></span>

### <span data-ttu-id="642b2-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="642b2-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="642b2-119">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="642b2-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="642b2-120">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="642b2-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="642b2-121">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="642b2-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="642b2-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="642b2-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="642b2-123">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="642b2-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="642b2-124">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="642b2-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="642b2-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="642b2-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="642b2-126">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="642b2-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="642b2-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="642b2-127">The default value is 10.</span></span>

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

### <span data-ttu-id="642b2-128">-Context</span><span class="sxs-lookup"><span data-stu-id="642b2-128">-Context</span></span>
<span data-ttu-id="642b2-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="642b2-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="642b2-130">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="642b2-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="642b2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642b2-131">-DefaultProfile</span></span>
<span data-ttu-id="642b2-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="642b2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642b2-133">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="642b2-133">-Directory</span></span>
<span data-ttu-id="642b2-134">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="642b2-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="642b2-135">Dieses Cmdlet entfernt eine Datei aus dem Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="642b2-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642b2-136">-Datei</span><span class="sxs-lookup"><span data-stu-id="642b2-136">-File</span></span>
<span data-ttu-id="642b2-137">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="642b2-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="642b2-138">Dieses Cmdlet entfernt die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="642b2-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="642b2-139">Verwenden Sie das Get-AzStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="642b2-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642b2-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="642b2-140">-PassThru</span></span>
<span data-ttu-id="642b2-141">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="642b2-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="642b2-142">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="642b2-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="642b2-143">-Path</span><span class="sxs-lookup"><span data-stu-id="642b2-143">-Path</span></span>
<span data-ttu-id="642b2-144">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="642b2-144">Specifies the path of a file.</span></span>
<span data-ttu-id="642b2-145">Dieses Cmdlet löscht die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="642b2-145">This cmdlet deletes the file that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642b2-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="642b2-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="642b2-147">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="642b2-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="642b2-148">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="642b2-148">-Share</span></span>
<span data-ttu-id="642b2-149">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="642b2-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="642b2-150">Mit diesem Cmdlet wird die Datei in der Freigabe, die dieser Parameter angibt, entfernt.</span><span class="sxs-lookup"><span data-stu-id="642b2-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="642b2-151">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="642b2-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="642b2-152">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="642b2-152">This object contains the storage context.</span></span>
<span data-ttu-id="642b2-153">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="642b2-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="642b2-154">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="642b2-154">-ShareName</span></span>
<span data-ttu-id="642b2-155">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="642b2-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="642b2-156">Mit diesem Cmdlet wird die Datei in der Freigabe, die dieser Parameter angibt, entfernt.</span><span class="sxs-lookup"><span data-stu-id="642b2-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="642b2-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="642b2-157">-Confirm</span></span>
<span data-ttu-id="642b2-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="642b2-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642b2-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642b2-159">-WhatIf</span></span>
<span data-ttu-id="642b2-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="642b2-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642b2-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="642b2-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642b2-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642b2-162">CommonParameters</span></span>
<span data-ttu-id="642b2-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642b2-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642b2-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="642b2-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642b2-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="642b2-165">INPUTS</span></span>

### <span data-ttu-id="642b2-166">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="642b2-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="642b2-167">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="642b2-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="642b2-168">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="642b2-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="642b2-169">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="642b2-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="642b2-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="642b2-170">OUTPUTS</span></span>

### <span data-ttu-id="642b2-171">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="642b2-171">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="642b2-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="642b2-172">NOTES</span></span>

## <span data-ttu-id="642b2-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="642b2-173">RELATED LINKS</span></span>

[<span data-ttu-id="642b2-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="642b2-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="642b2-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="642b2-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="642b2-176">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="642b2-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
