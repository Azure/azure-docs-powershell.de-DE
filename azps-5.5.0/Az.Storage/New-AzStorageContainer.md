---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165673"
---
# <span data-ttu-id="3f467-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f467-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="3f467-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f467-102">SYNOPSIS</span></span>
<span data-ttu-id="3f467-103">Erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="3f467-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="3f467-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f467-104">SYNTAX</span></span>

### <span data-ttu-id="3f467-105">ContainerName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f467-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3f467-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3f467-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3f467-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f467-107">DESCRIPTION</span></span>
<span data-ttu-id="3f467-108">Das **Cmdlet "New-AzStorageContainer"** erstellt einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="3f467-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="3f467-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f467-109">EXAMPLES</span></span>

### <span data-ttu-id="3f467-110">Beispiel 1: Erstellen eines Azure -Speichercontainers</span><span class="sxs-lookup"><span data-stu-id="3f467-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="3f467-111">Mit diesem Befehl wird ein Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f467-111">This command creates a storage container.</span></span>

### <span data-ttu-id="3f467-112">Beispiel 2: Erstellen mehrerer Azure -Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="3f467-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="3f467-113">In diesem Beispiel werden mehrere Speichercontainer erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f467-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="3f467-114">Sie verwendet die **Split-Methode** der **.NET-Zeichenfolgenklasse** und übergibt dann die Namen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f467-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="3f467-115">Beispiel 3: Erstellen eines Azure -Speichercontainers mit Verschlüsselungsbereich</span><span class="sxs-lookup"><span data-stu-id="3f467-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="3f467-116">Mit diesem Befehl wird ein Speichercontainer erstellt, der den Standardverschlüsselungsbereich als MyencryptScope enthält, und den BLOB-Upload mit einem anderen Verschlüsselungsbereich in diesen Container vorab zurückverwenden.</span><span class="sxs-lookup"><span data-stu-id="3f467-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="3f467-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f467-117">PARAMETERS</span></span>

### <span data-ttu-id="3f467-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f467-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3f467-119">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="3f467-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3f467-120">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f467-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3f467-121">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3f467-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3f467-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3f467-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3f467-123">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="3f467-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3f467-124">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="3f467-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3f467-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="3f467-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3f467-126">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3f467-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3f467-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3f467-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3f467-128">-Context</span><span class="sxs-lookup"><span data-stu-id="3f467-128">-Context</span></span>
<span data-ttu-id="3f467-129">Gibt einen Kontext für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="3f467-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="3f467-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="3f467-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="3f467-131">Standardmäßig verwendet der Container den angegebenen Verschlüsselungsbereich für alle Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="3f467-131">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="3f467-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f467-132">-DefaultProfile</span></span>
<span data-ttu-id="3f467-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f467-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f467-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3f467-134">-Name</span></span>
<span data-ttu-id="3f467-135">Gibt einen Namen für den neuen Container an.</span><span class="sxs-lookup"><span data-stu-id="3f467-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="3f467-136">-Permission</span><span class="sxs-lookup"><span data-stu-id="3f467-136">-Permission</span></span>
<span data-ttu-id="3f467-137">Gibt die Ebene des öffentlichen Zugriffs auf diesen Container an.</span><span class="sxs-lookup"><span data-stu-id="3f467-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="3f467-138">Standardmäßig kann nur der Besitzer des Speicherkontos auf den Container und alle darin gespeicherten BLOBS zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3f467-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="3f467-139">Wenn Sie anonymen Benutzern Leseberechtigungen für einen Container und dessen BLOBs erteilen möchten, können Sie die Containerberechtigungen zum Aktivieren des öffentlichen Zugriffs festlegen.</span><span class="sxs-lookup"><span data-stu-id="3f467-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="3f467-140">Anonyme Benutzer können Blobs in einem öffentlich verfügbaren Container lesen, ohne die Anforderung zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="3f467-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="3f467-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="3f467-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3f467-142">Container.</span><span class="sxs-lookup"><span data-stu-id="3f467-142">Container.</span></span>
<span data-ttu-id="3f467-143">Bietet vollständigen Lesezugriff auf einen Container und dessen Blobs.</span><span class="sxs-lookup"><span data-stu-id="3f467-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="3f467-144">Clients können Blobs im Container über anonyme Anforderung aufzählen, jedoch keine Container im Speicherkonto aufzählen.</span><span class="sxs-lookup"><span data-stu-id="3f467-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="3f467-145">BLOB.</span><span class="sxs-lookup"><span data-stu-id="3f467-145">Blob.</span></span>
<span data-ttu-id="3f467-146">Bietet Lesezugriff auf BLOB-Daten im gesamten Container über eine anonyme Anforderung, bietet aber keinen Zugriff auf Containerdaten.</span><span class="sxs-lookup"><span data-stu-id="3f467-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="3f467-147">Clients können blobs im Container nicht mithilfe einer anonymen Anforderung aufzählen.</span><span class="sxs-lookup"><span data-stu-id="3f467-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="3f467-148">"Aus" aus.</span><span class="sxs-lookup"><span data-stu-id="3f467-148">Off.</span></span>
<span data-ttu-id="3f467-149">Damit wird der Zugriff auf den Besitzer des Speicherkontos beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3f467-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="3f467-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="3f467-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="3f467-151">Blocküberschreibung des Verschlüsselungsbereichs vom Container standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="3f467-151">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="3f467-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f467-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3f467-153">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="3f467-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3f467-154">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3f467-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3f467-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f467-155">CommonParameters</span></span>
<span data-ttu-id="3f467-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f467-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f467-157">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f467-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f467-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f467-158">INPUTS</span></span>

### <span data-ttu-id="3f467-159">System.String</span><span class="sxs-lookup"><span data-stu-id="3f467-159">System.String</span></span>

### <span data-ttu-id="3f467-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3f467-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3f467-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f467-161">OUTPUTS</span></span>

### <span data-ttu-id="3f467-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f467-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3f467-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f467-163">NOTES</span></span>

## <span data-ttu-id="3f467-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f467-164">RELATED LINKS</span></span>

[<span data-ttu-id="3f467-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f467-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="3f467-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f467-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="3f467-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3f467-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


