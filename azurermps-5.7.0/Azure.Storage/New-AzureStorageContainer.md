---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
ms.openlocfilehash: 27442311630bf57f9424d940397f4fc8ef0655fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663510"
---
# <span data-ttu-id="989e9-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="989e9-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="989e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="989e9-102">SYNOPSIS</span></span>
<span data-ttu-id="989e9-103">Erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="989e9-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="989e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="989e9-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="989e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="989e9-105">DESCRIPTION</span></span>
<span data-ttu-id="989e9-106">Das Cmdlet **New-AzureStorageContainer** erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="989e9-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="989e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="989e9-107">EXAMPLES</span></span>

### <span data-ttu-id="989e9-108">Beispiel 1: Erstellen eines Azure-Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="989e9-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="989e9-109">Mit diesem Befehl wird ein Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="989e9-109">This command creates a storage container.</span></span>

### <span data-ttu-id="989e9-110">Beispiel 2: Erstellen mehrerer Azure-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="989e9-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="989e9-111">In diesem Beispiel werden mehrere Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="989e9-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="989e9-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="989e9-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="989e9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="989e9-113">PARAMETERS</span></span>

### <span data-ttu-id="989e9-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="989e9-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="989e9-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="989e9-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="989e9-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="989e9-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="989e9-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="989e9-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="989e9-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="989e9-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="989e9-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="989e9-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="989e9-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="989e9-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="989e9-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="989e9-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="989e9-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="989e9-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="989e9-123">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-124">-Context</span><span class="sxs-lookup"><span data-stu-id="989e9-124">-Context</span></span>
<span data-ttu-id="989e9-125">Gibt einen Kontext für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="989e9-125">Specifies a context for the new container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="989e9-126">-Name</span></span>
<span data-ttu-id="989e9-127">Gibt einen Namen für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="989e9-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="989e9-128">-Permission</span></span>
<span data-ttu-id="989e9-129">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="989e9-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="989e9-130">Standardmäßig kann der Container und alle darin enthaltenen BLOBs nur vom Besitzer des speicherkontos aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="989e9-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="989e9-131">Um anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs zu erteilen, können Sie die Container Berechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="989e9-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="989e9-132">Anonyme Benutzer können BLOBs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="989e9-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="989e9-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="989e9-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="989e9-134">Container.</span><span class="sxs-lookup"><span data-stu-id="989e9-134">Container.</span></span>
<span data-ttu-id="989e9-135">Bietet vollständigen Lesezugriff auf einen Container und seine BLOBs.</span><span class="sxs-lookup"><span data-stu-id="989e9-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="989e9-136">Clients können BLOBs im Container mithilfe einer anonymen Anforderung auflisten, aber keine Container im Speicherkonto auflisten.</span><span class="sxs-lookup"><span data-stu-id="989e9-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="989e9-137">BLOB.</span><span class="sxs-lookup"><span data-stu-id="989e9-137">Blob.</span></span>
<span data-ttu-id="989e9-138">Bietet Lesezugriff auf BLOB-Daten in einem Container durch anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="989e9-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="989e9-139">Clients können keine BLOBs im Container mithilfe einer anonymen Anforderung auflisten.</span><span class="sxs-lookup"><span data-stu-id="989e9-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="989e9-140">Aus.</span><span class="sxs-lookup"><span data-stu-id="989e9-140">Off.</span></span>
<span data-ttu-id="989e9-141">Dadurch wird der Zugriff auf den Besitzer des speicherkontos eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="989e9-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="989e9-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="989e9-143">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="989e9-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="989e9-144">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="989e9-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989e9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989e9-145">CommonParameters</span></span>
<span data-ttu-id="989e9-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989e9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989e9-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989e9-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989e9-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="989e9-148">INPUTS</span></span>

### <span data-ttu-id="989e9-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="989e9-149">IStorageContext</span></span>

<span data-ttu-id="989e9-150">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="989e9-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="989e9-151">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="989e9-151">String</span></span>

<span data-ttu-id="989e9-152">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="989e9-152">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="989e9-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="989e9-153">OUTPUTS</span></span>

### <span data-ttu-id="989e9-154">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="989e9-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="989e9-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="989e9-155">NOTES</span></span>

## <span data-ttu-id="989e9-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="989e9-156">RELATED LINKS</span></span>

[<span data-ttu-id="989e9-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="989e9-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="989e9-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="989e9-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="989e9-159">Satz-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="989e9-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


