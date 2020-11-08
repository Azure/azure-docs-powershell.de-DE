---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176221"
---
# <span data-ttu-id="7465f-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7465f-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="7465f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7465f-102">SYNOPSIS</span></span>
<span data-ttu-id="7465f-103">Listet die Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="7465f-103">Lists the storage containers.</span></span>

## <span data-ttu-id="7465f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7465f-104">SYNTAX</span></span>

### <span data-ttu-id="7465f-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="7465f-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7465f-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="7465f-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7465f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7465f-107">DESCRIPTION</span></span>
<span data-ttu-id="7465f-108">Das Cmdlet " **Get-AzStorageContainer** " listet die Speichercontainer auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7465f-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="7465f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7465f-109">EXAMPLES</span></span>

### <span data-ttu-id="7465f-110">Beispiel 1: Abrufen des Azure Storage-BLOBs nach Name</span><span class="sxs-lookup"><span data-stu-id="7465f-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="7465f-111">In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="7465f-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="7465f-112">Beispiel 2: Abrufen des Azure-Speichercontainers nach dem Containernamen Präfix</span><span class="sxs-lookup"><span data-stu-id="7465f-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="7465f-113">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="7465f-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="7465f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7465f-114">PARAMETERS</span></span>

### <span data-ttu-id="7465f-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7465f-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7465f-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7465f-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7465f-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="7465f-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7465f-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7465f-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7465f-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7465f-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7465f-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="7465f-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7465f-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="7465f-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7465f-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="7465f-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7465f-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="7465f-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7465f-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="7465f-124">The default value is 10.</span></span>

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

### <span data-ttu-id="7465f-125">-Context</span><span class="sxs-lookup"><span data-stu-id="7465f-125">-Context</span></span>
<span data-ttu-id="7465f-126">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="7465f-126">Specifies the storage context.</span></span>
<span data-ttu-id="7465f-127">Sie können das New-AzStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7465f-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="7465f-128">Die Container Berechtigungen werden nicht abgerufen, wenn Sie einen aus SAS-Token erstellten Speicherkontext verwenden, da für Abfrage Container Berechtigungen speicherkontoschlüssel erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7465f-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="7465f-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="7465f-129">-ContinuationToken</span></span>
<span data-ttu-id="7465f-130">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="7465f-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="7465f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7465f-131">-DefaultProfile</span></span>
<span data-ttu-id="7465f-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7465f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7465f-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7465f-133">-MaxCount</span></span>
<span data-ttu-id="7465f-134">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7465f-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="7465f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7465f-135">-Name</span></span>
<span data-ttu-id="7465f-136">Gibt den Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="7465f-136">Specifies the container name.</span></span>
<span data-ttu-id="7465f-137">Wenn Containername leer ist, listet das Cmdlet alle Container auf.</span><span class="sxs-lookup"><span data-stu-id="7465f-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="7465f-138">Andernfalls werden alle Container aufgelistet, die dem angegebenen Namen oder dem regulären Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7465f-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="7465f-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7465f-139">-Prefix</span></span>
<span data-ttu-id="7465f-140">Gibt ein Präfix an, das im Namen des Containers oder Containers verwendet wird, den Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="7465f-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="7465f-141">Sie können damit alle Container finden, die mit der gleichen Zeichenfolge beginnen, wie "mein" oder "Test".</span><span class="sxs-lookup"><span data-stu-id="7465f-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="7465f-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7465f-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7465f-143">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="7465f-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7465f-144">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7465f-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7465f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7465f-145">CommonParameters</span></span>
<span data-ttu-id="7465f-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7465f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7465f-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7465f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7465f-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7465f-148">INPUTS</span></span>

### <span data-ttu-id="7465f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7465f-149">System.String</span></span>

### <span data-ttu-id="7465f-150">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7465f-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7465f-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7465f-151">OUTPUTS</span></span>

### <span data-ttu-id="7465f-152">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7465f-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="7465f-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="7465f-153">NOTES</span></span>

## <span data-ttu-id="7465f-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7465f-154">RELATED LINKS</span></span>

[<span data-ttu-id="7465f-155">Neu – AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7465f-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="7465f-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7465f-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="7465f-157">Satz-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7465f-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


