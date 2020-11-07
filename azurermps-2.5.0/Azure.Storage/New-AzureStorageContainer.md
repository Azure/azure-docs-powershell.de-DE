---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 87967dbaaa57bb8050191ee1b20ebb5a760bc045
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849440"
---
# <span data-ttu-id="c6a7c-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c6a7c-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="c6a7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a7c-103">Erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6a7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6a7c-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c6a7c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a7c-106">Das Cmdlet **New-AzureStorageContainer** erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="c6a7c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a7c-108">Beispiel 1: Erstellen eines Azure-Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="c6a7c-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="c6a7c-109">Mit diesem Befehl wird ein Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-109">This command creates a storage container.</span></span>

### <span data-ttu-id="c6a7c-110">Beispiel 2: Erstellen mehrerer Azure-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="c6a7c-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="c6a7c-111">In diesem Beispiel werden mehrere Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="c6a7c-112">Sie verwendet die **Split** -Methode der .net- **Zeichenfolgen** Klasse und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="c6a7c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6a7c-113">PARAMETERS</span></span>

### <span data-ttu-id="c6a7c-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6a7c-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6a7c-115">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6a7c-116">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6a7c-117">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6a7c-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6a7c-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6a7c-119">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6a7c-120">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6a7c-121">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6a7c-122">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6a7c-123">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-123">The default value is 10.</span></span>

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

### <span data-ttu-id="c6a7c-124">-Context</span><span class="sxs-lookup"><span data-stu-id="c6a7c-124">-Context</span></span>
<span data-ttu-id="c6a7c-125">Gibt einen Kontext für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="c6a7c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a7c-126">-DefaultProfile</span></span>
<span data-ttu-id="c6a7c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a7c-128">-Name</span></span>
<span data-ttu-id="c6a7c-129">Gibt einen Namen für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="c6a7c-130">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="c6a7c-130">-Permission</span></span>
<span data-ttu-id="c6a7c-131">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="c6a7c-132">Standardmäßig kann der Container und alle darin enthaltenen BLOBs nur vom Besitzer des speicherkontos aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="c6a7c-133">Um anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs zu erteilen, können Sie die Container Berechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="c6a7c-134">Anonyme Benutzer können BLOBs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="c6a7c-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c6a7c-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6a7c-136">Container.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-136">Container.</span></span>
<span data-ttu-id="c6a7c-137">Bietet vollständigen Lesezugriff auf einen Container und seine BLOBs.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="c6a7c-138">Clients können BLOBs im Container mithilfe einer anonymen Anforderung auflisten, aber keine Container im Speicherkonto auflisten.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="c6a7c-139">BLOB.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-139">Blob.</span></span>
<span data-ttu-id="c6a7c-140">Bietet Lesezugriff auf BLOB-Daten in einem Container durch anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="c6a7c-141">Clients können keine BLOBs im Container mithilfe einer anonymen Anforderung auflisten.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="c6a7c-142">Aus.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-142">Off.</span></span>
<span data-ttu-id="c6a7c-143">Dadurch wird der Zugriff auf den Besitzer des speicherkontos eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6a7c-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6a7c-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6a7c-145">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c6a7c-146">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c6a7c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a7c-147">CommonParameters</span></span>
<span data-ttu-id="c6a7c-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a7c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a7c-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a7c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a7c-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6a7c-150">INPUTS</span></span>

### <span data-ttu-id="c6a7c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c6a7c-151">System.String</span></span>

### <span data-ttu-id="c6a7c-152">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6a7c-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6a7c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6a7c-153">OUTPUTS</span></span>

### <span data-ttu-id="c6a7c-154">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c6a7c-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c6a7c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6a7c-155">NOTES</span></span>

## <span data-ttu-id="c6a7c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6a7c-156">RELATED LINKS</span></span>

[<span data-ttu-id="c6a7c-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c6a7c-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="c6a7c-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c6a7c-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="c6a7c-159">Satz-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c6a7c-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


