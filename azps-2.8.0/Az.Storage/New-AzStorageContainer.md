---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: c4e3ba53ccb583b72001bfdfcc08c15025eda0da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826719"
---
# <span data-ttu-id="1a667-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1a667-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="1a667-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a667-102">SYNOPSIS</span></span>
<span data-ttu-id="1a667-103">Erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="1a667-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="1a667-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a667-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1a667-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a667-105">DESCRIPTION</span></span>
<span data-ttu-id="1a667-106">Das Cmdlet **New-AzStorageContainer** erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="1a667-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="1a667-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a667-107">EXAMPLES</span></span>

### <span data-ttu-id="1a667-108">Beispiel 1: Erstellen eines Azure-Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="1a667-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="1a667-109">Mit diesem Befehl wird ein Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a667-109">This command creates a storage container.</span></span>

### <span data-ttu-id="1a667-110">Beispiel 2: Erstellen mehrerer Azure-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="1a667-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="1a667-111">In diesem Beispiel werden mehrere Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="1a667-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="1a667-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1a667-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="1a667-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a667-113">PARAMETERS</span></span>

### <span data-ttu-id="1a667-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a667-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a667-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1a667-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a667-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="1a667-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a667-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1a667-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a667-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a667-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a667-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="1a667-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a667-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="1a667-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a667-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="1a667-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a667-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="1a667-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a667-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1a667-123">The default value is 10.</span></span>

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

### <span data-ttu-id="1a667-124">-Context</span><span class="sxs-lookup"><span data-stu-id="1a667-124">-Context</span></span>
<span data-ttu-id="1a667-125">Gibt einen Kontext für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="1a667-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="1a667-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a667-126">-DefaultProfile</span></span>
<span data-ttu-id="1a667-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a667-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a667-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1a667-128">-Name</span></span>
<span data-ttu-id="1a667-129">Gibt einen Namen für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="1a667-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a667-130">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="1a667-130">-Permission</span></span>
<span data-ttu-id="1a667-131">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="1a667-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="1a667-132">Standardmäßig kann der Container und alle darin enthaltenen BLOBs nur vom Besitzer des speicherkontos aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1a667-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="1a667-133">Um anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs zu erteilen, können Sie die Container Berechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1a667-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="1a667-134">Anonyme Benutzer können BLOBs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="1a667-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="1a667-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1a667-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a667-136">Container.</span><span class="sxs-lookup"><span data-stu-id="1a667-136">Container.</span></span>
<span data-ttu-id="1a667-137">Bietet vollständigen Lesezugriff auf einen Container und seine BLOBs.</span><span class="sxs-lookup"><span data-stu-id="1a667-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="1a667-138">Clients können BLOBs im Container mithilfe einer anonymen Anforderung auflisten, aber keine Container im Speicherkonto auflisten.</span><span class="sxs-lookup"><span data-stu-id="1a667-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="1a667-139">BLOB.</span><span class="sxs-lookup"><span data-stu-id="1a667-139">Blob.</span></span>
<span data-ttu-id="1a667-140">Bietet Lesezugriff auf BLOB-Daten in einem Container durch anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="1a667-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="1a667-141">Clients können keine BLOBs im Container mithilfe einer anonymen Anforderung auflisten.</span><span class="sxs-lookup"><span data-stu-id="1a667-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="1a667-142">Aus.</span><span class="sxs-lookup"><span data-stu-id="1a667-142">Off.</span></span>
<span data-ttu-id="1a667-143">Dadurch wird der Zugriff auf den Besitzer des speicherkontos eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="1a667-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a667-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a667-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a667-145">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1a667-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="1a667-146">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1a667-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="1a667-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a667-147">CommonParameters</span></span>
<span data-ttu-id="1a667-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a667-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a667-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a667-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a667-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a667-150">INPUTS</span></span>

### <span data-ttu-id="1a667-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1a667-151">System.String</span></span>

### <span data-ttu-id="1a667-152">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a667-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a667-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a667-153">OUTPUTS</span></span>

### <span data-ttu-id="1a667-154">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1a667-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="1a667-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a667-155">NOTES</span></span>

## <span data-ttu-id="1a667-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a667-156">RELATED LINKS</span></span>

[<span data-ttu-id="1a667-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1a667-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="1a667-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1a667-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="1a667-159">Satz-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="1a667-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


