---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66845678619a7777bbda9257aa208393b0fa178c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475690"
---
# <span data-ttu-id="4929b-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4929b-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="4929b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4929b-102">SYNOPSIS</span></span>
<span data-ttu-id="4929b-103">Listet die Speichercontainer auf.</span><span class="sxs-lookup"><span data-stu-id="4929b-103">Lists the storage containers.</span></span>

## <span data-ttu-id="4929b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4929b-104">SYNTAX</span></span>

### <span data-ttu-id="4929b-105">Containername (Standard)</span><span class="sxs-lookup"><span data-stu-id="4929b-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4929b-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="4929b-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4929b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4929b-107">DESCRIPTION</span></span>
<span data-ttu-id="4929b-108">Das Cmdlet " **Get-AzureStorageContainer** " listet die Speichercontainer auf, die dem Speicherkonto in Azure zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4929b-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4929b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4929b-109">EXAMPLES</span></span>

### <span data-ttu-id="4929b-110">Beispiel 1: Abrufen des Azure Storage-BLOBs nach Name</span><span class="sxs-lookup"><span data-stu-id="4929b-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="4929b-111">In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="4929b-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="4929b-112">Beispiel 2: Abrufen des Azure-Speichercontainers nach dem Containernamen Präfix</span><span class="sxs-lookup"><span data-stu-id="4929b-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="4929b-113">In diesem Beispiel wird der *prefix* -Parameter verwendet, um eine Liste aller Container mit einem Namen zurückzugeben, der mit Container beginnt.</span><span class="sxs-lookup"><span data-stu-id="4929b-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="4929b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4929b-114">PARAMETERS</span></span>

### <span data-ttu-id="4929b-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4929b-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4929b-116">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4929b-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4929b-117">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="4929b-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4929b-118">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4929b-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4929b-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4929b-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4929b-120">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="4929b-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4929b-121">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="4929b-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4929b-122">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="4929b-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4929b-123">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="4929b-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4929b-124">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="4929b-124">The default value is 10.</span></span>

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

### <span data-ttu-id="4929b-125">-Context</span><span class="sxs-lookup"><span data-stu-id="4929b-125">-Context</span></span>
<span data-ttu-id="4929b-126">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="4929b-126">Specifies the storage context.</span></span>
<span data-ttu-id="4929b-127">Sie können das New-AzureStorageContext-Cmdlet verwenden, um es zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4929b-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4929b-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="4929b-128">-ContinuationToken</span></span>
<span data-ttu-id="4929b-129">Gibt ein Fortsetzungstoken für die BLOB-Liste an.</span><span class="sxs-lookup"><span data-stu-id="4929b-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="4929b-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4929b-130">-MaxCount</span></span>
<span data-ttu-id="4929b-131">Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4929b-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="4929b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4929b-132">-Name</span></span>
<span data-ttu-id="4929b-133">Gibt den Containernamen an.</span><span class="sxs-lookup"><span data-stu-id="4929b-133">Specifies the container name.</span></span>
<span data-ttu-id="4929b-134">Wenn Containername leer ist, listet das Cmdlet alle Container auf.</span><span class="sxs-lookup"><span data-stu-id="4929b-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="4929b-135">Andernfalls werden alle Container aufgelistet, die dem angegebenen Namen oder dem regulären Namensmuster entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4929b-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4929b-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4929b-136">-Prefix</span></span>
<span data-ttu-id="4929b-137">Gibt ein Präfix an, das im Namen des Containers oder Containers verwendet wird, den Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="4929b-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="4929b-138">Sie können damit alle Container finden, die mit der gleichen Zeichenfolge beginnen, wie "mein" oder "Test".</span><span class="sxs-lookup"><span data-stu-id="4929b-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="4929b-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4929b-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4929b-140">Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="4929b-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4929b-141">Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4929b-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4929b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4929b-142">CommonParameters</span></span>
<span data-ttu-id="4929b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4929b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4929b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4929b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4929b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4929b-145">INPUTS</span></span>

## <span data-ttu-id="4929b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4929b-146">OUTPUTS</span></span>

## <span data-ttu-id="4929b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="4929b-147">NOTES</span></span>

## <span data-ttu-id="4929b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4929b-148">RELATED LINKS</span></span>

[<span data-ttu-id="4929b-149">Neu – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4929b-149">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="4929b-150">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4929b-150">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="4929b-151">Satz-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4929b-151">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


