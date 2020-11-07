---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageContainerAcl.md
ms.openlocfilehash: c3451552d919b33b7dd2dcf72b8b9982f50e8b88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663024"
---
# <span data-ttu-id="ec267-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="ec267-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="ec267-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec267-102">SYNOPSIS</span></span>
<span data-ttu-id="ec267-103">Legt die Berechtigung für den öffentlichen Zugriff auf einen Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="ec267-103">Sets the public access permission to a storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec267-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec267-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ec267-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec267-105">DESCRIPTION</span></span>
<span data-ttu-id="ec267-106">Das Cmdlet " **Set-AzureStorageContainerAcl** " legt die Berechtigung für den öffentlichen Zugriff auf den angegebenen Speichercontainer in Azure fest.</span><span class="sxs-lookup"><span data-stu-id="ec267-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="ec267-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec267-107">EXAMPLES</span></span>

### <span data-ttu-id="ec267-108">Beispiel 1: Einrichten des Azure Storage Container-ACL nach Name</span><span class="sxs-lookup"><span data-stu-id="ec267-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="ec267-109">Dieser Befehl erstellt einen Container, der keinen öffentlichen Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="ec267-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="ec267-110">Beispiel 2: Einrichten der Azure-Speichercontainer-ACL mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="ec267-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="ec267-111">Dieser Befehl ruft alle Speichercontainer ab, deren Name mit dem Container beginnt, und übergibt dann das Ergebnis in der Pipeline, um die Berechtigung für alle auf den BLOB-Zugriff zu setzen.</span><span class="sxs-lookup"><span data-stu-id="ec267-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="ec267-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec267-112">PARAMETERS</span></span>

### <span data-ttu-id="ec267-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec267-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ec267-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ec267-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ec267-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="ec267-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ec267-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ec267-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ec267-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ec267-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ec267-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="ec267-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ec267-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="ec267-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ec267-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="ec267-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ec267-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="ec267-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ec267-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="ec267-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ec267-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ec267-123">-Context</span></span>
<span data-ttu-id="ec267-124">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="ec267-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ec267-125">Sie können es mithilfe des New-AzureStorageContext-Cmdlets erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec267-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ec267-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec267-126">-DefaultProfile</span></span>
<span data-ttu-id="ec267-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec267-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec267-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ec267-128">-Name</span></span>
<span data-ttu-id="ec267-129">Gibt einen Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="ec267-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="ec267-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec267-130">-PassThru</span></span>
<span data-ttu-id="ec267-131">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ec267-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec267-132">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ec267-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec267-133">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="ec267-133">-Permission</span></span>
<span data-ttu-id="ec267-134">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="ec267-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="ec267-135">Standardmäßig kann der Container und alle darin enthaltenen BLOBs nur vom Besitzer des speicherkontos aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ec267-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="ec267-136">Um anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs zu erteilen, können Sie die Container Berechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec267-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="ec267-137">Anonyme Benutzer können BLOBs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="ec267-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="ec267-138">Die akzeptablen Werte für diesen Parameter sind:--Container.</span><span class="sxs-lookup"><span data-stu-id="ec267-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="ec267-139">Bietet vollständigen Lesezugriff auf einen Container und seine BLOBs.</span><span class="sxs-lookup"><span data-stu-id="ec267-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="ec267-140">Clients können BLOBs im Container mithilfe einer anonymen Anforderung auflisten, aber keine Container im Speicherkonto auflisten.</span><span class="sxs-lookup"><span data-stu-id="ec267-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="ec267-141">--BLOB.</span><span class="sxs-lookup"><span data-stu-id="ec267-141">--Blob.</span></span>
<span data-ttu-id="ec267-142">Bietet Lesezugriff auf BLOB-Daten in einem Container durch anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="ec267-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="ec267-143">Clients können keine BLOBs im Container mithilfe einer anonymen Anforderung auflisten.</span><span class="sxs-lookup"><span data-stu-id="ec267-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="ec267-144">--Aus.</span><span class="sxs-lookup"><span data-stu-id="ec267-144">--Off.</span></span>
<span data-ttu-id="ec267-145">Beschränkt den Zugriff auf den Besitzer des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="ec267-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec267-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec267-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ec267-147">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ec267-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ec267-148">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ec267-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="ec267-149">Server seitige Timeout für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ec267-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="ec267-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec267-150">CommonParameters</span></span>
<span data-ttu-id="ec267-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec267-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec267-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec267-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec267-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec267-153">INPUTS</span></span>

### <span data-ttu-id="ec267-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ec267-154">System.String</span></span>

### <span data-ttu-id="ec267-155">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec267-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ec267-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec267-156">OUTPUTS</span></span>

### <span data-ttu-id="ec267-157">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec267-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="ec267-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec267-158">NOTES</span></span>

## <span data-ttu-id="ec267-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec267-159">RELATED LINKS</span></span>

[<span data-ttu-id="ec267-160">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec267-160">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="ec267-161">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec267-161">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="ec267-162">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec267-162">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


