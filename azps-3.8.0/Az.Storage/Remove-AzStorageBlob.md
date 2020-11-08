---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: dd93de8d7bbbccdda1841a73b2c8f3a810592669
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004874"
---
# <span data-ttu-id="8a13d-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a13d-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="8a13d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a13d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a13d-103">Entfernt das angegebene Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a13d-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="8a13d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a13d-104">SYNTAX</span></span>

### <span data-ttu-id="8a13d-105">NamePipeline (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a13d-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a13d-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="8a13d-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a13d-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="8a13d-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a13d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a13d-108">DESCRIPTION</span></span>
<span data-ttu-id="8a13d-109">Das Cmdlet **Remove-AzStorageBlob** entfernt das angegebene BLOB aus einem Speicherkonto in Azure.</span><span class="sxs-lookup"><span data-stu-id="8a13d-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="8a13d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a13d-110">EXAMPLES</span></span>

### <span data-ttu-id="8a13d-111">Beispiel 1: Entfernen eines Speicher-BLOBs nach Name</span><span class="sxs-lookup"><span data-stu-id="8a13d-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="8a13d-112">Mit diesem Befehl wird ein BLOB entfernt, das mit dem Namen identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a13d-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="8a13d-113">Beispiel 2: Entfernen eines Speicher-BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8a13d-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="8a13d-114">Dieser Befehl verwendet die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a13d-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="8a13d-115">Beispiel 3: Entfernen von Speicher-BLOBs mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="8a13d-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="8a13d-116">Dieser Befehl verwendet das Sternchen (\*)-Platzhalterzeichen und die Pipeline, um das BLOB oder die BLOBs abzurufen und dann zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8a13d-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="8a13d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a13d-117">PARAMETERS</span></span>

### <span data-ttu-id="8a13d-118">-BLOB</span><span class="sxs-lookup"><span data-stu-id="8a13d-118">-Blob</span></span>
<span data-ttu-id="8a13d-119">Gibt den Namen des zu entfernenden BLOB an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="8a13d-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a13d-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="8a13d-121">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="8a13d-122">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="8a13d-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="8a13d-123">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="8a13d-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="8a13d-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a13d-124">-CloudBlob</span></span>
<span data-ttu-id="8a13d-125">Gibt ein Cloud-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="8a13d-126">Verwenden Sie das Get-AzStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8a13d-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="8a13d-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a13d-127">-CloudBlobContainer</span></span>
<span data-ttu-id="8a13d-128">Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="8a13d-129">Sie können das Get-AzStorageContainer-Cmdlet verwenden, um es abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8a13d-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="8a13d-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="8a13d-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="8a13d-131">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="8a13d-132">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="8a13d-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="8a13d-133">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="8a13d-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="8a13d-134">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="8a13d-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="8a13d-135">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="8a13d-135">The default value is 10.</span></span>

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

### <span data-ttu-id="8a13d-136">-Container</span><span class="sxs-lookup"><span data-stu-id="8a13d-136">-Container</span></span>
<span data-ttu-id="8a13d-137">Gibt den Namen des Containers an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="8a13d-138">-Context</span><span class="sxs-lookup"><span data-stu-id="8a13d-138">-Context</span></span>
<span data-ttu-id="8a13d-139">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8a13d-140">Sie können das New-AzStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8a13d-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="8a13d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a13d-141">-DefaultProfile</span></span>
<span data-ttu-id="8a13d-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a13d-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a13d-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="8a13d-143">-DeleteSnapshot</span></span>
<span data-ttu-id="8a13d-144">Gibt an, dass alle Snapshots gelöscht werden, aber nicht das Basis-BLOB.</span><span class="sxs-lookup"><span data-stu-id="8a13d-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="8a13d-145">Wenn dieser Parameter nicht angegeben wird, werden das Basis-BLOB und dessen Snapshots zusammen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8a13d-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="8a13d-146">Der Benutzer wird aufgefordert, den Löschvorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="8a13d-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="8a13d-147">-Force</span><span class="sxs-lookup"><span data-stu-id="8a13d-147">-Force</span></span>
<span data-ttu-id="8a13d-148">Gibt an, dass dieses Cmdlet das BLOB und seinen Snapshot ohne Bestätigung entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a13d-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="8a13d-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a13d-149">-PassThru</span></span>
<span data-ttu-id="8a13d-150">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="8a13d-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8a13d-151">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a13d-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8a13d-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="8a13d-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="8a13d-153">Gibt das Azure-Profil für das zu lesende Cmdlet an.</span><span class="sxs-lookup"><span data-stu-id="8a13d-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="8a13d-154">Wenn keine Angabe erfolgt, liest das Cmdlet aus dem Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8a13d-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="8a13d-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a13d-155">-Confirm</span></span>
<span data-ttu-id="8a13d-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a13d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a13d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a13d-157">-WhatIf</span></span>
<span data-ttu-id="8a13d-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a13d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a13d-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a13d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a13d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a13d-160">CommonParameters</span></span>
<span data-ttu-id="8a13d-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a13d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a13d-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a13d-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a13d-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a13d-163">INPUTS</span></span>

### <span data-ttu-id="8a13d-164">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="8a13d-164">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="8a13d-165">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="8a13d-165">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="8a13d-166">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a13d-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a13d-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a13d-167">OUTPUTS</span></span>

### <span data-ttu-id="8a13d-168">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a13d-168">System.Boolean</span></span>

## <span data-ttu-id="8a13d-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a13d-169">NOTES</span></span>

## <span data-ttu-id="8a13d-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a13d-170">RELATED LINKS</span></span>

[<span data-ttu-id="8a13d-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="8a13d-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="8a13d-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8a13d-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="8a13d-173">Satz-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8a13d-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
