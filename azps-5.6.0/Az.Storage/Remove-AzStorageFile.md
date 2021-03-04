---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: f0a6352c8a9bbe20130924ce62b20c46fc005290
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932187"
---
# <span data-ttu-id="645c8-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="645c8-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="645c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="645c8-102">SYNOPSIS</span></span>
<span data-ttu-id="645c8-103">Löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="645c8-103">Deletes a file.</span></span>

## <span data-ttu-id="645c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="645c8-104">SYNTAX</span></span>

### <span data-ttu-id="645c8-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="645c8-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="645c8-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="645c8-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="645c8-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="645c8-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="645c8-108">Datei</span><span class="sxs-lookup"><span data-stu-id="645c8-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="645c8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="645c8-109">DESCRIPTION</span></span>
<span data-ttu-id="645c8-110">Das **Cmdlet Remove-AzStorageFile** löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="645c8-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="645c8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="645c8-111">EXAMPLES</span></span>

### <span data-ttu-id="645c8-112">Beispiel 1: Löschen einer Datei aus einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="645c8-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="645c8-113">Mit diesem Befehl wird die Datei mit dem Namen ContosoFile22 aus der Dateifreigabe namens ContosoShare06 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="645c8-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="645c8-114">Beispiel 2: Herunterladen einer Datei aus einer Dateifreigabe mithilfe eines Dateifreigabeobjekts</span><span class="sxs-lookup"><span data-stu-id="645c8-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="645c8-115">Dieser Befehl verwendet das **Get-AzStorageShare-Cmdlet,** um die Dateifreigabe namens ContosoShare06 zu erhalten, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="645c8-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="645c8-116">Mit dem aktuellen Befehl wird die Datei mit dem Namen ContosoFile22 aus ContosoShare06 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="645c8-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="645c8-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="645c8-117">PARAMETERS</span></span>

### <span data-ttu-id="645c8-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="645c8-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="645c8-119">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="645c8-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="645c8-120">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="645c8-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="645c8-121">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="645c8-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="645c8-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="645c8-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="645c8-123">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="645c8-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="645c8-124">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="645c8-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="645c8-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="645c8-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="645c8-126">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="645c8-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="645c8-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="645c8-127">The default value is 10.</span></span>

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

### <span data-ttu-id="645c8-128">-Context</span><span class="sxs-lookup"><span data-stu-id="645c8-128">-Context</span></span>
<span data-ttu-id="645c8-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="645c8-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="645c8-130">Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="645c8-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="645c8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645c8-131">-DefaultProfile</span></span>
<span data-ttu-id="645c8-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="645c8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="645c8-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="645c8-133">-Directory</span></span>
<span data-ttu-id="645c8-134">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="645c8-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="645c8-135">Dieses Cmdlet entfernt eine Datei in dem Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="645c8-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="645c8-136">-Datei</span><span class="sxs-lookup"><span data-stu-id="645c8-136">-File</span></span>
<span data-ttu-id="645c8-137">Gibt eine Datei als **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="645c8-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="645c8-138">Dieses Cmdlet entfernt die Datei, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="645c8-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="645c8-139">Zum Abrufen eines **CloudFile-Objekts** verwenden Sie das Get-AzStorageFile Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="645c8-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="645c8-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="645c8-140">-PassThru</span></span>
<span data-ttu-id="645c8-141">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="645c8-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="645c8-142">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="645c8-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="645c8-143">-Path</span><span class="sxs-lookup"><span data-stu-id="645c8-143">-Path</span></span>
<span data-ttu-id="645c8-144">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="645c8-144">Specifies the path of a file.</span></span>
<span data-ttu-id="645c8-145">Dieses Cmdlet löscht die Datei, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="645c8-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="645c8-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="645c8-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="645c8-147">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="645c8-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="645c8-148">-Teilen</span><span class="sxs-lookup"><span data-stu-id="645c8-148">-Share</span></span>
<span data-ttu-id="645c8-149">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="645c8-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="645c8-150">Dieses Cmdlet entfernt die Datei in der freigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="645c8-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="645c8-151">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="645c8-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="645c8-152">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="645c8-152">This object contains the storage context.</span></span>
<span data-ttu-id="645c8-153">Wenn Sie diesen Parameter angeben, geben Sie den Parameter *Kontext nicht* an.</span><span class="sxs-lookup"><span data-stu-id="645c8-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="645c8-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="645c8-154">-ShareName</span></span>
<span data-ttu-id="645c8-155">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="645c8-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="645c8-156">Dieses Cmdlet entfernt die Datei in der freigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="645c8-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="645c8-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="645c8-157">-Confirm</span></span>
<span data-ttu-id="645c8-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="645c8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645c8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645c8-159">-WhatIf</span></span>
<span data-ttu-id="645c8-160">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="645c8-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="645c8-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="645c8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645c8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645c8-162">CommonParameters</span></span>
<span data-ttu-id="645c8-163">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="645c8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645c8-164">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="645c8-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645c8-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="645c8-165">INPUTS</span></span>

### <span data-ttu-id="645c8-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="645c8-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="645c8-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="645c8-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="645c8-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="645c8-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="645c8-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="645c8-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="645c8-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="645c8-170">OUTPUTS</span></span>

### <span data-ttu-id="645c8-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="645c8-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="645c8-172">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="645c8-172">NOTES</span></span>

## <span data-ttu-id="645c8-173">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="645c8-173">RELATED LINKS</span></span>

[<span data-ttu-id="645c8-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="645c8-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="645c8-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="645c8-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="645c8-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="645c8-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
