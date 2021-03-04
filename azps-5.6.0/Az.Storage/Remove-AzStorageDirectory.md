---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 87e8792697093182d3ccd36d75ac072239f76e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931600"
---
# <span data-ttu-id="8d9da-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8d9da-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="8d9da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9da-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9da-103">Löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8d9da-103">Deletes a directory.</span></span>

## <span data-ttu-id="8d9da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d9da-104">SYNTAX</span></span>

### <span data-ttu-id="8d9da-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d9da-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d9da-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="8d9da-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d9da-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8d9da-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d9da-108">DESCRIPTION</span></span>
<span data-ttu-id="8d9da-109">Das **Cmdlet Remove-AzStorageDirectory** löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="8d9da-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="8d9da-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d9da-110">EXAMPLES</span></span>

### <span data-ttu-id="8d9da-111">Beispiel 1: Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="8d9da-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="8d9da-112">Mit diesem Befehl wird der Ordner ContosoWorkingFolder aus der Dateifreigabe namens ContosoShare06 gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8d9da-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="8d9da-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d9da-113">PARAMETERS</span></span>

### <span data-ttu-id="8d9da-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d9da-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8d9da-115">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8d9da-116">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d9da-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8d9da-117">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9da-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8d9da-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8d9da-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8d9da-119">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8d9da-120">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="8d9da-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8d9da-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8d9da-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8d9da-122">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8d9da-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8d9da-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8d9da-123">The default value is 10.</span></span>

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

### <span data-ttu-id="8d9da-124">-Context</span><span class="sxs-lookup"><span data-stu-id="8d9da-124">-Context</span></span>
<span data-ttu-id="8d9da-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8d9da-126">Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="8d9da-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8d9da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9da-127">-DefaultProfile</span></span>
<span data-ttu-id="8d9da-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d9da-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9da-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="8d9da-129">-Directory</span></span>
<span data-ttu-id="8d9da-130">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8d9da-131">Dieses Cmdlet entfernt den Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8d9da-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="8d9da-132">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d9da-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="8d9da-133">Sie können auch das **Get-AzStorageFile-Cmdlet** verwenden, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d9da-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="8d9da-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d9da-134">-PassThru</span></span>
<span data-ttu-id="8d9da-135">Gibt an, dass, wenn dieses Cmdlet erfolgreich ist, ein Wert von $True.</span><span class="sxs-lookup"><span data-stu-id="8d9da-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="8d9da-136">Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines  unangemessenen Werts für den Parameter Pfad nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9da-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="8d9da-137">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9da-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8d9da-138">-Path</span><span class="sxs-lookup"><span data-stu-id="8d9da-138">-Path</span></span>
<span data-ttu-id="8d9da-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="8d9da-140">Wenn der ordner, den dieser Parameter angibt, leer ist, löscht dieses Cmdlet diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="8d9da-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="8d9da-141">Wenn der Ordner nicht leer ist, nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8d9da-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="8d9da-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8d9da-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8d9da-143">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8d9da-144">-Teilen</span><span class="sxs-lookup"><span data-stu-id="8d9da-144">-Share</span></span>
<span data-ttu-id="8d9da-145">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8d9da-146">Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8d9da-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="8d9da-147">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d9da-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="8d9da-148">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="8d9da-148">This object contains the storage context.</span></span>
<span data-ttu-id="8d9da-149">Wenn Sie diesen Parameter angeben, geben Sie den Parameter *Kontext nicht* an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="8d9da-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8d9da-150">-ShareName</span></span>
<span data-ttu-id="8d9da-151">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8d9da-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="8d9da-152">Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8d9da-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d9da-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d9da-153">-Confirm</span></span>
<span data-ttu-id="8d9da-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d9da-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9da-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9da-155">-WhatIf</span></span>
<span data-ttu-id="8d9da-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d9da-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9da-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d9da-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9da-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9da-158">CommonParameters</span></span>
<span data-ttu-id="8d9da-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9da-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9da-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9da-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9da-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d9da-161">INPUTS</span></span>

### <span data-ttu-id="8d9da-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8d9da-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="8d9da-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8d9da-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="8d9da-164">System.String</span><span class="sxs-lookup"><span data-stu-id="8d9da-164">System.String</span></span>

### <span data-ttu-id="8d9da-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d9da-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8d9da-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d9da-166">OUTPUTS</span></span>

### <span data-ttu-id="8d9da-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8d9da-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="8d9da-168">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d9da-168">NOTES</span></span>

## <span data-ttu-id="8d9da-169">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d9da-169">RELATED LINKS</span></span>

[<span data-ttu-id="8d9da-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8d9da-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="8d9da-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8d9da-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8d9da-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="8d9da-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
