---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 979cfd1241910cb98bebee3b80bc0a1ab6b8da71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150369"
---
# <span data-ttu-id="f9a4d-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9a4d-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="f9a4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a4d-103">Beendet einen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-103">Stops a copy operation.</span></span>

## <span data-ttu-id="f9a4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a4d-104">SYNTAX</span></span>

### <span data-ttu-id="f9a4d-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9a4d-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9a4d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="f9a4d-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9a4d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="f9a4d-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a4d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9a4d-108">DESCRIPTION</span></span>
<span data-ttu-id="f9a4d-109">Das **Cmdlet "Stop-AzStorageBlobCopy"** beendet einen Kopiervorgang zum angegebenen Ziel-BLOB.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="f9a4d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9a4d-110">EXAMPLES</span></span>

### <span data-ttu-id="f9a4d-111">Beispiel 1: Beenden des Kopiervorgangs nach Name</span><span class="sxs-lookup"><span data-stu-id="f9a4d-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="f9a4d-112">Dieser Befehl beendet den Kopiervorgang nach Name.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="f9a4d-113">Beispiel 2: Beenden des Kopiervorgangs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="f9a4d-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="f9a4d-114">Dieser Befehl beendet den Kopiervorgang, indem der Container aus **"Get-AzStorageContainer"** an die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="f9a4d-115">Beispiel 3: Beenden des Kopiervorgangs mithilfe der Pipeline und Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f9a4d-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="f9a4d-116">In diesem Beispiel wird der Kopiervorgang beendet, indem der Container an die Pipeline aus dem Get-AzStorageBlob übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="f9a4d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9a4d-117">PARAMETERS</span></span>

### <span data-ttu-id="f9a4d-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="f9a4d-118">-Blob</span></span>
<span data-ttu-id="f9a4d-119">Gibt den Namen des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-119">Specifies the name of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a4d-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9a4d-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f9a4d-121">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f9a4d-122">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f9a4d-123">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f9a4d-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f9a4d-124">-CloudBlob</span></span>
<span data-ttu-id="f9a4d-125">Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="f9a4d-126">Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a4d-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f9a4d-127">-CloudBlobContainer</span></span>
<span data-ttu-id="f9a4d-128">Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="f9a4d-129">Sie können das Objekt erstellen oder das cmdlet Get-AzStorageContainer verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a4d-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f9a4d-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f9a4d-131">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f9a4d-132">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f9a4d-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f9a4d-134">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f9a4d-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-135">The default value is 10.</span></span>

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

### <span data-ttu-id="f9a4d-136">-Container</span><span class="sxs-lookup"><span data-stu-id="f9a4d-136">-Container</span></span>
<span data-ttu-id="f9a4d-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-137">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a4d-138">-Context</span><span class="sxs-lookup"><span data-stu-id="f9a4d-138">-Context</span></span>
<span data-ttu-id="f9a4d-139">Gibt den Azure -Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f9a4d-140">Sie können den Kontext mithilfe des New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f9a4d-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="f9a4d-141">-CopyId</span></span>
<span data-ttu-id="f9a4d-142">Gibt die Kopier-ID an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-142">Specifies the copy ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a4d-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a4d-143">-DefaultProfile</span></span>
<span data-ttu-id="f9a4d-144">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a4d-145">-Force</span><span class="sxs-lookup"><span data-stu-id="f9a4d-145">-Force</span></span>
<span data-ttu-id="f9a4d-146">Beendet die aktuelle Kopieraufgabe für das angegebene BLOB ohne Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f9a4d-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9a4d-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f9a4d-148">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f9a4d-149">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f9a4d-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9a4d-150">-Confirm</span></span>
<span data-ttu-id="f9a4d-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9a4d-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f9a4d-152">-WhatIf</span></span>
<span data-ttu-id="f9a4d-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9a4d-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9a4d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a4d-155">CommonParameters</span></span>
<span data-ttu-id="f9a4d-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a4d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a4d-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a4d-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a4d-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9a4d-158">INPUTS</span></span>

### <span data-ttu-id="f9a4d-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f9a4d-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="f9a4d-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f9a4d-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="f9a4d-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9a4d-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f9a4d-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9a4d-162">OUTPUTS</span></span>

### <span data-ttu-id="f9a4d-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f9a4d-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="f9a4d-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f9a4d-164">NOTES</span></span>

## <span data-ttu-id="f9a4d-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f9a4d-165">RELATED LINKS</span></span>

[<span data-ttu-id="f9a4d-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f9a4d-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="f9a4d-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f9a4d-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="f9a4d-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f9a4d-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="f9a4d-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="f9a4d-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
