---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: 31a8d6cbb205b451233bdc72793fb45443350fdd
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93665419"
---
# <span data-ttu-id="cca7d-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cca7d-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="cca7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cca7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cca7d-103">Ruft eine Liste der Dateifreigaben ab.</span><span class="sxs-lookup"><span data-stu-id="cca7d-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cca7d-104">SYNTAX</span></span>

### <span data-ttu-id="cca7d-105">MatchingPrefix (Standard)</span><span class="sxs-lookup"><span data-stu-id="cca7d-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cca7d-106">Spezifische</span><span class="sxs-lookup"><span data-stu-id="cca7d-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cca7d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cca7d-107">DESCRIPTION</span></span>
<span data-ttu-id="cca7d-108">Das Cmdlet " **Get-AzureStorageShare** " Ruft eine Liste der Dateifreigaben für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="cca7d-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="cca7d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cca7d-109">EXAMPLES</span></span>

### <span data-ttu-id="cca7d-110">Beispiel 1: Abrufen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="cca7d-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="cca7d-111">Dieser Befehl ruft die Dateifreigabe mit dem Namen ContosoShare06 ab.</span><span class="sxs-lookup"><span data-stu-id="cca7d-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="cca7d-112">Beispiel 2: Abrufen aller Dateifreigaben, die mit einer Zeichenfolge beginnen</span><span class="sxs-lookup"><span data-stu-id="cca7d-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="cca7d-113">Dieser Befehl ruft alle Dateifreigaben ab, deren Namen mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="cca7d-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="cca7d-114">Beispiel 3: Abrufen aller Dateifreigaben in einem angegebenen Kontext</span><span class="sxs-lookup"><span data-stu-id="cca7d-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="cca7d-115">Der erste Befehl verwendet das Cmdlet **New-AzureStorageContext** , um einen Kontext mithilfe des *lokalen* Parameters zu erstellen, und speichert dann dieses Kontextobjekt in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="cca7d-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="cca7d-116">Der zweite Befehl ruft die Dateifreigaben für das Kontextobjekt ab, das in $context gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="cca7d-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="cca7d-117">Beispiel 4: Abrufen eines Snapshots einer Dateifreigabe mit einem bestimmten Freigabenamen und einer Snapshotzeit</span><span class="sxs-lookup"><span data-stu-id="cca7d-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="cca7d-118">Dieser Befehl ruft einen Dateifreigabe-Schnappschuss mit einem bestimmten Freigabenamen und einer Snapshotzeit ab.</span><span class="sxs-lookup"><span data-stu-id="cca7d-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="cca7d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="cca7d-119">PARAMETERS</span></span>

### <span data-ttu-id="cca7d-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cca7d-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cca7d-121">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cca7d-122">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="cca7d-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cca7d-123">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="cca7d-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cca7d-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cca7d-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cca7d-125">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cca7d-126">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="cca7d-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cca7d-127">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="cca7d-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cca7d-128">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="cca7d-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cca7d-129">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="cca7d-129">The default value is 10.</span></span>

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

### <span data-ttu-id="cca7d-130">-Context</span><span class="sxs-lookup"><span data-stu-id="cca7d-130">-Context</span></span>
<span data-ttu-id="cca7d-131">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cca7d-132">Verwenden Sie zum Abrufen eines Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="cca7d-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="cca7d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca7d-133">-DefaultProfile</span></span>
<span data-ttu-id="cca7d-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cca7d-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca7d-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cca7d-135">-Name</span></span>
<span data-ttu-id="cca7d-136">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="cca7d-137">Dieses Cmdlet ruft die Dateifreigabe ab, die dieser Parameter angibt, oder Nothing, wenn Sie den Namen einer Dateifreigabe angeben, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cca7d-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="cca7d-138">-Prefix</span></span>
<span data-ttu-id="cca7d-139">Gibt das Präfix für Dateifreigaben an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="cca7d-140">Dieses Cmdlet ruft Dateifreigaben ab, die dem Präfix entsprechen, das dieser Parameter angibt, oder keine Dateifreigaben, wenn keine Dateifreigaben dem angegebenen Präfix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cca7d-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cca7d-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cca7d-142">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="cca7d-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="cca7d-143">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="cca7d-143">-SnapshotTime</span></span>
<span data-ttu-id="cca7d-144">Momentaufnahme des zu empfangenden Snapshots der Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="cca7d-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca7d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca7d-145">CommonParameters</span></span>
<span data-ttu-id="cca7d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca7d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca7d-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca7d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca7d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cca7d-148">INPUTS</span></span>

### <span data-ttu-id="cca7d-149">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cca7d-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cca7d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cca7d-150">OUTPUTS</span></span>

### <span data-ttu-id="cca7d-151">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cca7d-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="cca7d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="cca7d-152">NOTES</span></span>

## <span data-ttu-id="cca7d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cca7d-153">RELATED LINKS</span></span>

[<span data-ttu-id="cca7d-154">Neu – AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cca7d-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="cca7d-155">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="cca7d-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
