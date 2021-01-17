---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 811671E9-592E-4E58-8174-34D665206A65
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageFile.md
ms.openlocfilehash: 99809e5115cb256b8e546334efce0e6e399be04f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460215"
---
# <span data-ttu-id="8ccb5-101">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="8ccb5-101">Remove-AzStorageFile</span></span>

## <span data-ttu-id="8ccb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ccb5-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccb5-103">Löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-103">Deletes a file.</span></span>

## <span data-ttu-id="8ccb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ccb5-104">SYNTAX</span></span>

### <span data-ttu-id="8ccb5-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ccb5-105">ShareName (Default)</span></span>
```
Remove-AzStorageFile [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ccb5-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="8ccb5-106">Share</span></span>
```
Remove-AzStorageFile [-Share] <CloudFileShare> [-Path] <String> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccb5-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="8ccb5-107">Directory</span></span>
```
Remove-AzStorageFile [-Directory] <CloudFileDirectory> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ccb5-108">Datei</span><span class="sxs-lookup"><span data-stu-id="8ccb5-108">File</span></span>
```
Remove-AzStorageFile [-File] <CloudFile> [-PassThru] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ccb5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ccb5-109">DESCRIPTION</span></span>
<span data-ttu-id="8ccb5-110">Das **Cmdlet "Remove-AzStorageFile"** löscht eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-110">The **Remove-AzStorageFile** cmdlet deletes a file.</span></span>

## <span data-ttu-id="8ccb5-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ccb5-111">EXAMPLES</span></span>

### <span data-ttu-id="8ccb5-112">Beispiel 1: Löschen einer Datei aus einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="8ccb5-112">Example 1: Delete a file from a file share</span></span>
```
PS C:\>Remove-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoFile22"
```

<span data-ttu-id="8ccb5-113">Mit diesem Befehl wird die Datei mit dem Namen "ContosoFile22" aus der Dateifreigabe "ContosoShare06" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-113">This command deletes the file that is named ContosoFile22 from the file share named ContosoShare06.</span></span>

### <span data-ttu-id="8ccb5-114">Beispiel 2: Herunterladen einer Datei aus einer Dateifreigabe mithilfe eines Dateifreigabeobjekts</span><span class="sxs-lookup"><span data-stu-id="8ccb5-114">Example 2: Get a file from a file share by using a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | Remove-AzStorageFile -Path "ContosoFile22"
```

<span data-ttu-id="8ccb5-115">Dieser Befehl verwendet das **Cmdlet "Get-AzStorageShare",** um die Dateifreigabe "ContosoShare06" zu erhalten, und übergibt dieses Objekt dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8ccb5-116">Mit dem aktuellen Befehl wird die Datei mit dem Namen "ContosoFile22" aus "ContosoShare06" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-116">The current command deletes the file that is named ContosoFile22 from ContosoShare06.</span></span>

## <span data-ttu-id="8ccb5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ccb5-117">PARAMETERS</span></span>

### <span data-ttu-id="8ccb5-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8ccb5-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8ccb5-119">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8ccb5-120">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8ccb5-121">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8ccb5-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8ccb5-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8ccb5-123">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8ccb5-124">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8ccb5-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8ccb5-126">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8ccb5-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-127">The default value is 10.</span></span>

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

### <span data-ttu-id="8ccb5-128">-Context</span><span class="sxs-lookup"><span data-stu-id="8ccb5-128">-Context</span></span>
<span data-ttu-id="8ccb5-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8ccb5-130">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="8ccb5-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="8ccb5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccb5-131">-DefaultProfile</span></span>
<span data-ttu-id="8ccb5-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ccb5-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="8ccb5-133">-Directory</span></span>
<span data-ttu-id="8ccb5-134">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="8ccb5-135">Dieses Cmdlet entfernt eine Datei in dem Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-135">This cmdlet removes a file in the folder that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ccb5-136">-File</span><span class="sxs-lookup"><span data-stu-id="8ccb5-136">-File</span></span>
<span data-ttu-id="8ccb5-137">Gibt eine Datei als **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-137">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="8ccb5-138">Dieses Cmdlet entfernt die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-138">This cmdlet removes the file that this parameter specifies.</span></span>
<span data-ttu-id="8ccb5-139">Verwenden Sie zum Abrufen eines **CloudFile-Objekts** das Get-AzStorageFile-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-139">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="8ccb5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ccb5-140">-PassThru</span></span>
<span data-ttu-id="8ccb5-141">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-141">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8ccb5-142">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8ccb5-143">-Path</span><span class="sxs-lookup"><span data-stu-id="8ccb5-143">-Path</span></span>
<span data-ttu-id="8ccb5-144">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-144">Specifies the path of a file.</span></span>
<span data-ttu-id="8ccb5-145">Dieses Cmdlet löscht die Datei, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-145">This cmdlet deletes the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ccb5-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8ccb5-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8ccb5-147">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-147">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="8ccb5-148">-Teilen</span><span class="sxs-lookup"><span data-stu-id="8ccb5-148">-Share</span></span>
<span data-ttu-id="8ccb5-149">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="8ccb5-150">Mit diesem Cmdlet wird die Datei in dem von diesem Parameter angegebenen Freigabe entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-150">This cmdlet removes the file in the share this parameter specifies.</span></span>
<span data-ttu-id="8ccb5-151">Verwenden Sie zum Abrufen **eines CloudFileShare-Objekts** das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="8ccb5-152">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-152">This object contains the storage context.</span></span>
<span data-ttu-id="8ccb5-153">Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="8ccb5-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8ccb5-154">-ShareName</span></span>
<span data-ttu-id="8ccb5-155">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="8ccb5-156">Mit diesem Cmdlet wird die Datei in dem von diesem Parameter angegebenen Freigabe entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-156">This cmdlet removes the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="8ccb5-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ccb5-157">-Confirm</span></span>
<span data-ttu-id="8ccb5-158">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ccb5-159">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8ccb5-159">-WhatIf</span></span>
<span data-ttu-id="8ccb5-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ccb5-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ccb5-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccb5-162">CommonParameters</span></span>
<span data-ttu-id="8ccb5-163">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ccb5-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccb5-164">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ccb5-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccb5-165">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ccb5-165">INPUTS</span></span>

### <span data-ttu-id="8ccb5-166">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="8ccb5-166">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="8ccb5-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="8ccb5-167">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="8ccb5-168">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="8ccb5-168">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8ccb5-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ccb5-169">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8ccb5-170">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ccb5-170">OUTPUTS</span></span>

### <span data-ttu-id="8ccb5-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="8ccb5-171">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="8ccb5-172">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8ccb5-172">NOTES</span></span>

## <span data-ttu-id="8ccb5-173">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8ccb5-173">RELATED LINKS</span></span>

[<span data-ttu-id="8ccb5-174">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="8ccb5-174">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="8ccb5-175">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="8ccb5-175">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="8ccb5-176">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="8ccb5-176">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
