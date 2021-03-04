---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933379"
---
# <span data-ttu-id="c7b8a-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7b8a-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="c7b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b8a-103">Listet die Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-103">Lists the storage containers.</span></span>

## <span data-ttu-id="c7b8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7b8a-104">SYNTAX</span></span>

### <span data-ttu-id="c7b8a-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7b8a-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c7b8a-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="c7b8a-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c7b8a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7b8a-107">DESCRIPTION</span></span>
<span data-ttu-id="c7b8a-108">Im **Get-AzStorageContainer-Cmdlet** werden die Speichercontainer aufgeführt, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c7b8a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7b8a-109">EXAMPLES</span></span>

### <span data-ttu-id="c7b8a-110">Beispiel 1: Azure Storage Blob nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="c7b8a-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="c7b8a-111">In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit container beginnt.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="c7b8a-112">Beispiel 2: Azure Storage-Container nach Containernamenpräfix erhalten</span><span class="sxs-lookup"><span data-stu-id="c7b8a-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="c7b8a-113">In diesem Beispiel wird der *Parameter Präfix* verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit container beginnt.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="c7b8a-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7b8a-114">PARAMETERS</span></span>

### <span data-ttu-id="c7b8a-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7b8a-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c7b8a-116">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c7b8a-117">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c7b8a-118">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c7b8a-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c7b8a-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c7b8a-120">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c7b8a-121">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c7b8a-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c7b8a-123">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c7b8a-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-124">The default value is 10.</span></span>

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

### <span data-ttu-id="c7b8a-125">-Context</span><span class="sxs-lookup"><span data-stu-id="c7b8a-125">-Context</span></span>
<span data-ttu-id="c7b8a-126">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-126">Specifies the storage context.</span></span>
<span data-ttu-id="c7b8a-127">Zum Erstellen können Sie das cmdlet New-AzStorageContext verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c7b8a-128">Die Containerberechtigungen werden nicht abgerufen, wenn Sie einen Speicherkontext verwenden, der aus dem SAS-Token erstellt wurde, da für Abfragecontainerberechtigungen die Berechtigung Speicherkontoschlüssel erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="c7b8a-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="c7b8a-129">-ContinuationToken</span></span>
<span data-ttu-id="c7b8a-130">Gibt ein Fortsetzungstoken für die Blobliste an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b8a-131">-DefaultProfile</span></span>
<span data-ttu-id="c7b8a-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b8a-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c7b8a-133">-MaxCount</span></span>
<span data-ttu-id="c7b8a-134">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="c7b8a-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c7b8a-135">-Name</span></span>
<span data-ttu-id="c7b8a-136">Gibt den Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-136">Specifies the container name.</span></span>
<span data-ttu-id="c7b8a-137">Wenn der Containername leer ist, werden im Cmdlet alle Container aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="c7b8a-138">Andernfalls werden alle Container aufgeführt, die dem angegebenen Namen oder dem normalen Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8a-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c7b8a-139">-Prefix</span></span>
<span data-ttu-id="c7b8a-140">Gibt ein Präfix an, das im Namen des Containers oder der Container verwendet wird, den Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="c7b8a-141">Damit können Sie alle Container suchen, die mit derselben Zeichenfolge beginnen, z. B. "my" oder "test".</span><span class="sxs-lookup"><span data-stu-id="c7b8a-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b8a-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c7b8a-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c7b8a-143">Gibt das dienstseitige Zeitintervall in Sekunden für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c7b8a-144">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c7b8a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b8a-145">CommonParameters</span></span>
<span data-ttu-id="c7b8a-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b8a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b8a-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b8a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b8a-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7b8a-148">INPUTS</span></span>

### <span data-ttu-id="c7b8a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c7b8a-149">System.String</span></span>

### <span data-ttu-id="c7b8a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c7b8a-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c7b8a-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7b8a-151">OUTPUTS</span></span>

### <span data-ttu-id="c7b8a-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7b8a-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c7b8a-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c7b8a-153">NOTES</span></span>

## <span data-ttu-id="c7b8a-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c7b8a-154">RELATED LINKS</span></span>

[<span data-ttu-id="c7b8a-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7b8a-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="c7b8a-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c7b8a-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="c7b8a-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c7b8a-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


