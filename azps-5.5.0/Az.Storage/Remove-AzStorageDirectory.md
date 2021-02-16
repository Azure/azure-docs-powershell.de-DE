---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162945"
---
# <span data-ttu-id="b0e3e-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b0e3e-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="b0e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e3e-103">Löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-103">Deletes a directory.</span></span>

## <span data-ttu-id="b0e3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0e3e-104">SYNTAX</span></span>

### <span data-ttu-id="b0e3e-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0e3e-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e3e-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="b0e3e-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b0e3e-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="b0e3e-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e3e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0e3e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e3e-109">Das **Cmdlet "Remove-AzStorageDirectory"** löscht ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="b0e3e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0e3e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e3e-111">Beispiel 1: Löschen eines Ordners</span><span class="sxs-lookup"><span data-stu-id="b0e3e-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b0e3e-112">Mit diesem Befehl wird der Ordner "ContosoWorkingFolder" aus der Dateifreigabe namens "ContosoShare06" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="b0e3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e3e-113">PARAMETERS</span></span>

### <span data-ttu-id="b0e3e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0e3e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b0e3e-115">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b0e3e-116">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b0e3e-117">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b0e3e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b0e3e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b0e3e-119">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b0e3e-120">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b0e3e-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b0e3e-122">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b0e3e-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b0e3e-124">-Context</span><span class="sxs-lookup"><span data-stu-id="b0e3e-124">-Context</span></span>
<span data-ttu-id="b0e3e-125">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b0e3e-126">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="b0e3e-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b0e3e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e3e-127">-DefaultProfile</span></span>
<span data-ttu-id="b0e3e-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e3e-129">-Directory</span><span class="sxs-lookup"><span data-stu-id="b0e3e-129">-Directory</span></span>
<span data-ttu-id="b0e3e-130">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b0e3e-131">Dieses Cmdlet entfernt den Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="b0e3e-132">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b0e3e-133">Sie können auch das **Cmdlet "Get-AzStorageFile"** verwenden, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b0e3e-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0e3e-134">-PassThru</span></span>
<span data-ttu-id="b0e3e-135">Gibt an, dass bei einem erfolgreichen Cmdlet der Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="b0e3e-136">Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines ungeeigneten Werts für den Parameter _"Path"_ nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="b0e3e-137">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b0e3e-138">-Path</span><span class="sxs-lookup"><span data-stu-id="b0e3e-138">-Path</span></span>
<span data-ttu-id="b0e3e-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="b0e3e-140">Wenn der von diesem Parameter festgelegte Ordner leer ist, löscht dieses Cmdlet diesen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="b0e3e-141">Wenn der Ordner nicht leer ist, nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="b0e3e-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b0e3e-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b0e3e-143">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b0e3e-144">-Teilen</span><span class="sxs-lookup"><span data-stu-id="b0e3e-144">-Share</span></span>
<span data-ttu-id="b0e3e-145">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b0e3e-146">Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="b0e3e-147">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="b0e3e-148">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-148">This object contains the storage context.</span></span>
<span data-ttu-id="b0e3e-149">Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b0e3e-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b0e3e-150">-ShareName</span></span>
<span data-ttu-id="b0e3e-151">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="b0e3e-152">Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="b0e3e-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0e3e-153">-Confirm</span></span>
<span data-ttu-id="b0e3e-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e3e-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0e3e-155">-WhatIf</span></span>
<span data-ttu-id="b0e3e-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e3e-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e3e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e3e-158">CommonParameters</span></span>
<span data-ttu-id="b0e3e-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e3e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e3e-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e3e-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e3e-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0e3e-161">INPUTS</span></span>

### <span data-ttu-id="b0e3e-162">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b0e3e-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="b0e3e-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b0e3e-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="b0e3e-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b0e3e-164">System.String</span></span>

### <span data-ttu-id="b0e3e-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0e3e-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0e3e-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0e3e-166">OUTPUTS</span></span>

### <span data-ttu-id="b0e3e-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b0e3e-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="b0e3e-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0e3e-168">NOTES</span></span>

## <span data-ttu-id="b0e3e-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0e3e-169">RELATED LINKS</span></span>

[<span data-ttu-id="b0e3e-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="b0e3e-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="b0e3e-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0e3e-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b0e3e-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b0e3e-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
