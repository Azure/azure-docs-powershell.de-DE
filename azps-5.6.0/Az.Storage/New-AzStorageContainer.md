---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: d726ec3fe70ca329f6e5c07ea7aae46de4ad048a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944542"
---
# <span data-ttu-id="b2cd3-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b2cd3-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="b2cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cd3-103">Erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="b2cd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2cd3-104">SYNTAX</span></span>

### <span data-ttu-id="b2cd3-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2cd3-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b2cd3-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b2cd3-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b2cd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="b2cd3-108">Das **Cmdlet New-AzStorageContainer** erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="b2cd3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="b2cd3-110">Beispiel 1: Erstellen eines Azure-Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="b2cd3-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="b2cd3-111">Mit diesem Befehl wird ein Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-111">This command creates a storage container.</span></span>

### <span data-ttu-id="b2cd3-112">Beispiel 2: Erstellen mehrerer Azure-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="b2cd3-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="b2cd3-113">In diesem Beispiel werden mehrere Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="b2cd3-114">Sie verwendet die **Split-Methode** der .NET **String-Klasse** und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="b2cd3-115">Beispiel 3: Erstellen eines Azure-Speichercontainers mit Verschlüsselungsbereich</span><span class="sxs-lookup"><span data-stu-id="b2cd3-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="b2cd3-116">Mit diesem Befehl wird ein Speichercontainer mit dem Standardverschlüsselungsbereich als Myencryptscope erstellt und der Blobupload mit einem anderen Verschlüsselungsbereich in diesen Container vorverwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="b2cd3-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b2cd3-117">PARAMETERS</span></span>

### <span data-ttu-id="b2cd3-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2cd3-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b2cd3-119">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b2cd3-120">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b2cd3-121">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b2cd3-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b2cd3-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b2cd3-123">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b2cd3-124">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b2cd3-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b2cd3-126">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b2cd3-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-127">The default value is 10.</span></span>

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

### <span data-ttu-id="b2cd3-128">-Context</span><span class="sxs-lookup"><span data-stu-id="b2cd3-128">-Context</span></span>
<span data-ttu-id="b2cd3-129">Gibt einen Kontext für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="b2cd3-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b2cd3-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="b2cd3-131">Standardmäßig wird der Container für die Verwendung des angegebenen Verschlüsselungsbereichs für alle Schreibvorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cd3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cd3-132">-DefaultProfile</span></span>
<span data-ttu-id="b2cd3-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2cd3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b2cd3-134">-Name</span></span>
<span data-ttu-id="b2cd3-135">Gibt einen Namen für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="b2cd3-136">-Permission</span><span class="sxs-lookup"><span data-stu-id="b2cd3-136">-Permission</span></span>
<span data-ttu-id="b2cd3-137">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="b2cd3-138">Standardmäßig kann nur vom Besitzer des Speicherkontos auf den Container und alle darin gespeicherten Blobs zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="b2cd3-139">Wenn Sie anonymen Benutzern Leseberechtigungen für einen Container und dessen Blobs erteilen möchten, können Sie die Containerberechtigungen festlegen, um den öffentlichen Zugriff zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="b2cd3-140">Anonyme Benutzer können Blobs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="b2cd3-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="b2cd3-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2cd3-142">Container.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-142">Container.</span></span>
<span data-ttu-id="b2cd3-143">Bietet vollständigen Lesezugriff auf einen Container und seine Blobs.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="b2cd3-144">Clients können Blobs im Container über eine anonyme Anforderung aufzählen, jedoch keine Container im Speicherkonto aufzählen.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="b2cd3-145">Blob.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-145">Blob.</span></span>
<span data-ttu-id="b2cd3-146">Ermöglicht den Lesezugriff auf Blobdaten im gesamten Container über eine anonyme Anforderung, bietet jedoch keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="b2cd3-147">Clients können blobs im Container nicht mithilfe einer anonymen Anforderung aufzählen.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="b2cd3-148">Aus.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-148">Off.</span></span>
<span data-ttu-id="b2cd3-149">Dies schränkt den Zugriff nur auf den Besitzer des Speicherkontos ein.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="b2cd3-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="b2cd3-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="b2cd3-151">Block override of encryption scope from the container default.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cd3-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b2cd3-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b2cd3-153">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b2cd3-154">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b2cd3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cd3-155">CommonParameters</span></span>
<span data-ttu-id="b2cd3-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cd3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cd3-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cd3-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cd3-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cd3-158">INPUTS</span></span>

### <span data-ttu-id="b2cd3-159">System.String</span><span class="sxs-lookup"><span data-stu-id="b2cd3-159">System.String</span></span>

### <span data-ttu-id="b2cd3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b2cd3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b2cd3-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cd3-161">OUTPUTS</span></span>

### <span data-ttu-id="b2cd3-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b2cd3-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="b2cd3-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b2cd3-163">NOTES</span></span>

## <span data-ttu-id="b2cd3-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b2cd3-164">RELATED LINKS</span></span>

[<span data-ttu-id="b2cd3-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b2cd3-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="b2cd3-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b2cd3-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="b2cd3-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b2cd3-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


