---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501009"
---
# <span data-ttu-id="22c1d-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22c1d-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="22c1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="22c1d-103">Listet die Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="22c1d-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22c1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c1d-104">SYNTAX</span></span>

### <span data-ttu-id="22c1d-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="22c1d-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="22c1d-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="22c1d-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="22c1d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22c1d-107">DESCRIPTION</span></span>
<span data-ttu-id="22c1d-108">Das Cmdlet " **Get-AzureStorageContainer** " listet die Speichercontainer auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="22c1d-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="22c1d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22c1d-109">EXAMPLES</span></span>

### <span data-ttu-id="22c1d-110">Beispiel 1: Abrufen des Azure Storage-BLOBs nach Name</span><span class="sxs-lookup"><span data-stu-id="22c1d-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="22c1d-111">In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="22c1d-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="22c1d-112">Beispiel 2: Abrufen des Azure-Speichercontainers nach dem Containernamen Präfix</span><span class="sxs-lookup"><span data-stu-id="22c1d-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="22c1d-113">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="22c1d-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="22c1d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c1d-114">PARAMETERS</span></span>

### <span data-ttu-id="22c1d-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="22c1d-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="22c1d-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="22c1d-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="22c1d-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="22c1d-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="22c1d-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="22c1d-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="22c1d-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="22c1d-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="22c1d-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="22c1d-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="22c1d-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="22c1d-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="22c1d-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="22c1d-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="22c1d-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="22c1d-124">The default value is 10.</span></span>

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

### <span data-ttu-id="22c1d-125">-Context</span><span class="sxs-lookup"><span data-stu-id="22c1d-125">-Context</span></span>
<span data-ttu-id="22c1d-126">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-126">Specifies the storage context.</span></span>
<span data-ttu-id="22c1d-127">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22c1d-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="22c1d-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="22c1d-128">-ContinuationToken</span></span>
<span data-ttu-id="22c1d-129">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-129">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1d-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="22c1d-130">-MaxCount</span></span>
<span data-ttu-id="22c1d-131">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="22c1d-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="22c1d-132">-Name</span><span class="sxs-lookup"><span data-stu-id="22c1d-132">-Name</span></span>
<span data-ttu-id="22c1d-133">Gibt den Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-133">Specifies the container name.</span></span>
<span data-ttu-id="22c1d-134">Wenn Containername leer ist, listet das Cmdlet alle Container auf.</span><span class="sxs-lookup"><span data-stu-id="22c1d-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="22c1d-135">Andernfalls werden alle Container aufgelistet, die dem angegebenen Namen oder dem regulären Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="22c1d-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="22c1d-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="22c1d-136">-Prefix</span></span>
<span data-ttu-id="22c1d-137">Gibt ein Präfix an, das im Namen des Containers oder Containers verwendet wird, den Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="22c1d-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="22c1d-138">Sie können damit alle Container finden, die mit der gleichen Zeichenfolge beginnen, wie "mein" oder "Test".</span><span class="sxs-lookup"><span data-stu-id="22c1d-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c1d-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="22c1d-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="22c1d-140">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="22c1d-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="22c1d-141">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="22c1d-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="22c1d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c1d-142">CommonParameters</span></span>
<span data-ttu-id="22c1d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c1d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c1d-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22c1d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c1d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22c1d-145">INPUTS</span></span>

### <span data-ttu-id="22c1d-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="22c1d-146">IStorageContext</span></span>

<span data-ttu-id="22c1d-147">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="22c1d-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="22c1d-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="22c1d-148">String</span></span>

<span data-ttu-id="22c1d-149">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="22c1d-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="22c1d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22c1d-150">OUTPUTS</span></span>

### <span data-ttu-id="22c1d-151">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22c1d-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="22c1d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="22c1d-152">NOTES</span></span>

## <span data-ttu-id="22c1d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22c1d-153">RELATED LINKS</span></span>

[<span data-ttu-id="22c1d-154">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22c1d-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="22c1d-155">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22c1d-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="22c1d-156">Satz-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="22c1d-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


