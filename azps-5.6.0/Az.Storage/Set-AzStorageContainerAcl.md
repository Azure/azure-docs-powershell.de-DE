---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944435"
---
# <span data-ttu-id="2858a-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2858a-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="2858a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2858a-102">SYNOPSIS</span></span>
<span data-ttu-id="2858a-103">Legt die Berechtigung für den öffentlichen Zugriff auf einen Speichercontainer fest.</span><span class="sxs-lookup"><span data-stu-id="2858a-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="2858a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2858a-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2858a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2858a-105">DESCRIPTION</span></span>
<span data-ttu-id="2858a-106">Das **Cmdlet Set-AzStorageContainerAcl** legt die Berechtigung für den öffentlichen Zugriff auf den angegebenen Speichercontainer in Azure fest.</span><span class="sxs-lookup"><span data-stu-id="2858a-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="2858a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2858a-107">EXAMPLES</span></span>

### <span data-ttu-id="2858a-108">Beispiel 1: Festlegen von Azure Storage Container ACL nach Name</span><span class="sxs-lookup"><span data-stu-id="2858a-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="2858a-109">Mit diesem Befehl wird ein Container ohne öffentlichen Zugriff erstellt.</span><span class="sxs-lookup"><span data-stu-id="2858a-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="2858a-110">Beispiel 2: Festlegen von Azure Storage Container ACL mithilfe der Pipeline</span><span class="sxs-lookup"><span data-stu-id="2858a-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="2858a-111">Dieser Befehl ruft alle Speichercontainer ab, deren Name mit dem Container beginnt, und übergibt dann das Ergebnis an die Pipeline, um die Berechtigung für alle Container an den Blobzugriff zu legen.</span><span class="sxs-lookup"><span data-stu-id="2858a-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="2858a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2858a-112">PARAMETERS</span></span>

### <span data-ttu-id="2858a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2858a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2858a-114">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2858a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2858a-115">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2858a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2858a-116">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2858a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2858a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2858a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2858a-118">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="2858a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2858a-119">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="2858a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2858a-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2858a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2858a-121">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="2858a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2858a-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="2858a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="2858a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="2858a-123">-Context</span></span>
<span data-ttu-id="2858a-124">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="2858a-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2858a-125">Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="2858a-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2858a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2858a-126">-DefaultProfile</span></span>
<span data-ttu-id="2858a-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2858a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2858a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2858a-128">-Name</span></span>
<span data-ttu-id="2858a-129">Gibt einen Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="2858a-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="2858a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2858a-130">-PassThru</span></span>
<span data-ttu-id="2858a-131">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2858a-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2858a-132">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2858a-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2858a-133">-Permission</span><span class="sxs-lookup"><span data-stu-id="2858a-133">-Permission</span></span>
<span data-ttu-id="2858a-134">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="2858a-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="2858a-135">Standardmäßig kann nur vom Besitzer des Speicherkontos auf den Container und alle darin gespeicherten Blobs zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="2858a-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="2858a-136">Wenn Sie anonymen Benutzern Leseberechtigungen für einen Container und dessen Blobs erteilen möchten, können Sie die Containerberechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2858a-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="2858a-137">Anonyme Benutzer können Blobs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="2858a-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="2858a-138">Die zulässigen Werte für diesen Parameter sind: --Container.</span><span class="sxs-lookup"><span data-stu-id="2858a-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="2858a-139">Bietet vollständigen Lesezugriff auf einen Container und seine Blobs.</span><span class="sxs-lookup"><span data-stu-id="2858a-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="2858a-140">Clients können Blobs im Container über eine anonyme Anforderung aufzählen, jedoch keine Container im Speicherkonto aufzählen.</span><span class="sxs-lookup"><span data-stu-id="2858a-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="2858a-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="2858a-141">--Blob.</span></span>
<span data-ttu-id="2858a-142">Ermöglicht den Lesezugriff auf Blobdaten in einem Container über anonyme Anfragen, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="2858a-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="2858a-143">Clients können blobs im Container nicht mithilfe einer anonymen Anforderung aufzählen.</span><span class="sxs-lookup"><span data-stu-id="2858a-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="2858a-144">--Aus.</span><span class="sxs-lookup"><span data-stu-id="2858a-144">--Off.</span></span>
<span data-ttu-id="2858a-145">Schränkt den Zugriff nur auf den Besitzer des Speicherkontos ein.</span><span class="sxs-lookup"><span data-stu-id="2858a-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858a-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2858a-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2858a-147">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="2858a-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2858a-148">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2858a-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="2858a-149">Serverseitige Auszeit für jede Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2858a-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="2858a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2858a-150">CommonParameters</span></span>
<span data-ttu-id="2858a-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2858a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2858a-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2858a-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2858a-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2858a-153">INPUTS</span></span>

### <span data-ttu-id="2858a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2858a-154">System.String</span></span>

### <span data-ttu-id="2858a-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2858a-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2858a-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2858a-156">OUTPUTS</span></span>

### <span data-ttu-id="2858a-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2858a-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="2858a-158">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2858a-158">NOTES</span></span>

## <span data-ttu-id="2858a-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2858a-159">RELATED LINKS</span></span>

[<span data-ttu-id="2858a-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2858a-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="2858a-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2858a-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="2858a-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2858a-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


