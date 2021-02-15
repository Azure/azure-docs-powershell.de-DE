---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145441"
---
# <span data-ttu-id="f0be1-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f0be1-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="f0be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0be1-102">SYNOPSIS</span></span>
<span data-ttu-id="f0be1-103">Listet die Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="f0be1-103">Lists the storage containers.</span></span>

## <span data-ttu-id="f0be1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0be1-104">SYNTAX</span></span>

### <span data-ttu-id="f0be1-105">ContainerName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0be1-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f0be1-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="f0be1-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f0be1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0be1-107">DESCRIPTION</span></span>
<span data-ttu-id="f0be1-108">Das **Cmdlet "Get-AzStorageContainer"** listet die Speichercontainer auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f0be1-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="f0be1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0be1-109">EXAMPLES</span></span>

### <span data-ttu-id="f0be1-110">Beispiel 1: Azure Storage BLOB nach Name erhalten</span><span class="sxs-lookup"><span data-stu-id="f0be1-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="f0be1-111">In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit einem Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="f0be1-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="f0be1-112">Beispiel 2: Azure Storage Container nach Containernamenpräfix erhalten</span><span class="sxs-lookup"><span data-stu-id="f0be1-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="f0be1-113">In diesem Beispiel wird der *Präfixparameter* verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit dem Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="f0be1-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="f0be1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0be1-114">PARAMETERS</span></span>

### <span data-ttu-id="f0be1-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0be1-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f0be1-116">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0be1-117">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0be1-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0be1-118">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f0be1-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f0be1-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f0be1-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f0be1-120">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f0be1-121">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="f0be1-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f0be1-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f0be1-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f0be1-123">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="f0be1-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f0be1-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="f0be1-124">The default value is 10.</span></span>

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

### <span data-ttu-id="f0be1-125">-Context</span><span class="sxs-lookup"><span data-stu-id="f0be1-125">-Context</span></span>
<span data-ttu-id="f0be1-126">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-126">Specifies the storage context.</span></span>
<span data-ttu-id="f0be1-127">Zum Erstellen können Sie das cmdlet New-AzStorageContext erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0be1-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="f0be1-128">Die Containerberechtigungen werden nicht abgerufen, wenn Sie einen aus dem SAS-Token erstellten Speicherkontext verwenden, da für Abfragecontainerberechtigungen die Schlüsselberechtigung für das Speicherkonto erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f0be1-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="f0be1-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="f0be1-129">-ContinuationToken</span></span>
<span data-ttu-id="f0be1-130">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="f0be1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0be1-131">-DefaultProfile</span></span>
<span data-ttu-id="f0be1-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0be1-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0be1-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f0be1-133">-MaxCount</span></span>
<span data-ttu-id="f0be1-134">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f0be1-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="f0be1-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f0be1-135">-Name</span></span>
<span data-ttu-id="f0be1-136">Gibt den Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-136">Specifies the container name.</span></span>
<span data-ttu-id="f0be1-137">Wenn der Containername leer ist, werden im Cmdlet alle Container aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0be1-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="f0be1-138">Andernfalls werden alle Container aufgeführt, die dem angegebenen Namen oder dem normalen Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="f0be1-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="f0be1-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="f0be1-139">-Prefix</span></span>
<span data-ttu-id="f0be1-140">Gibt ein Präfix an, das im Namen des Containers oder der Container verwendet wird, den bzw. die Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="f0be1-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="f0be1-141">Sie können dies verwenden, um alle Container zu finden, die mit derselben Zeichenfolge beginnen, z. B. "my" oder "test".</span><span class="sxs-lookup"><span data-stu-id="f0be1-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="f0be1-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0be1-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f0be1-143">Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="f0be1-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f0be1-144">Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f0be1-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f0be1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0be1-145">CommonParameters</span></span>
<span data-ttu-id="f0be1-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0be1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0be1-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0be1-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0be1-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0be1-148">INPUTS</span></span>

### <span data-ttu-id="f0be1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f0be1-149">System.String</span></span>

### <span data-ttu-id="f0be1-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0be1-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f0be1-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0be1-151">OUTPUTS</span></span>

### <span data-ttu-id="f0be1-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f0be1-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="f0be1-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0be1-153">NOTES</span></span>

## <span data-ttu-id="f0be1-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0be1-154">RELATED LINKS</span></span>

[<span data-ttu-id="f0be1-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f0be1-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="f0be1-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f0be1-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="f0be1-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f0be1-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


